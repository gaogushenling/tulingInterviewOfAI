# 10大MySQL高可用方案对比

## 自动故障转移高可用方案
### MMM方案（Multi Master Replication Manager）
![1719405747821-3ab8ba71-b6fe-4386-b929-ed4160cbadfc.png](./img/bxbN11a2QgbndAJl/1719405747821-3ab8ba71-b6fe-4386-b929-ed4160cbadfc-891988.png)

![1719405790415-cce72004-2171-49ad-993c-ea8a87d7c0eb.png](./img/bxbN11a2QgbndAJl/1719405790415-cce72004-2171-49ad-993c-ea8a87d7c0eb-345937.png)

### ProxySQL 方案
![1719407333857-ee859eee-efbb-42b5-ab55-61cc53da31f0.png](./img/bxbN11a2QgbndAJl/1719407333857-ee859eee-efbb-42b5-ab55-61cc53da31f0-698920.png)

<font style="color:rgb(51, 51, 51);">优点：</font>

1. **<font style="color:rgb(51, 51, 51);">高性能</font>**<font style="color:rgb(51, 51, 51);">：ProxySQL设计得非常快，能够处理大量的连接。</font>
2. **<font style="color:rgb(51, 51, 51);">可伸缩性</font>**<font style="color:rgb(51, 51, 51);">：ProxySQL可以通过简单的配置来处理大量的数据库后端。</font>
3. **<font style="color:rgb(51, 51, 51);">灵活性</font>**<font style="color:rgb(51, 51, 51);">：ProxySQL提供了多种路由查询到后端数据库的方法，包括简单的轮询、最少连接、读写分离等。</font>
4. **<font style="color:rgb(51, 51, 51);">监控</font>**<font style="color:rgb(51, 51, 51);">：ProxySQL内置了监控系统，可以监控后端服务器的健康状况和性能指标。</font>
5. **<font style="color:rgb(51, 51, 51);">配置灵活</font>**<font style="color:rgb(51, 51, 51);">：ProxySQL配置可以通过管理接口实时更改，不需要停机。</font>
6. **<font style="color:rgb(51, 51, 51);">兼容性</font>**<font style="color:rgb(51, 51, 51);">：ProxySQL兼容MySQL协议，因此客户端可以像连接到MySQL服务器一样连接到ProxySQL。</font>
7. **<font style="color:rgb(51, 51, 51);">安全性</font>**<font style="color:rgb(51, 51, 51);">：ProxySQL支持用户名和密码认证，并且可以设置防火墙规则来限制访问。</font>

<font style="color:rgb(51, 51, 51);"></font>

<font style="color:rgb(51, 51, 51);">缺点：</font>

1. <font style="color:rgb(51, 51, 51);">配置复杂：ProxySQL配置相对复杂，需要管理员具有较深的MySQL和ProxySQL知识。</font>
2. <font style="color:rgb(51, 51, 51);">学习曲线：ProxySQL的学习曲线较为陡峭，需要时间去熟悉所有的配置选项和管理命令。</font>
3. <font style="color:rgb(51, 51, 51);">性能损耗：虽然ProxySQL提供了很多额外的功能，但在某些情况下，可能会导致性能略微下降。</font>
4. <font style="color:rgb(51, 51, 51);">维护成本：ProxySQL的维护需要专业知识，如果不正确管理，可能会导致系统故障。</font>
5. <font style="color:rgb(51, 51, 51);">兼容性问题：ProxySQL与某些MySQL特性不兼容，比如某些存储过程或触发器。</font>
6. <font style="color:rgb(51, 51, 51);">文档：ProxySQL的官方文档较为稀缺，社区支持不如某些开源项目丰富。</font>



### MHA方案
![1719405938408-3702becd-a728-49bd-9d4f-8a3830a9750a.png](./img/bxbN11a2QgbndAJl/1719405938408-3702becd-a728-49bd-9d4f-8a3830a9750a-070722.png)

![1719406013404-e68cbc98-f258-402a-a41f-2ef183385e69.png](./img/bxbN11a2QgbndAJl/1719406013404-e68cbc98-f258-402a-a41f-2ef183385e69-255798.png)

