[TOC]

# spring-jdbc

## 总览

```mermaid
flowchart TB
  subgraph spring-jdbc
    A[JDBC]
    B[配置数据源]
    C[JDBC模板]
  end
```

《Spring实战 第4版》

- [x] 第10章 通过Spring和JDBC征服数据库

### 配置数据源

- 连接池数据源（Hikari，Druid）
- JNDI数据源

### JDBC模板

- JdbcTemplate（JdbcOperations）
- NamedParameterJdbcTemplate（NamedParameterJdbcOperations）

### JDBC

```mermaid
graph TB

A[Start]
B[DataSource]
C[Connection]
D[PreparedStatement]
E[Connection/PreparedStatement/ResultSet资源关闭]
F[ResultSet]

A-->B-->|getConnection方法|C-->|prepareStatement方法|D-->|execute方法|E
D-->|executeQuery方法|F-->|查询结果处理|E

```

> 执行图中各类方法会抛出SQLException