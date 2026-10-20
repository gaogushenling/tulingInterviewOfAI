# MySQL关键特性索引下推ICP

## 前置知识：

整体架构

![1727094728653-6720c79e-3a80-4853-ad29-ad10be8ef528.png](./img/JMVEnM0WSvtyegQa/1727094728653-6720c79e-3a80-4853-ad29-ad10be8ef528-449438.png)

## <font style="background:#F8CED3;color:#70000D">MySQL</font> <font style="background:#DBF1B7;color:#2A4200">索引下推</font>

<font style="color:rgb(51, 51, 51);">索引下推(Index Condition Pushdown) ICP 是Mysql5.6之后新增的功能，主要的核心点就在于把数据筛选的过程放在了存储引擎层去处理，而不是像之前一样放到Server层去做过滤。</font>

### 什么是索引下推

<font style="color:rgb(51, 51, 51);">首先创建一张</font><font style="color:rgb(255, 100, 65);">user</font><font style="color:rgb(51, 51, 51);">表，同时建立</font><font style="color:rgb(255, 100, 65);">age_name</font><font style="color:rgb(51, 51, 51);">的联合索引，同时插入3条测试数据。</font>

![1630309506999-1fde32be-50c7-4ecc-a192-a566df1dab32.jpeg](./img/JMVEnM0WSvtyegQa/1630309506999-1fde32be-50c7-4ecc-a192-a566df1dab32-312926.jpeg)

<font style="color:rgb(51, 51, 51);">然后，执行查询</font><code><font style="color:rgb(255, 100, 65);">explain SELECT * from user where age >10 and name = 'a'</font></code><font style="color:rgb(51, 51, 51);">，如下图所示，就会看见</font><font style="color:rgb(255, 100, 65);">Extra</font><font style="color:rgb(51, 51, 51);">中显示了</font><font style="color:rgb(255, 100, 65);">Using index condition</font><font style="color:rgb(51, 51, 51);">，这表示出现了</font>**<font style="color:black;">索引下推</font>**<font style="color:rgb(51, 51, 51);">了。</font>

![1630309386682-2be33f96-c623-4afe-8f11-fbe5d8447ebc.webp](./img/JMVEnM0WSvtyegQa/1630309386682-2be33f96-c623-4afe-8f11-fbe5d8447ebc-826631.webp)

<font style="color:rgb(51, 51, 51);">没错，针对这个查询场景就是索引下推，那到底什么是索引下推呢？</font>

<font style="color:rgb(51, 51, 51);">按照上述的场景，实际上就存在两个索引树，一个是主键索引(</font>*<font style="color:rgb(247, 49, 49);">Clustered Index</font>*<font style="color:rgb(51, 51, 51);">)，存储了具体的数据的信息，另外则是</font><font style="color:rgb(255, 100, 65);">age_name</font><font style="color:rgb(51, 51, 51);">的联合索引(</font><font style="color:#DF2A3F;">secondary index</font><font style="color:rgb(51, 51, 51);">)，保存了主键的ID。</font>

![1630309386822-cfc6a770-42a0-440b-acf2-a915e8a31b77.webp](./img/JMVEnM0WSvtyegQa/1630309386822-cfc6a770-42a0-440b-acf2-a915e8a31b77-422282.webp)

<font style="color:rgb(51, 51, 51);">在没有ICP索引下推的时候，这个查询的流程应该是这样（略过无关的细节）：</font>

1. <font style="color:rgb(51, 51, 51);">Mysql Server层调用API查询存储引擎数据</font>
2. <font style="color:rgb(51, 51, 51);">存储引擎根据联合索引首先通过条件找到所有age>10的数据</font>
3. <font style="color:rgb(51, 51, 51);">找到的每一条数据都根据主键索引进行回表查询，直到找到不符合条件的结果</font>
4. <font style="color:rgb(51, 51, 51);">返回数据给Server层，Server根据条件对结果进行过滤，流程结束</font>

<font style="color:rgb(51, 51, 51);">而有了ICP之后的流程则是这样：</font>

