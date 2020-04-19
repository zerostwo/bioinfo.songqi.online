---
title: R Markdown的使用技巧
author: Songqi Duan
date: '2020-04-17'
slug: r_markdown
categories:
  - 生物信息学
tags:
  - R
lastmod: '2020-04-19T11:42:23+08:00'
keywords: []
description: ''
comment: true
postMetaInFooter: true
hiddenFromHomePage: no
contentCopyright: "<a href='https://creativecommons.org/licenses/by-nc-nd/4.0/'>CC BY-NC-ND 4.0</a>"
reward: no
mathjax: true
mathjaxEnableSingleDollar: true
mathjaxEnableAutoNumber: true
hideHeaderAndFooter: no
flowchartDiagrams:
  enable: no
  options: ''
sequenceDiagrams:
  enable: no
  options: ''
---
`R markdown`通过R代码创建交互式报告。这篇文章提供了一些我每天用来改善输出文档外观的技巧。

此文介绍`R markdown`的一些使用技巧和常用快捷键[^1][^2]。

# 1 图片居中

```R
<center>
![Naruto](http://songqi.zzmath.top/Naruto.jpg){width=50%}
</center>
```

<center>
![Naruto](https://songqi.zzmath.top/Naruto.jpg){width=50%}
</center>
<center style="font-size:16px;color:#C0C0C0;margin-block-start: 1em;margin-block-end: 1em;">图1. 言ったことは、まげねぇ。それが俺の忍道だ！</center>

# 2 图注

可以在`{r}`中增添以下信息：

```R
{r, 
  fig.align="center", fig.width=6, fig.height=6,
  fig.cap="我是图注."
}
```

```R
plot(c(1:10))
```
<center>
![plot(c(1:10))](https://songqi.zzmath.top/unnamed-chunk-1-1.png)
</center>
</center>
<center style="font-size:16px;color:#C0C0C0;margin-block-start: 1em;margin-block-end: 1em;">图2. 我是图注.</center>

# 3 数学公式

块级公式：

```Latex
$$E=mc^2$$
```

$$E=mc^2$$
行内公式：

```Latex
$c\approx 299,792,458\space m/s$
```

其中$c\approx 299,792,458\space m/s$

# 4 并排放两张图

可以在`{r}`中增添以下信息：

```R
{r out.width=c('50%', '50%'), fig.show='hold'}
```

```R
boxplot(rnorm(10))
plot(rnorm(10))
```

<center>![boxplot](https://songqi.zzmath.top/unnamed-chunk-2-1.png){width=50%}![plot](https://songqi.zzmath.top/unnamed-chunk-2-2.png){width=50%}</center>
<center style="font-size:16px;color:#C0C0C0;margin-block-start: 1em;margin-block-end: 1em;">图3. 并排放两张图.</center>


[^1]: [Pimp my RMD: a few tips for R Markdown](https://holtzy.github.io/Pimp-my-rmd/#)
[^2]: [第 5 章 R Markdown](https://bookdown.org/xiao/RAnalysisBook/r-markdown.html)

