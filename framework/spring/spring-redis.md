[TOC]

# spring-redis

## 总览

```mermaid
flowchart TB
  subgraph spring-redis
    A[redis客户端]
    B[Spring集成]
    C[连接工厂与连接]
    D[模板]
    
    E[序列化]
  end

B-->C
B-->D
D-->E
```

《Spring实战 第4版》

- [x] 第12章 使用NoSQL数据库

## redis客户端

- Jedis
- Lettuce
- Redisson

## spring集成

### 连接工厂与连接

RedisConnectionFactory与RedisConnection

> Spring提供了JedisConnectionFactory和LuttuceConnectionFactory

### 模板

- RedisTemplate
- StringRedisTemplate

#### 序列化器RedisSerializer

RedisTemplat用了JdkSerializationRedisSerializer
StringRedisTemplate使用了StringRedisSerializer
