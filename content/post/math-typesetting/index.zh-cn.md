---
author: Hugo Authors
title: 数学公式渲染
date: 2019-03-08
description: KaTeX 简要设置指南
math: true
---

在 Hugo 项目中可以启用数学公式表示法，这需要通过第三方 JavaScript 库来实现。
<!--more-->

在本示例中，我们将使用 [KaTeX](https://katex.org/)

- 在 `/layouts/partials/math.html` 路径下创建一个局部模板
- 在此局部模板中引用 [自动渲染扩展](https://katex.org/docs/autorender.html) 或在本地托管这些脚本
- 按如下方式将局部模板包含到您的模板中：

```bash
{{ if or .Params.math .Site.Params.math }}
{{ partial "math.html" . }}
{{ end }}
```

- 要全局启用 KaTeX，请在项目配置中将参数 `math` 设置为 `true`
- 要基于单个页面启用 KaTeX，请在内容文件中包含参数 `math: true`

**注意：** 请参考在线的 [支持的 TeX 函数列表](https://katex.org/docs/supported.html)

{{< math.inline >}}
{{ if or .Page.Params.math .Site.Params.math }}
<!-- KaTeX -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css" integrity="sha384-n8MVd4RsNIU0tAv4ct0nTaAbDJwPJzDEaqSD1odI+WdtXRGWt2kTvGFasHpSy3SV" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js" integrity="sha384-XjKyOOlGwcjNTAIQHIpgOno0Hl1YQqzUOEleOLALmuqehneUG+vnGctmUb0ZY0l8" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js" integrity="sha384-+VBxd3r6XgURycqtZ117nYw44OOcIax56Z4dCRWbxyPt0Koah1uHoK0o4+/RRE05" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
{{ end }}
{{</ math.inline >}}

### 示例

行内公式：$\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…$

块级公式：
$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$