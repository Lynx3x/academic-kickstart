---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Lary自用型Markdown攻略"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2020-01-29T21:52:15+08:00
lastmod: 2020-01-29T21:52:15+08:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---


# Lary自用型Markdown攻略

## 概览

编辑器：VsCode、Typora（VsCode插件渲染得有点慢，还是Typora好）  
个人分类原则：三级分类  
内容参照：Typora中的Markdown Reference

<!-- TOC -->

- [Lary自用型Markdown攻略](#lary自用型markdown攻略)
    - [概览](#概览)
    - [Block元素](#block元素)
        - [段落和换行](#段落和换行)
        - [标题](#标题)
        - [块引用](#块引用)
        - [列表](#列表)
        - [TODO](#todo)
        - [代码块](#代码块)
        - [数学公式块](#数学公式块)
        - [表](#表)
        - [水平分割线](#水平分割线)
    - [Span元素](#span元素)
        - [链接](#链接)
        - [URL](#url)
        - [图片](#图片)
        - [斜体](#斜体)
        - [加粗](#加粗)
        - [编程](#编程)
        - [删除线](#删除线)
        - [下划线](#下划线)
        - [行内数学公式](#行内数学公式)
    - [HTML](#html)
        - [嵌入内容](#嵌入内容)
        - [视频](#视频)

<!-- /TOC -->

## Block元素

### 段落和换行

<!-- 此为错误的分隔段落方式，两个段落间没有用空白行分隔。 -->
段落被两个或多个空白行分隔。
单独换行一般会被解释器忽略。
<!--  此为正确的分隔段落方式 -->

在一行的末尾留下两个空格后再换行便能实现单独换行的效果。  
单独换行测试。

### 标题

在行首使用#号，一个#号为一级标题，六个#号为六级标题。

### 块引用

> 在行首使用>符号实现引用效果
>
> 引用中换行测试
>
> > 嵌套块引用测试

> 另起一段引用测试

### 列表

使用\*号创建无序列表——*符号可用+或者-替代。

* item1
* item2
* item3

使用数字加点创建有序列表。

1. item1
2. item2
3. item3

### TODO

使用[ ]或者[x]实现TODO列表。

- [ ] 待办事项1
- [x] 待办事项2
- [ ] 待办事项3

使用ALT + C 可以快速勾选TODO框（VsCode-MarkdownAllinOne插件）

### 代码块

使用```实现代码块高亮功能。

```markdown
* item1
* item2
* item3
```

### 数学公式块

个人不常用，仅附范例。
$$
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\
\end{vmatrix}
$$
[更多内容参考](http://support.typora.io/Math/)  
[手写识别LaTeX符号](http://detexify.kirelabs.org/classify.html)

### 表

表范例如下。  
冒号在最左边表示左对齐，最右则右对齐，两边则表示居中。  
ALT + SHIFT + F 可以自动格式化表。（VsCode-MarkdownAllinOne插件）

左 | 中 | 右
:--|:-:|--:
居中测试文本|居中测试文本|居中测试文本
TEST|TEST|TEST

### 水平分割线

在空白行输入***或者---创建一条水平分割线

---
测试
***

## Span元素

Span元素将在输入后被立刻解析和显示。

### 链接

Markdown支持两种链接的写法：行内链接和参考链接。  

行内链接：  
[链接](https://example.com/)  
[内部链接](#Span元素)

参考链接：  
[参考链接][Cankao]

[Cankao]:https://example.com/ "备注文本"

<!-- 个人觉得这种写法在源代码上来说更为美观-->
[参考链接2][]

[参考链接2]:https://example.com/

### URL

使用<>包括URL，或者直接写标准URL。

<https://example.com/>  
https://example.com/

### 图片

类似链接，只需要在链接语法前加！即可。

![小光_newgame第八集](P:\1_File\_B1_图册\素材库\头像\小光_newgame第八集.png)

![测试图片](https://avatars0.githubusercontent.com/u/44776216?s=460&v=4)

### 斜体

*斜体*  
_斜体_

### 加粗

**加粗**  
__加粗__

### 编程

行内代码片使用右单引号（`）。
> 使用 `printf()`函数。

### 删除线

标准Markdown语法不支持。  
~~此为被删除的内容~~

### 下划线

使用原生HTML语法。  
<u>下划线</u>

### 行内数学公式

$\lim_{x \to \infty} \exp(-x) = 0$

## HTML

当纯Markdown语法不支持时，可以使用HTML个性化内容。

<span style="color:red">这句话是红色的</span>

### 嵌入内容

<iframe height='265'scrolling='no'title='Fancy Animated SVG Menu'src='http://codepen.io/jeangontijo/embed/OxVywj/?height=265&theme-id=0&default-tab=css,result&embed-version=2'frameborder='no'allowtransparency='true'allowfullscreen='true'style='width: 100%;'></iframe>
### 视频

<video src="xxx.mp4"/>