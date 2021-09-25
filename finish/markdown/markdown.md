[TOC]

# markdown

## 总览

```mermaid
flowchart TB
  subgraph Markdown
    A[Markdown语法]
    B[写作场景]

    C[基础语法]
    D[GFM语法]
    E[扩展语法]
  end

A-->C
A-->D
A-->E

```

《了不起的Markdown》

- [x] 第1章 人人都应学会Markdown
- [x] 第2章 人人都能学会Markdown
- [x] 第3章 沉浸在写作之中-Typora
- [x] ~~第4章 遨游在“宇宙第一编辑器”-VS Code之中~~
- [x] ~~第5章 轻快、省力地写幻灯片-reveal.js~~
- [x] 第6章 Markdown工具一箩筐
- [x] 第7章 我的地盘我做主
- [x] ~~第8章 自由地写作-GitBook~~
- [x] 附录

## 基础语法

### 标题

### 文字格式

#### 粗体

#### 斜体

### 列表

#### 无序列表

#### 有序列表

### 图片

### 链接

#### 文字链接

#### 引用链接

#### 网址链接

### 引用

### 代码

#### 行内代码

#### 代码块

### 分隔线

### 转义字符

## 扩展语法GFM

### 围栏代码块

### 表格

### 删除线

### 自动链接

### Emoji表情

[参考地址](https://www.webfx.com/tools/emoji-cheat-sheet/)

### 任务列表

### 锚点/书签

## Typora扩展语法

### 下画线

### 数学公式

#### 内联数学公式

#### 数学公式块

### 上标和下标

### 高亮

### 注释

### 目录

### 脚注

### 图表操作

序列图（sequence）

> 基于js-sequence-diagrams开发，使用[js-sequence-diagrams语法](https://bramp.github.io/js-sequence-diagrams/)

流程图（flow）

> 基于flowchat.js开发，使用[flowchat.js语法](https://github.com/adrai/flowchart.js)

Mermaid（mermaid）

> 集成了Mermaid，支持序列图、流程图、甘特图等，使用[Mermaid语法](https://mermaid-js.github.io/mermaid/#/)

### HTML标签

[HTML标签支持](https://support.typora.io/HTML/)

## 写作场景及平台

| 场景             | 工具和平台                      |
| ---------------- | ------------------------------- |
| 笔记             | 印象笔记、有道云笔记            |
| 在线多人协作文档 | 腾讯文档、石墨文档              |
| 博客             | 知乎、简书、CSDN、Hexo[^1]      |
| 微信公众号文章   | Online-Markdown[^2]、Md2All[^3] |
| 邮件             | Markdown Here[^4]               |
| 项目文档         | VuePress[^5]                    |
| 幻灯片           | reveal.js                       |
| 书               | GitBook                         |

[^1]: [Hexo文档](https://hexo.io/zh-cn/docs/)、[Next主题](https://github.com/theme-next/hexo-theme-next)、[Next主题配置](https://theme-next.iissnan.com/getting-started.html)

[^2]: https://www.flyzy2005.cn/tools/online-markdown/

[^3]: http://md.aclickall.com/

[^4]: [Markdown Here流行主题](https://github.com/caseywatts/markdown-here-css)

[^5]: https://vuepress.vuejs.org/zh/guide/