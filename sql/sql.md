[TOC]

# SQL

## SELECT语句

## DISTINCT关键字

## 限制结果

MySQL

```sql
-- 以下语句等价
SELECT prod_name FROM products LIMIT 4 OFFSET 3
SELECT prod_name FROM products LIMIT 3,4

-- LIMIT 4 OFFSET 3 第一个数字是检索的行数（第一个被检索的行是第0行），第二个数字是指从哪儿开始

```

## 注释

```sql
-- 行内注释
# 行内注释

/*多行注释*/
```