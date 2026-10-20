# 小米在Flink实时数仓的优化方案

## 背景介绍：
### <font style="color:rgb(25, 25, 25);">Flink简介</font>
<font style="color:rgb(25, 25, 25);">Flink是</font><font style="color:rgb(51, 51, 51);">Apache提供的</font><font style="color:rgb(25, 25, 25);">一个批处理和流处理结合的统一计算框架，其核心是一个提供了数据分发以及并行化计算的流数据处理引擎。它的最大亮点是流处理，是业界最顶级的开源流处理引擎。</font>

<font style="color:rgb(25, 25, 25);">Flink最适合的应用场景是低时延的数据处理（Data Processing）场景：高并发pipeline处理数据，时延毫秒级，且兼具可靠性。</font>

<font style="color:rgb(25, 25, 25);">Flink技术栈如</font>[<font style="color:rgb(25, 25, 25);">图1</font>](https://support.huaweicloud.com/productdesc-mrs/mrs_08_003401.html#mrs_08_003401__fca1fea71ad8a4d748cee96d9d10bc4a6)<font style="color:rgb(25, 25, 25);">所示。</font>

<font style="color:rgb(25, 25, 25);">Flink技术栈  
</font>![1722343706357-cd525970-53e9-4778-847e-6230b8074dc5.png](./img/suhhnYD91Z1YFNj7/1722343706357-cd525970-53e9-4778-847e-6230b8074dc5-123404.png)

<font style="color:rgb(25, 25, 25);">Flink在当前版本中重点构建如下特性：</font>

+ <font style="color:rgb(25, 25, 25);">DataStream</font>
+ <font style="color:rgb(25, 25, 25);">Checkpoint</font>
+ <font style="color:rgb(25, 25, 25);">窗口</font>
+ <font style="color:rgb(25, 25, 25);">Job Pipeline</font>
+ <font style="color:rgb(25, 25, 25);">配置表</font>

### Flink在小米的版本历程：
![1722343656497-15cd16f0-0655-4dc8-8a57-57ed44e21c6d.png](./img/suhhnYD91Z1YFNj7/1722343656497-15cd16f0-0655-4dc8-8a57-57ed44e21c6d-894165.png)



### Flink在小米的现状：
![1722343761778-44356c19-28f3-4985-bf06-8c1eba882256.png](./img/suhhnYD91Z1YFNj7/1722343761778-44356c19-28f3-4985-bf06-8c1eba882256-677815.png)



## Flink在小米的系统架构
![1722343799393-73c5698f-820e-49cd-9705-c49f31c41237.png](./img/suhhnYD91Z1YFNj7/1722343799393-73c5698f-820e-49cd-9705-c49f31c41237-595555.png)



### 服务业务  

![1722343832303-22ded85f-23c2-4892-857c-dc1f763c3d30.png](./img/suhhnYD91Z1YFNj7/1722343832303-22ded85f-23c2-4892-857c-dc1f763c3d30-086489.png)



### 面临问题：
![1722343858439-df9fe3d7-d65f-456c-8a4a-233208754568.png](./img/suhhnYD91Z1YFNj7/1722343858439-df9fe3d7-d65f-456c-8a4a-233208754568-903026.png)

### 解决方案：
### 一：作业资源用量不好确定，影响资源利用率
![1722343912934-01aee781-34d9-46b0-9c06-39c64480db37.png](./img/suhhnYD91Z1YFNj7/1722343912934-01aee781-34d9-46b0-9c06-39c64480db37-363558.png)

如何抉择?

![1722343970152-8e32aa25-6259-4449-b176-f333de6af9c1.png](./img/suhhnYD91Z1YFNj7/1722343970152-8e32aa25-6259-4449-b176-f333de6af9c1-232708.png)

![1722344008061-75e6dd72-4359-4c49-8cdd-589c6bd6d3e2.png](./img/suhhnYD91Z1YFNj7/1722344008061-75e6dd72-4359-4c49-8cdd-589c6bd6d3e2-945673.png)



### 二：存量版本过多，开发和运维压力大
多个版本同存，老用户没有强意愿升级

导致：开发压力大，多版本同时维护；运维压力大，多版本来回切换

解决策略：

![1722344163811-6db4bcac-b026-4498-9d33-ca1a7836b20b.png](./img/suhhnYD91Z1YFNj7/1722344163811-6db4bcac-b026-4498-9d33-ca1a7836b20b-262875.png)

### 三：作业启动速度慢，造成作业重启时间断流
### ![1722344362652-20babc48-a42d-487f-993f-4f65f09dea76.png](./img/suhhnYD91Z1YFNj7/1722344362652-20babc48-a42d-487f-993f-4f65f09dea76-883262.png)
优化措施：

![1722344327526-839c76c6-c446-4d10-a380-1e0ab84b687a.png](./img/suhhnYD91Z1YFNj7/1722344327526-839c76c6-c446-4d10-a380-1e0ab84b687a-629029.png)



### 四：Flink SQL维表Join 相关优化
Flink SQL维表Join 维表类型占比

![1722344483821-01f97c68-c103-4299-a957-0c585efc7aa4.png](./img/suhhnYD91Z1YFNj7/1722344483821-01f97c68-c103-4299-a957-0c585efc7aa4-016361.png)

表大小及速度对比：

![1722344517329-9bc29dea-4c2a-40e3-81d3-8d80eb5db050.png](./img/suhhnYD91Z1YFNj7/1722344517329-9bc29dea-4c2a-40e3-81d3-8d80eb5db050-353298.png)

优化策略：

![1722344545745-6bdd0b92-a9af-4c54-83b7-4d28283ca046.png](./img/suhhnYD91Z1YFNj7/1722344545745-6bdd0b92-a9af-4c54-83b7-4d28283ca046-301220.png)

![1722344583687-2692e14d-ad36-45ed-b5ef-0144fd0d0643.png](./img/suhhnYD91Z1YFNj7/1722344583687-2692e14d-ad36-45ed-b5ef-0144fd0d0643-529039.png)

![1722344604970-c1e591db-8d78-4542-8b76-969042fd2dc2.png](./img/suhhnYD91Z1YFNj7/1722344604970-c1e591db-8d78-4542-8b76-969042fd2dc2-150647.png)

![1722344626781-cc163a8a-147c-4024-9897-f63a3ac0fb5b.png](./img/suhhnYD91Z1YFNj7/1722344626781-cc163a8a-147c-4024-9897-f63a3ac0fb5b-715141.png)

![1723038660151-e3c0b7ee-e791-4b02-aeea-cfb40e57324b.png](./img/suhhnYD91Z1YFNj7/1723038660151-e3c0b7ee-e791-4b02-aeea-cfb40e57324b-378440.png)

![1722344660704-d9d2f8de-3e39-4705-8f66-2b28aec8f8e3.png](./img/suhhnYD91Z1YFNj7/1722344660704-d9d2f8de-3e39-4705-8f66-2b28aec8f8e3-481867.png)



## 最佳实践：
![1722344783402-97036d13-5db3-49b0-93cf-ff684cf964bd.png](./img/suhhnYD91Z1YFNj7/1722344783402-97036d13-5db3-49b0-93cf-ff684cf964bd-955964.png)

![1722344804958-d8bbbebb-82f1-451b-b157-1efc1648c897.png](./img/suhhnYD91Z1YFNj7/1722344804958-d8bbbebb-82f1-451b-b157-1efc1648c897-921200.png)

![1722344840541-fc771255-6817-4609-95f1-a6e73a10fb6f.png](./img/suhhnYD91Z1YFNj7/1722344840541-fc771255-6817-4609-95f1-a6e73a10fb6f-172208.png)



## 规划与展望：
![1722344903493-95a057b8-89e0-462f-a4b1-2c033f0b6216.png](./img/suhhnYD91Z1YFNj7/1722344903493-95a057b8-89e0-462f-a4b1-2c033f0b6216-976957.png)



## 总结：
![1722344927958-c265f7d3-71f3-412c-ad82-e226cdc3be79.png](./img/suhhnYD91Z1YFNj7/1722344927958-c265f7d3-71f3-412c-ad82-e226cdc3be79-161837.png)





















> 更新: 2024-08-07 21:51:02  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/qei98h4r8ar0i9on>