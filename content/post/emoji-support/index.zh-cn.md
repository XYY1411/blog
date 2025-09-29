+++
author = "Hugo Authors"
title = "Emoji 支持"
date = "2019-03-05"
description = "Hugo Emoji 使用指南"
categories = [
    "测试"
]
tags = [
    "Emoji",
]
image = "the-creative-exchange-d2zvqp3fpro-unsplash.jpg"
+++

在 Hugo 项目中，可以通过多种方式启用 Emoji。

<!--more-->

[`emojify`](https://gohugo.io/functions/emojify/) 函数可以直接在模板或 [内联 Shortcode](https://gohugo.io/templates/shortcode-templates/#inline-shortcodes) 中调用。

如果想在全站范围启用 Emoji，可以在站点的 [配置文件](https://gohugo.io/getting-started/configuration/) 中将 `enableEmoji` 设置为 `true`，然后就可以在内容文件中直接输入 Emoji 简写代码；例如：

<p><span class="nowrap"><span class="emojify">🙈</span> <code>:see_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙉</span> <code>:hear_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙊</span> <code>:speak_no_evil:</code></span></p>
<br>

[Emoji 速查表](http://www.emoji-cheat-sheet.com/)是一个非常实用的 Emoji 简写参考工具。

---

**注意**： 上述步骤启用了 Hugo 中的 Unicode 标准 Emoji 字符和序列，但这些符号的渲染效果取决于浏览器和平台。
如果需要自定义 Emoji 样式，可以使用第三方 Emoji 字体或字体堆栈，例如：

{{< highlight html >}}
.emoji {
font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
}
{{< /highlight >}}

{{< css.inline >}}

<style>
.emojify {
	font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
	font-size: 2rem;
	vertical-align: middle;
}
@media screen and (max-width:650px) {
  .nowrap {
    display: block;
    margin: 25px 0;
  }
}
</style>

{{< /css.inline >}}
