[TOC]

# SQL

## SELECT语句

```sql
SELECT column FROM table_name
```

### DISTINCT关键字

### 计算字段

#### 连接字段

MySQL使用`CONCAT()`完成

#### 算术运算

+-*/

### 别名AS

### 函数

CONVERT数据类型转换
CURDATE获取当前日期

#### 文本处理函数

UPPER/LOWER
LEFT/RIGHT/SUBSTRING
LENGTH
TRIM/LTRIM/RTRIM

#### 日期和时间处理函数

YEAR/MONTH

#### 数值处理函数

#### 格式化函数

#### 系统函数

### 限制结果

MySQL

```sql
-- 以下语句等价
SELECT prod_name FROM products LIMIT 4 OFFSET 3
SELECT prod_name FROM products LIMIT 3,4

-- LIMIT 4 OFFSET 3 第一个数字是检索的行数（第一个被检索的行是第0行），第二个数字是指从哪儿开始

```

### ORDER BY排序

> 多列排序的排列方向需分别指定（DESC降序，默认升序ASC）

### WHERE过滤

#### 操作符

- =
- !=或\<\>
- \<、\<=、\>、\>=
- BETWEEN
- IS NULL

> NULL值非匹配问题

#### AND子句

#### OR子句

#### IN操作符

可以包含其他SELECT子句

#### NOT操作符

#### LIKE与通配符

1. %（匹配0、1或多个字符）
2. \_（匹配单个字符）

## 注释

```sql
-- 行内注释
# 行内注释

/*多行注释*/
```
