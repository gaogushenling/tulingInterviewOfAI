# 高并发微服务架构为何都在放弃 Zookeeper

## 背景：
目前主流的微服务与高并发的程序都在放弃zk

比如，Kafka，Facebook，RocketMq等都在转研自己的配置管理中心。

![1720365578090-7221ba13-404d-473a-b704-efd62174bd5b.png](./img/Sc-L3fO0GcaAuQ9h/1720365578090-7221ba13-404d-473a-b704-efd62174bd5b-108175.png)

要明白为什么？首先我们来看看

### ZK是做什么的
很多人对zk的基本认识就是一个分布式协调中间件。主要做为注册中心，配置中心。

注册中心：

![1720365639912-d2791947-b9e4-45b8-b581-1370464fa6b4.png](./img/Sc-L3fO0GcaAuQ9h/1720365639912-d2791947-b9e4-45b8-b581-1370464fa6b4-146374.png)



配置中心：

![1720365683447-06ac8043-0b2f-4266-a8de-3ef61eb1b599.png](./img/Sc-L3fO0GcaAuQ9h/1720365683447-06ac8043-0b2f-4266-a8de-3ef61eb1b599-350606.png)

### 那为啥不受待见了呢？
架构图如下：

![1720365716327-7dc59a02-1fb1-4530-9db8-95430ce0c02f.png](./img/Sc-L3fO0GcaAuQ9h/1720365716327-7dc59a02-1fb1-4530-9db8-95430ce0c02f-819790.png)

![1720365754254-611f34fc-c3b7-4ec1-ac4a-db5947334da8.png](./img/Sc-L3fO0GcaAuQ9h/1720365754254-611f34fc-c3b7-4ec1-ac4a-db5947334da8-110154.png)

![1720365838297-415ffbde-430f-4b61-a255-22f75591474d.png](./img/Sc-L3fO0GcaAuQ9h/1720365838297-415ffbde-430f-4b61-a255-22f75591474d-701416.png)

![1720365867646-d3eacbfd-2771-4fa0-8d40-4b80acac4a10.png](./img/Sc-L3fO0GcaAuQ9h/1720365867646-d3eacbfd-2771-4fa0-8d40-4b80acac4a10-166794.png)

![1720365888816-076dad61-b610-4a88-94be-f1415667adc0.png](./img/Sc-L3fO0GcaAuQ9h/1720365888816-076dad61-b610-4a88-94be-f1415667adc0-718705.png)





> 更新: 2024-07-07 23:25:36  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/ggtxz1u0gq08nf6c>