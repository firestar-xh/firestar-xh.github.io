---
layout:     post
title:      "Hello Makrdown"
subtitle:   " \"Hello World, Hello Blog\""
date:       2024-7-14 12:00:00
author:     "Xh"
header-img: "img/markdown_bg.jpg"
catalog: true
tags:
    - Meta
---

> “Yeah It's on. ”

Markdown 是一种轻量级标记语言，它的语法简洁明了，易于学习和使用。它最初由 John Gruber 在 2004 年创建，目的是让文档的编写变得更简单和直观，同时能够生成结构良好的 HTML。

## 正文

接下来说说 Markdown 的基本语法和用法：

### 标题

Markdown 支持两种标题的语法，Setext 和atx 形式。

Setext 形式是用底线的形式，利用两个换行符来定义标题，底线的长度对应标题的级别。

atx 形式则是在行首插入 1 到 6 个 # ，对应 H1 到 H6 标题，行首的 # 数量对应标题的级别。


#### Setext 形式
```
Title 1
=======

Title 2
-------
```

#### atx 形式
```
# Title 1

## Title 2

### Title 3

#### Title 4

##### Title 5

###### Title 6 
```
---
### 列表

Markdown 支持有序列表和无序列表。

无序列表使用星号、加号或是减号作为列表标记：

#### 星号列表形式
```
* Red
* Green
* Blue
```

#### 加号列表形式
```
+ Red
+ Green
+ Blue
```

#### 减号列表形式
```
- Red
- Green
- Blue
```

#### 有序列表则使用数字接着一个英文句点：

```
1. Bird
2. McHale
3. Parish
```
---
### 引用代码块

Markdown 也支持代码块的语法，代码块的语法有两种，一种是行内代码块，即在文字前面加上 1 个反引号 ` ，如：

    `print("Hello, World!")`

另一种是代码块，即在每行加上 4 个空格或者一个制表符，如：

    ```python
    def fib(n):    # write Fibonacci series up to n
        a, b = 0, 1
        while a < n:
            print(a, end=' ')
            a, b = b, a+b    # calculate the next term
        print()
    ```
---
### 转义字符

Markdown 使用反斜杠 `\` 来转义一些特殊字符，比如星号、加号、减号、下划线等。如果你需要在文字中插入反斜杠，可以在反斜杠后面加上反斜杠，比如：

```
\*this text is surrounded by literal asterisks\*
```
---
### 字体

Markdown 还支持加粗、斜体和删除线。

#### 加粗

Markdown 使用两个星号或是两个下划线包围的文字会被转化为粗体，如：

```
**This text will be bold**
```

#### 斜体

Markdown 使用一个星号或是一个下划线包围的文字会被转化为斜体，如：

```
*This text will be italic*
_This text will also be italic_
```

#### 删除线

Markdown 使用两个波浪线包围的文字会被转化为删除线，如：

```
~~This text will be deleted~~
```
#### 文本高亮

Markdown 还支持文本高亮的语法，使用两个波浪线包围的文字会被高亮显示，如：

```
==This text will be highlighted==
```
---
### 分割线

你可以在一行中用三个以上的星号、减号、下划线来建立一个分割线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。

```
***
---
___
```
---
### 链接

Markdown 支持两种形式的链接语法，行内式和参考式两种形式。

行内式的链接是在方括号后面紧接着圆括号并插入链接，如：

```
This is an [example link](http://example.com/).
```

参考式的链接是在链接文字的括号后面再接上另一个方括号，里面放链接的标题，如：

```
This is an [example link][id].

[id]: http://example.com/
```
ULR 地址也可以用尖括号包围，不过这种方式不够直观，不建议使用。
```
URL: http://example.com/
```
---
### 图片

Markdown 也支持链接图片的语法，语法如下：

```
![alt text](image.jpg)

![alt text](https://www.markdownguide.org/assets/images/tux.png "Tux, the Linux mascot")
```
---
### 表格

Markdown 表格语法如下：

```
| Header1 | Header2 | Header3 |
|---------|---------|---------|
| Cell1   | Cell2   | Cell3   |
| Cell4   | Cell5   | Cell6   |
```

可以在第二行使用 `:` 来定义表头的对齐方式，`:---` 表示左对齐，`:---:` 表示居中对齐，`:-----` 表示右对齐。

```
| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |
```
---

### 公式

Markdown 也支持数学公式的语法，使用两个美元符 $$ 来包围公式，如：

```
$$E=mc^2$$
```

公式的大小可以使用 `\big`、`\small`、`\Large`、`\small` 等命令来调整。 公式的上下标可以使用 `_` 和 `^` 来表示，如：

```
$x_1 + 2x_2 = 3$

$x^2 + y^2 = z^2$
```

公式的对齐方式可以使用 `\left` 和 `\right` 命令来调整，如：

```
$$\left(\sum_{i=1}^n a_i\right)^2 \leq \sum_{i=1}^n a_i^2$$
``` 

公式的分组可以使用 `\frac` 命令来表示，如：

```
$$\frac{1}{2\pi i}\int\limits_{-\infty}^{\infty}e^{-i\pi/2}f(x)\,dx$$
```

公式的根号可以使用 `\sqrt` 命令来表示，如：

```
$$\sqrt{3x-1}+(1+x)^2$$
```
公式下标可以使用 `\sub` 和 `\sup` 命令来表示，如：

```
$$H_2O\sub{2} + O_2\sub{2} \rightarrow H_2O$$

$$H_2O\sup{2-} + O_2\sup{2-} \rightarrow H_2O$$
```

公式的分式可以使用 `\over` 和 `\under` 命令来表示，如：

```
$$\frac{x^2}{y^2} \over \frac{x^2+y^2}{y^2} = \frac{x}{y}$$

$$\frac{d}{dx}\left( \int_{-\infty}^{\infty} e^{-x^2} \,dx \right) = \frac{1}{\sqrt{\pi}}$$
```
---
### 其他

Markdown 还支持一些其他的语法，比如脚注、视频、音频等。 这些语法的详细信息请参考 [Markdown 语法说明](https://www.markdownguide.org/basic-syntax/)。