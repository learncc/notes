[TOC]

# Spring

## MVC

### 请求流程图

```mermaid
graph LR

A>请求]
B[DispatcherServlet]
C[处理器映射]
D[控制器]
E[视图解析器]
F[视图]
G>响应]

A-->|1|B-->|2|C
B-->|3|D
B-->|5|E
B-->|6|F
D-->|4模型及逻辑视图名|B
F-->G

```

### 控制器

1. 类级别：@Controller+@RequestMapping
2. 方法级别：@RequestMapping

#### 请求输入

均在方法参数级别上

1. 查询参数（@RequestParam）
2. 表单参数
3. 路径参数（@PathVariable）

##### 表单参数校验

1. @Valid（控制器方法参数）
2. 校验注解（模型属性）

#### 文件上传

@RequestPart+MultipartFile/Part

#### 异常处理

1. 异常类添加@ResponseStatus

2. @ExceptionHandler注解方法

> 注意：@ExceptionHandler能处理同个控制器中所有处理器方法抛出的异常，如果需要能够处理所有控制器中处理器方法抛出的异常，需要使用控制器通知（带有@ControllerAdvice注解的类）



## spring-redis

### redis客户端

- Jedis
- Lettuce
- Redisson

### 连接工厂与连接

RedisConnectionFactory与RedisConnection

> Spring提供了JedisConnectionFactory和LuttuceConnectionFactory

### 模板

- RedisTemplate
- StringRedisTemplate

#### 序列化器RedisSerializer

RedisTemplat用了JdkSerializationRedisSerializer
StringRedisTemplate使用了StringRedisSerializer

## 注意事项

> 路线图、第2部分、Servlet-Filter-Listener
