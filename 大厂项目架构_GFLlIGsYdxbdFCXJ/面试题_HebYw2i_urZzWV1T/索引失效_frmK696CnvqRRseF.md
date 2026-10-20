# 索引失效

```sql
-- 创建示例表

CREATE TABLE employees (

    id INT PRIMARY KEY,

    first_name VARCHAR(50),

    last_name VARCHAR(50),

    age INT,

    salary DECIMAL(10, 2)

);

-- 创建索引

CREATE INDEX idx_last_name ON employees(last_name);

CREATE INDEX idx_age_salary ON employees(age, salary);

-- 插入示例数据

INSERT INTO employees (id, first_name, last_name, age, salary) VALUES

(1, 'John', 'Doe', 28, 50000),

(2, 'Jane', 'Smith', 34, 60000),

(3, 'Mike', 'Brown', 40, 75000),

(4, 'Sara', 'Davis', 30, 52000);
```

## <font style="color:rgb(0, 0, 0);">1. 使用函数进行查询</font>
```sql
-- 使用函数，索引失效
EXPLAIN SELECT * FROM employees WHERE UPPER(last_name) = 'DOE';
```

## <font style="color:rgb(0, 0, 0);">2. 隐式转换</font>
```sql
-- 整数被隐式转换为字符串，索引失效
EXPLAIN SELECT * FROM employees WHERE last_name = 123;
```

## <font style="color:rgb(0, 0, 0);">3. 不等操作</font>
```sql
-- 使用 != 导致索引失效
EXPLAIN SELECT * FROM employees WHERE last_name != 'Smith';
```

## <font style="color:rgb(0, 0, 0);">4. 通配符位置</font>
```sql
-- 通配符在开头，索引失效
EXPLAIN SELECT * FROM employees WHERE last_name LIKE '%mith';
```

## <font style="color:rgb(0, 0, 0);">5. OR 条件</font>
```sql
-- OR 条件，索引失效
EXPLAIN SELECT * FROM employees WHERE last_name = 'Doe' OR age = 28;
```

## <font style="color:rgb(0, 0, 0);">6. 复合索引的最左前缀规则  （走索引）</font>
```sql
-- 复合索引的最左前缀规则未遵循
EXPLAIN SELECT * FROM employees WHERE salary = 50000 AND age = 28;
```

## <font style="color:rgb(0, 0, 0);">7. 范围条件</font>
```sql
-- 范围查询后索引无法用于后面的列
EXPLAIN SELECT * FROM employees WHERE age > 30 AND salary = 52000;
```



假设index(a,b,c)

| where语句 | 索引是否被使用 |
| --- | --- |
| where a =3 | Y， 使用到a |
| where a =3 and  b =5 | Y，使用到a，b |
| where a =3 and  b =5  and  c=4 | Y，使用到a，b，c |
| where b = 3 或者  where b =3 and  c=4  或者  where c=4 | N |
| where a =3  and  c =5  | 使用到a ，但是c不可以，b中间断了 |
| where a=3   and  b > 4 and c=5  | 使用到a和b，c不能用在范围之后，b断了 |
| where a=3   and  b like 'kk%'  and  c=4 | Y，使用到a，b，c |
| where a=3   and  b like '%kk'  and  c=4 | Y，只用到a |
| where a=3   and  b like '%kk%'  and  c=4 | Y，只用到a |
| where a=3   and  b like 'k%kk%'  and  c=4 | Y，使用到a，b，c |


like kk%相当于=常量，%kk和%kk%相当于范围



> 更新: 2025-04-20 22:39:01  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/cqpyxhtpq3yfbobg>