# 我为什么不建议使用Docker部署MySQL数据库？



从应用场景下，数据存储节点是少量而稳定的，大多数场景并没有“灵活扩容的需求”

![1729923560300-1c1dbd1e-79ce-4285-abb8-24a7348ac07a.png](./img/MfnYaiHGOVjRiN0s/1729923560300-1c1dbd1e-79ce-4285-abb8-24a7348ac07a-285269.png)















从技术方面，Mysql容器是“有状态的”无法轻易的水平扩容

![1729925692334-14608c97-fa9b-45a6-adb4-25700c0f3de1.png](./img/MfnYaiHGOVjRiN0s/1729925692334-14608c97-fa9b-45a6-adb4-25700c0f3de1-393025.png)













扩容容器，共享数据文件

![1729926100606-1f91ddb7-8e71-4391-b1db-7c944a497e84.png](./img/MfnYaiHGOVjRiN0s/1729926100606-1f91ddb7-8e71-4391-b1db-7c944a497e84-235419.png)









每个容器都挂载各自的SSD

![1729926529580-37ae210a-3178-43af-9468-b083eea94fed.png](./img/MfnYaiHGOVjRiN0s/1729926529580-37ae210a-3178-43af-9468-b083eea94fed-896651.png)















![1729930657194-8b758ac2-f711-48c3-9348-d6ab2dd0ccc7.png](./img/MfnYaiHGOVjRiN0s/1729930657194-8b758ac2-f711-48c3-9348-d6ab2dd0ccc7-934421.png)























资源上占用

![1729928571107-8601473f-2e29-46b9-89cc-f88d0e55afaf.png](./img/MfnYaiHGOVjRiN0s/1729928571107-8601473f-2e29-46b9-89cc-f88d0e55afaf-892513.png)



> 更新: 2025-04-20 22:38:59  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/wcmxppyaztm7mb8l>