1. <font style="color:rgb(51, 51, 51);">Mysql Server层调用API查询存储引擎数据</font>
2. <font style="color:rgb(51, 51, 51);">存储引擎根据联合索引首先通过条件找到所有age>10的数据，根据联合索引中已经存在的</font><font style="color:rgb(255, 100, 65);">name</font><font style="color:rgb(51, 51, 51);">数据进行过滤，找到符合条件的数据</font>
3. <font style="color:rgb(51, 51, 51);">根据找到符合条件的数据，回表查询</font>
4. <font style="color:rgb(51, 51, 51);">返回数据给Server层，流程结束</font>

<font style="color:rgb(51, 51, 51);">对比这两个流程就会很明显的发现，使用ICP之后就是简单的通过联合索引中本来就有的数据直接过滤了，不需要再查到一堆无用的数据去Server层进行过滤，这样的话减少了回表的次数和返回的数据，IO次数减少了，对性能有很好的提升。</font>

<font style="color:rgb(51, 51, 51);">按照官方文档所说，ICP其实也存在一定的使用限制场景，只说关键的，乱七八糟的不说。</font>

1. <font style="color:rgb(51, 51, 51);">首先，ICP适用于range、ref、eq_ref和ref_or_null的场景下</font>
2. <font style="color:rgb(51, 51, 51);">InnoDB和MyISAM都支持ICP，Mysql partition分表的话也可以使用</font>
3. <font style="color:rgb(51, 51, 51);">对于InndoDB而言，ICP只支持二级索引，因为主键索引它用不上不是吗？</font>
4. <font style="color:rgb(51, 51, 51);">子查询不支持</font>

<font style="color:rgb(51, 51, 51);">现在基本都使用的5.6以上的版本了，默认就是开启ICP的，想关闭的话可以通过命令</font><code><font style="color:rgb(255, 100, 65);">SET optimizer_switch = 'index_condition_pushdown=off';</font></code><font style="color:rgb(51, 51, 51);">。</font>

# 二、索引下推案例

用户表user，联合索引为（name, age）

| id | name | age |
| --- | --- | --- |
| 1 | 张三 | 10 |
| 2 | 李四 | 12 |
| 3 | 王五 | 12 |
| 4 | 张猛 | 16 |

语句\
根据最左匹配原则，只能用到索引 '张'

![1653230844204-da7e3b44-c731-4f5c-a946-751a9325bffc.png](./img/JMVEnM0WSvtyegQa/1653230844204-da7e3b44-c731-4f5c-a946-751a9325bffc-930486.webp)

**未使用索引下推**\
先根据二级索引得到张三和张猛的两条记录\
根据id回表查询（id=1 id = 4）\
讲记录返回server层，判断age条件

![1653231771962-6bb67852-e903-42ce-86ee-69262f126a37.png](./img/JMVEnM0WSvtyegQa/1653231771962-6bb67852-e903-42ce-86ee-69262f126a37-908386.webp)

**使用索引下推**\
先根据二级索引得到张三和张猛的两条记录\
由于是name跟age的联合索引，所以可直接根据age条件判断，得到id=1的记录\
回表查询id=1的记录返回server层

![1653232012686-d4c365d7-27fd-42e6-9d5d-8a952f50e0b7.png](./img/JMVEnM0WSvtyegQa/1653232012686-d4c365d7-27fd-42e6-9d5d-8a952f50e0b7-657136.webp)

# 索引下推与覆盖索引的区别

索引下推是将在Server层的数据筛选，推到了存储引擎，让存储引擎去做这样的操作。

覆盖索引则是将要查找的数据放在一起，变成组合索引，进行查找时不需要回表操作

例如：

select name,age from user where name="张三"；

这里name与age建立组合索引，当找到张三时就能从索引树上得到name,age返回给Server层，这就是覆盖索引，即组合索引包含着我们的查询的字段。

同样

select name,age ,sex from user where name="张三"  and age=12;

组合索引当中是根据name来排序的，age是无序的。所以在不使用ICP时，组合索引树只会判断name，从而回表查找整个行数据，交给Server层

使用ICP时，会判断name和age，再去回表查找整个行数据，交给Server层，减少了回表次数。


> 更新: 2025-04-20 22:39:01  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/as6tg55xes098npo>