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

### 导入配置

@Import

## 注意事项

> 路线图、第一部分 spring的核心
