# 如何实现无状态的JWT令牌自动续约

## 概念
JSON Web Token (JWT)是一个开放标准(RFC 7519) <font style="color:rgb(51, 51, 51);">，它定义了一种简洁的、自包含的方法用于通信双方之间以 </font><font style="color:rgb(0, 82, 217);">JSON</font><font style="color:rgb(51, 51, 51);"> 对象的形式安全地传输信息。这种信息可以被验证和信任，因为它是</font><font style="color:rgb(0, 82, 217);">数字签名</font><font style="color:rgb(51, 51, 51);">的。JWT通常用于互联网应用程序中，用于身份验证和授权。 </font>**<font style="color:rgb(51, 51, 51);">JWT 和 传统 Token 的区别</font>**

| | <font style="color:rgb(103, 116, 137);">JWT</font> | <font style="color:rgb(103, 116, 137);">传统 Token</font> |
| --- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">存储位置</font> | <font style="color:rgb(51, 51, 51);">JWT通常存储在客户端</font> | <font style="color:rgb(51, 51, 51);">传统的Token如Cookies和Session Tokens通常在服务器端存储状态</font> |
| <font style="color:rgb(51, 51, 51);">传输方式</font> | <font style="color:rgb(51, 51, 51);">JWT作为HTTP请求的一部分传输，可以直接在请求的Header中</font> | <font style="color:rgb(51, 51, 51);">传统Token通常通过Cookie在浏览器和服务器之间传输</font> |
| <font style="color:rgb(51, 51, 51);">状态管理</font> | <font style="color:rgb(51, 51, 51);">JWT是自包含的，不依赖于服务器的会话状态，减轻服务器负担。</font> | <font style="color:rgb(51, 51, 51);">传统Token通常与服务器的会话状态绑定，服务器需要存储用户的会话信息，这可能导致更高的服务器负载和状态管理复杂性。</font> |
| <font style="color:rgb(51, 51, 51);">安全性和隐私</font> | <font style="color:rgb(51, 51, 51);">JWT的所有信息都是加密的，并且可以设置权限，只有拥有正确密钥的用户才能解码信息。但是，如果密钥被泄露，那么所有的JWT都可能受到影响。</font> | <font style="color:rgb(51, 51, 51);">不包含敏感信息，因此不加密</font> |
| <font style="color:rgb(51, 51, 51);">跨域使用</font> | <font style="color:rgb(51, 51, 51);">由于 JWT 不依靠服务器状态，可以在不同域之间请求和传递用户信息，因此适合跨域请求</font> | <font style="color:rgb(51, 51, 51);">传统Token在跨域请求中可能需要服务器配置CORS（跨源资源共享）策略</font> |


#### <font style="color:rgb(0, 0, 0);">JWT 组成部分</font>
![1727097801626-ac7512a6-6f1e-45a2-bdc7-e6d0976d94b8.png](./img/eEKTfzmA-GzBAjM_/1727097801626-ac7512a6-6f1e-45a2-bdc7-e6d0976d94b8-802039.png)

**<font style="color:rgb(51, 51, 51);"></font>**