![1719406056285-128c9a2f-c5da-41be-8b94-88919cb966f4.png](./img/bxbN11a2QgbndAJl/1719406056285-128c9a2f-c5da-41be-8b94-88919cb966f4-133774.png)

### MGR(MySQL Group Replication)方案
![1719406167629-98d6f29a-7457-41ba-ae9a-67eb8b5457e6.png](./img/bxbN11a2QgbndAJl/1719406167629-98d6f29a-7457-41ba-ae9a-67eb8b5457e6-393698.png)

![1719406198540-d2c37f65-882d-4182-a91b-99c3c6839128.png](./img/bxbN11a2QgbndAJl/1719406198540-d2c37f65-882d-4182-a91b-99c3c6839128-029463.png)

![1719406263005-95e09346-03c4-4285-a3f0-861b1b68fccd.png](./img/bxbN11a2QgbndAJl/1719406263005-95e09346-03c4-4285-a3f0-861b1b68fccd-341875.png)



### MIC（MySQL InnoDB Cluster）
![1719406476899-930a69fc-5b59-4724-b8e6-48e89079e8ce.png](./img/bxbN11a2QgbndAJl/1719406476899-930a69fc-5b59-4724-b8e6-48e89079e8ce-675016.png)

![1719406525615-fc130b17-c095-4b56-853f-db2448acf3af.png](./img/bxbN11a2QgbndAJl/1719406525615-fc130b17-c095-4b56-853f-db2448acf3af-893598.png)



### Galera Cluster 多主
![1719406572947-ec9b2de7-b618-4246-9c97-3381beb82a8a.png](./img/bxbN11a2QgbndAJl/1719406572947-ec9b2de7-b618-4246-9c97-3381beb82a8a-889689.png)



![1719406653666-31f10c1d-869b-4b03-8aed-ab279bd378b4.png](./img/bxbN11a2QgbndAJl/1719406653666-31f10c1d-869b-4b03-8aed-ab279bd378b4-148700.png)

![1719406682193-787d9975-8498-4425-8200-33f45f5a27f5.png](./img/bxbN11a2QgbndAJl/1719406682193-787d9975-8498-4425-8200-33f45f5a27f5-039528.png)



### PXC（Percona XtraDB Cluster）多主
![1719406740816-b99e3a71-7248-444c-acf7-0fdc91d83649.png](./img/bxbN11a2QgbndAJl/1719406740816-b99e3a71-7248-444c-acf7-0fdc91d83649-131215.png)

![1719406766277-700ce00e-4bfa-4d70-868a-2c51c8a4532e.png](./img/bxbN11a2QgbndAJl/1719406766277-700ce00e-4bfa-4d70-868a-2c51c8a4532e-015120.png)

![1719406779710-466dba21-3ed4-47bc-9f0d-98ddbaac5f76.png](./img/bxbN11a2QgbndAJl/1719406779710-466dba21-3ed4-47bc-9f0d-98ddbaac5f76-261278.png)



## 数据可靠性方案
### RAID10原始方案
![1719406854242-1c672305-c82e-4753-882c-343731aed84e.png](./img/bxbN11a2QgbndAJl/1719406854242-1c672305-c82e-4753-882c-343731aed84e-018797.png)

### SAN共享存储
![1719406944961-a25b8653-6ee1-484e-9f6e-2d5f7cb20231.png](./img/bxbN11a2QgbndAJl/1719406944961-a25b8653-6ee1-484e-9f6e-2d5f7cb20231-657042.png)

### ![1719406969018-5110b5e7-3c99-40f3-8649-ae812c28d8e6.png](./img/bxbN11a2QgbndAJl/1719406969018-5110b5e7-3c99-40f3-8649-ae812c28d8e6-001720.png)DRBD磁盘复制
![1719407094079-b77edefe-e804-4861-a1fa-d86e95d50ad9.png](./img/bxbN11a2QgbndAJl/1719407094079-b77edefe-e804-4861-a1fa-d86e95d50ad9-035122.png)

当主机出现问题，远程主机上还保留着一份相同的数据，可以继续使用，确保数据安全性。



> 更新: 2024-06-26 21:12:53  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/ntru4adh4oztkwgz>