[TOC]

# spring-redis

## 总览

```mermaid
flowchart TB
  subgraph spring-redis
    A[redis客户端]
    B[连接工厂与连接]
    C[模板]
    
    D[序列化]
  end

C-->D
```

《Spring实战 第4版》

- [x] 第12章 使用NoSQL数据库

## redis客户端

- Jedis
- Lettuce
- Redisson

## 连接工厂与连接

RedisConnectionFactory与RedisConnection

> Spring提供了JedisConnectionFactory和LuttuceConnectionFactory

## 模板

- RedisTemplate
- StringRedisTemplate

### 序列化器RedisSerializer

RedisTemplat用了JdkSerializationRedisSerializer
StringRedisTemplate使用了StringRedisSerializer
