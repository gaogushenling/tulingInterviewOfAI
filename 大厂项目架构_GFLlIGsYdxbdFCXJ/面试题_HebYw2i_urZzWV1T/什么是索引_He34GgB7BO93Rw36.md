# 什么是索引

* 索引是高效获取数据的**排好序**的**数据结构**，<font style="color:rgb(0, 0, 0);">通过在某些列上创建索引，数据库可以更高效地查找、检索和排序数据；</font>
* <font style="color:rgb(0, 0, 0);">提高查询速度：索引用于快速查找特定行，特别是在大型数据表中，索引可以大大减少扫描的行数，从而加快查询速度。</font>
* <font style="color:rgb(0, 0, 0);">排序和分组：通过索引，数据库可以更快地进行 ORDER BY 和 GROUP BY 操作。</font>

## <font style="color:rgb(0, 0, 0);">1. 创建用户表</font>

```sql
CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(50) NOT NULL,
  email VARCHAR(100) NOT NULL,
  age INT
);


INSERT INTO users (username, email, age) VALUES
('user1', 'user1@example.com', 25),
('user2', 'user2@example.com', 26),
('user3', 'user3@example.com', 27),
('user4', 'user4@example.com', 28),
('user5', 'user5@example.com', 29),
('user6', 'user6@example.com', 30),
('user7', 'user7@example.com', 31),
('user8', 'user8@example.com', 32),
('user9', 'user9@example.com', 33),
('user10', 'user10@example.com', 34),
('user11', 'user11@example.com', 35),
('user12', 'user12@example.com', 36),
('user13', 'user13@example.com', 37),
('user14', 'user14@example.com', 38),
('user15', 'user15@example.com', 39),
('user16', 'user16@example.com', 40),
('user17', 'user17@example.com', 41),
('user18', 'user18@example.com', 42),
('user19', 'user19@example.com', 43),
('user20', 'user20@example.com', 44),
('user21', 'user21@example.com', 25),
('user22', 'user22@example.com', 26),
('user23', 'user23@example.com', 27),
('user24', 'user24@example.com', 28),
('user25', 'user25@example.com', 29),
('user26', 'user26@example.com', 30),
('user27', 'user27@example.com', 31),
('user28', 'user28@example.com', 32),
('user29', 'user29@example.com', 33),
('user30', 'user30@example.com', 34),
('user31', 'user31@example.com', 35),
('user32', 'user32@example.com', 36),
('user33', 'user33@example.com', 37),
('user34', 'user34@example.com', 38),
('user35', 'user35@example.com', 39),
('user36', 'user36@example.com', 40),
('user37', 'user37@example.com', 41),
('user38', 'user38@example.com', 42),
('user39', 'user39@example.com', 43),
('user40', 'user40@example.com', 44);
```

## <font style="color:rgb(0, 0, 0);">2. 添加索引</font>

<font style="color:rgb(0, 0, 0);">假设我们希望在 email 字段上添加一个索引，以提高查询速度。</font>

```sql
CREATE INDEX idx_email ON users(email);
```

## <font style="color:rgb(0, 0, 0);">3. 查看索引</font>

```sql
SHOW INDEX FROM users;
```

## <font style="color:rgb(0, 0, 0);">4. 修改索引</font>

<font style="color:rgb(0, 0, 0);"> </font><font style="color:rgb(0, 0, 0);">假设你想修改索引，比如改变索引名称或者添加一个复合索引，可以先删除现有的索引，再创建新的索引。例如，删除 </font><code><font style="color:rgb(0, 0, 0);">email</font></code><font style="color:rgb(0, 0, 0);"> 上的索引并添加一个 </font><code><font style="color:rgb(0, 0, 0);">email + age</font></code><font style="color:rgb(0, 0, 0);"> 复合索引。</font><font style="color:rgb(0, 0, 0);">  </font>

```sql
-- 删除原有索引

DROP INDEX idx_email ON users;

-- 创建新的复合索引

CREATE INDEX idx_email_age ON users(email, age);
```

## <font style="color:rgb(0, 0, 0);">5. 删除索引</font>

```sql
DROP INDEX idx_email_age ON users;
```


> 更新: 2025-04-20 22:39:01  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/zs2yd5a0vsh1fc03>