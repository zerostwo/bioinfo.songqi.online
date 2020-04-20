`R markdown`通过R代码创建交互式报告。这篇文章提供了一些我每天用来改善输出文档外观的技巧。

此文介绍`R markdown`的一些使用技巧和常用快捷键[^1][^2]。

# 1 图片居中

`.Rmd`文件写法：

```r
<center>
![Naruto](){width=50%}
</center>
```

`.md`文件写法：

```markdown
{{% figure class="center" src="http://songqi.zzmath.top/Naruto.jpg" title="图1. 言ったことは、まげねぇ。それが俺の忍道だ！" alt="Naruto" width="50%"%}}
```

{{% figure class="center" src="http://songqi.zzmath.top/Naruto.jpg" title="图1. 言ったことは、まげねぇ。それが俺の忍道だ！" alt="Naruto" width="50%"%}}

# 2 图注

可以在`{r}`中增添以下信息：

```r
{r, 
  fig.align="center", fig.width=6, fig.height=6,
  fig.cap="我是图注."
}
```

```r
plot(c(1:10))
```

{{% figure class="center" src="https://songqi.zzmath.top/unnamed-chunk-1-1.png" title="图2. 我是图注." alt="plot(c(1:10))" width="50%"%}}


# 3 数学公式

块级公式：

```latex
$$E=mc^2$$
```

$$E=mc^2$$

行内公式：

```latex
\\( c\approx 299,792,458\space m/s \\)
```

其中\\( c\approx 299,792,458\space m/s \\)

# 4 并排放两张图

可以在`{r}`中增添以下信息：

```r
{r out.width=c('50%', '50%'), fig.show='hold'}
```

```r
boxplot(rnorm(10))
plot(rnorm(10))
```

{{% figure class="center" src="https://songqi.zzmath.top/unnamed-chunk-2-1.png" title="图3. 并排放两张图." alt="boxplot" width="50%"%}}

{{% figure class="center" src="https://songqi.zzmath.top/unnamed-chunk-2-2.png" title="图3. 并排放两张图." alt="plot" width="50%"%}}

[^1]: [Pimp my RMD: a few tips for R Markdown](https://holtzy.github.io/Pimp-my-rmd/#)
[^2]: [第 5 章 R Markdown](https://bookdown.org/xiao/RAnalysisBook/r-markdown.html)

