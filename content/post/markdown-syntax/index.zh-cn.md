+++
author = "Hugo Authors"
title = "Markdown 语法指南"
date = "2019-03-11"
description = "展示在 Hugo 内容文件中使用的基本 Markdown 语法和 HTML 元素格式的示例文章。"
tags = [
    "markdown",
    "css",
    "html",
    "themes",
]
categories = [
    "主题",
    "语法",
]
series = ["主题指南"]
aliases = ["migrate-from-jekyl"]
image = "pawel-czerwinski-8uZPynIu-rQ-unsplash.jpg"
+++

本文提供了可在 Hugo 内容文件中使用的基本 Markdown 语法示例，同时也展示了基本的 HTML 元素是否在 Hugo 主题中通过 CSS 进行了美化。

<!--more-->

## 标题

以下的 HTML `<h1>`—`<h6>` 元素代表了六个级别的章节标题。`<h1>` 是最高级别，而 `<h6>` 是最低级别。

# H1

## H2

### H3

#### H4

##### H5

###### H6

## 段落

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## 块引用

块引用元素代表引自其他来源的内容，可以包含一个必须位于 `footer` 或 `cite` 元素内的引用来源，也可以选择性地包含行内更改，例如注释和缩写。

#### 无归属的块引用

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **注意**，你可以在块引用中使用 _Markdown 语法_。

#### 带归属的块引用

> 不要通过共享内存来通信，而要通过通信来共享内存。<br>
> — <cite>罗布·派克[^1]</cite>

[^1]: 上面的引用摘自罗布·派克在 2015 年 11 月 18 日 Gopherfest 上的[演讲](https://www.youtube.com/watch?v=PAAkCSZUG1c)。

## 表格

表格不是核心 Markdown 规范的一部分，但 Hugo 原生支持它们。

| 姓名   | 年龄 |
| ------ | ---- |
| 鲍勃   | 27   |
| 爱丽丝 | 23   |

#### 表格内的行内 Markdown

| 斜体   | 粗体     | 代码   |
| ------ | -------- | ------ |
| _斜体_ | **粗体** | `代码` |

| A                                                        | B                                                                                                             | C                                                                                                                                    | D                                                 | E                                                          | F                                                                    |
| -------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------- | ---------------------------------------------------------- | -------------------------------------------------------------------- |
| Lorem ipsum dolor sit amet, consectetur adipiscing elit. | Phasellus ultricies, sapien non euismod aliquam, dui ligula tincidunt odio, at accumsan nulla sapien eget ex. | Proin eleifend dictum ipsum, non euismod ipsum pulvinar et. Vivamus sollicitudin, quam in pulvinar aliquam, metus elit pretium purus | Proin sit amet velit nec enim imperdiet vehicula. | Ut bibendum vestibulum quam, eu egestas turpis gravida nec | Sed scelerisque nec turpis vel viverra. Vivamus vitae pretium sapien |

## 代码块

#### 使用反引号的代码块

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Example HTML5 Document</title>
    </head>
    <body>
        <p>Test</p>
    </body>
</html>
```

#### 缩进四个空格的代码块

    <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Example HTML5 Document</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>

#### 使用 Hugo 内部高亮短代码的代码块

{{< highlight html >}}

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
{{< /highlight >}}

#### 差异代码块

```diff
[dependencies.bevy]
git = "https://github.com/bevyengine/bevy"
rev = "11f52b8c72fc3a568e8bb4a4cd1f3eb025ac2e13"
- features = ["dynamic"]
+ features = ["jpeg", "dynamic"]
```

## 列表类型

#### 有序列表

1. First item
2. Second item
3. Third item

#### 无序列表

-   List item
-   Another item
-   And another item

#### 嵌套列表

-   Fruit
    -   Apple
    -   Orange
    -   Banana
-   Dairy
    -   Milk
    -   Cheese

## 其他元素 — abbr, sub, sup, kbd, mark

<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Press <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> to end the session.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.

## 带超链接的图片

[![Google](https://www.google.com/images/branding/googlelogo/1x/googlelogo_light_color_272x92dp.png)](https://google.com)