<font style="color:rgb(51, 51, 51);">由于JWT是自包含的，所以它不需要在</font>[<font style="color:rgb(51, 51, 51);">服务器</font>](https://cloud.tencent.com/act/pro/promotion-cvm?from_column=20065&from=20065)<font style="color:rgb(51, 51, 51);">上存储状态，这减少了攻击面，并允许用户在没有状态的系统中进行认证。同时，由于JWT是在客户端和服务器之间传输的，所以它也易于跨域使用。 以下是一段 JWT的内容，我们需要找到令牌中的用户名</font>



官网地址：[https://jwt.io](https://jwt.io)

## JWT 原理
JWT 的原理是，服务器认证以后，生成一个 JSON 对象，发回给用户，就像下面这样。



{

  "姓名": "诸葛",

  "角色": "管理员",

  "到期时间": "2028年12月11日0点0分"

}

以后，用户与服务端通信的时候，都要发回这个 JSON 对象。服务器完全只靠这个对象认定用户身份。为了防止用户篡改数据，服务器在生成这个对象的时候，会加上签名（详见后文）。



服务器就不保存任何 session 数据了，也就是说，服务器变成无状态了，从而比较容易实现扩展。

 

 ![1726752592121-0eec80fc-c0ef-4199-ac2d-ea9b96b18748.png](./img/eEKTfzmA-GzBAjM_/1726752592121-0eec80fc-c0ef-4199-ac2d-ea9b96b18748-504535.png)

认证流程流程说明：



浏览器发起请求登陆，用户携带用户名和密码等了



服务端验证身份，根据算法，将用户标识符打包生成 Token,



服务器返回JWT信息给浏览器，JWT不包含敏感信息



浏览器发起请求获取用户资料，把刚刚拿到的 Token一起发送给服务器



服务器发现数据中有 Token，验证身份是否合法



服务器根据当前Token解析返回该用户的用户资料



### 整体过程如下：
 

![1726750768983-2df0f2af-481d-4040-8eb3-3261cf86e87f.png](./img/eEKTfzmA-GzBAjM_/1726750768983-2df0f2af-481d-4040-8eb3-3261cf86e87f-891930.png)

![1726750803111-d3e786aa-fa6d-44cc-a74e-0ac62f5ddb61.png](./img/eEKTfzmA-GzBAjM_/1726750803111-d3e786aa-fa6d-44cc-a74e-0ac62f5ddb61-127867.png)

![1726750850740-12093993-b7e2-461d-b86d-535779bade7b.png](./img/eEKTfzmA-GzBAjM_/1726750850740-12093993-b7e2-461d-b86d-535779bade7b-327381.png)

![1726750887624-d44cb715-c654-41ee-83d5-c80dc79ea3dc.png](./img/eEKTfzmA-GzBAjM_/1726750887624-d44cb715-c654-41ee-83d5-c80dc79ea3dc-986636.png)



![1726750916727-7c6159d2-7041-4655-88b9-73fafe0445ac.png](./img/eEKTfzmA-GzBAjM_/1726750916727-7c6159d2-7041-4655-88b9-73fafe0445ac-207942.png)

![1726750985143-1acaaa72-c39c-4a04-8079-733b0b0e4f97.png](./img/eEKTfzmA-GzBAjM_/1726750985143-1acaaa72-c39c-4a04-8079-733b0b0e4f97-677025.png)

![1726751017764-04cf89aa-dc26-4c52-8e3d-7d971121206a.png](./img/eEKTfzmA-GzBAjM_/1726751017764-04cf89aa-dc26-4c52-8e3d-7d971121206a-037133.png)





![1726751070539-ae38ba3a-df74-46c4-b4d2-97c6235e2a56.png](./img/eEKTfzmA-GzBAjM_/1726751070539-ae38ba3a-df74-46c4-b4d2-97c6235e2a56-345777.png)![1726751148789-18aaa5a0-8056-40cd-8428-4ba839aafe0b.png](./img/eEKTfzmA-GzBAjM_/1726751148789-18aaa5a0-8056-40cd-8428-4ba839aafe0b-961696.png)

![1726751179759-72cee95d-5fc1-42bc-b242-31b5bfa9ff49.png](./img/eEKTfzmA-GzBAjM_/1726751179759-72cee95d-5fc1-42bc-b242-31b5bfa9ff49-286012.png)

![1726751257846-045b2400-24a8-44ef-8d25-4863fea11d03.png](./img/eEKTfzmA-GzBAjM_/1726751257846-045b2400-24a8-44ef-8d25-4863fea11d03-756809.png)

![1726751288214-c88a2303-b2e5-47b6-b50f-ab16f8a8cf87.png](./img/eEKTfzmA-GzBAjM_/1726751288214-c88a2303-b2e5-47b6-b50f-ab16f8a8cf87-057970.png)







> 更新: 2025-04-20 22:39:01  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/ch15inta1brw8y3m>