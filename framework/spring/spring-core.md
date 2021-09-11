[TOC]

# spring-core

## 总览

```mermaid
flowchart TB
  subgraph spring-core
    A[依赖注入]
    B[面向切面编程AOP]

    C[Bean容器]
    D[Bean生命周期]
    E[装配]
  end

A-->C
A-->D
A-->E
```

《Spring实战 第4版》

- [x] 第1章 Spring之旅
- [x] 第2章 装配Bean
- [x] 第3章 高级装配
- [x] 第4章 面向切面的Spring

## 依赖注入

### Bean容器

BeanFactory和ApplicationContext

### Bean生命周期

```mermaid
graph TB

A(实例化)
B(填充属性)
C(BeanNameAware的setBeanName方法)
D(BeanFactoryAware的setBeanFactory方法)
E(ApplicationContextAware的setApplicationContext方法)
F(BeanPostProcessor预初始化方法)
G(InitializingBean的afterPropertiesSet方法)
H(自定义的初始化方法)
I(BeanPostProcessor初始化后方法)
J(DisposableBean的destroy方法)
K(自定义销毁方法)

A-->B-->C-->D-->E-->F-->G-->H-->I-->|Bean可以使用|J-->K

```

### 装配

1. 隐式装配

> 组件扫描（@ComponentScan+@Component）+自动装配（@Autowired）

2. 显式装配

> @Configuration+@Bean

#### 导入配置

@Import

### 高级装配

#### 环境

@Profile+属性（spring.profiles.active和spring.profiles.default）

> 基于@Conditional实现

#### 自动装配歧义性问题

1. @Primary
2. @Qualifier

#### bean作用域

@Scope

1. 单例
2. 原型
3. 会话
4. 请求

> 使用会话或请求作用域时需要指明proxyMode以解决注入单例bean中所遇到的问题

#### 运行时值注入

@PropertySource声明属性源

1. Environment
2. @Value
3. SpEL

## 面向切面编程AOP

### 切面

@Aspect

### 切点

@Pointcut

### 通知

1. @Before、@After、@AfterReturning、@AfterThrowing
2. @Around(ProceedingJoinPoint)
