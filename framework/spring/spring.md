[TOC]

# Spring

## 依赖注入

### Bean容器

#### BeanFactory和ApplicationContext

#### 生命周期

```mermaid
graph TB;
A(实例化)-->B(填充属性)
B-->C(BeanNameAware的setBeanName方法)
C-->D(BeanFactoryAware的setBeanFactory方法)
D-->E(ApplicationContextAware的setApplicationContext方法)
E-->F(BeanPostProcessor预初始化方法)
F-->G(InitializingBean的afterPropertiesSet方法)
G-->H(自定义的初始化方法)
H-->I(BeanPostProcessor初始化后方法)
I-->|Bean可以使用|J(DisposableBean的destroy方法)
J-->K(自定义销毁方法)
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

## 注意事项

> 路线图、第一部分 spring的核心
