---
title: "markdown语法练习"
layout: single-t
permalink: 
collection: 
excerpt: "markdown语法练习"
author_profile: true
toc: ture
toc_sticky: true
sidebar:
  - title: 
    nav: XXX
---

https://github.github.com/gfm/ 这是GH喜欢的格式

# 大标题 大小有6个级别的标题
## 中标题
### 字体变化

**加粗字体**， *斜字体*， ***加粗斜字体***， ~~化掉字体~~

### 列表

1. 有序列表1
2. 有序列表2
3. 有序列表3

- 无序列表1
- 无序列表2
- 无序列表3

1. 列表1
    - 列表嵌套1
    - 列表嵌套2
2. 列表2
3. 列表3

- [x] ~~完成的任务1~~
- [x] ~~完成的任务2~~
- [ ] 未完成的任务1
- [ ] 未完成的任务2

### 代码

`<p>This is the first item</p>`

`python3 -m install numpy`

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

### 链接

#### 第一种方法（可以正确显示）
[文字链接1](http://olim.ca)

#### 第2种方法（也可以）
[文字链接]: http://archiz.com

[文字链接2-阿齐兹][文字链接]

图片链接和文字链接不同的是前面有个感叹号。可以加鼠标移动到图片时显示的文字。

![走势图](http://money.olim.ca/assets/images/2024/2024-05-31-DXY.jpg "hover me")

[图片链接]: http://money.olim.ca/assets/images/2024/2024-05-31-DXY-fl.jpg "hover me"
![12345][图片链接]

上面两张图片在VS code预览不能正确显示（因为用了外部网址链接的方式？），在GH page上能正确显示。

下面图片在GH page不能正确显示，在VS code预览能正确显示（这里用了文件的相对路径的时候/前面多了两个点）
![测试图片](../assets/images/2024/2024-05-31-DXY-fl.jpg)

> 疑问：如何限制图片显示的尺寸？（用css来规范）

下面是用HTML的picture格式来规定图片的显示：

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/25423296/163456776-7f95b81a-f1ed-45f7-b7ab-8fa810d529fa.png">
  <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://money.olim.ca/assets/images/2024b/AI-20240813-comments-1.png">
  <source media="(prefers-color-scheme: light)" srcset="https://money.olim.ca/assets/images/2024/2024-05-31-DXY-fl.jpg">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://money.olim.ca/assets/images/2024/2024-05-31-DXY-fl.jpg">
</picture>

### 插入视频
这里采用两种方法
#### 用html的video标签
`<video src="本地视频路径"></video>`

#### 用iframe
```
<iframe 
src="视频或者网页路径" 
scrolling="no" 
border="0" 
frameborder="no" 
framespacing="0" 
allowfullscreen="true" 
height=600 
width=800> 
</iframe>
```

<iframe 
src="/assets/video/blooming.mp4" 
scrolling="no" 
border="0" 
frameborder="no" 
framespacing="0" 
allowfullscreen="true" 
height=600 
width=800> 
</iframe>

<!-- 21:9 aspect ratio -->
<div class="embed-responsive embed-responsive-21by9">
  <iframe class="embed-responsive-item" src="/assets/video/blooming.mp4"></iframe>
</div>

<!-- 16:9 aspect ratio -->
<div class="embed-responsive embed-responsive-16by9">
  <iframe class="embed-responsive-item" src="/assets/video/blooming.mp4"></iframe>
</div>

<!-- 4:3 aspect ratio -->
<div class="embed-responsive embed-responsive-4by3">
  <iframe class="embed-responsive-item" src="/assets/video/blooming.mp4"></iframe>
</div>

<!-- 1:1 aspect ratio -->
<div class="embed-responsive embed-responsive-1by1">
  <iframe class="embed-responsive-item" src="/assets/video/blooming.mp4"></iframe>
</div>

### 引用 用>符号

> 这是引用的内容。
> 1. 引用内容里包括的列表1
> 2. 引用内容里包括的列表2

### 表格的制作

| SyntaxExpression | LongDescription | OtherNotesIncluded |
|:-----------|:-----------:|-----------:|
| Header | Title | Items |
| Paragraph | Text | Note |

上面这表格在vs code里预览能正确显示。在github page上不能正确显示。试过好多次不行。下面就没问题，太奇怪。

| 第二栏目居右 | 第二栏目居左居左 | 第三栏目居中居中居中居中居中居中 |
|-----:|:--------------|:-----------:|
|     1|     靠左边     | 居中排列的话1 |
|     2|     靠左左     | 居中排列的话2 |
|     3|     左左左     | 居中排列的话3 |

表格老是会出现这样或那样的问题。！

### 水平线制作 用三个“-”"*""_"符号都可以

第一种水平线(三个破折号，***建议使用***)

---

第二种水平线（三个星号，有时候有问题。我这里用了6ge星号）

******

第三种水平线（三个下划线，有时候有问题。我这里用了6个下划线.....不要考虑！）
______

### 脚注 （不正确显示）
这句话包括一个脚注明。[^1]

下面是我从GH里copy来的一段：
Here is a simple footnote[^2].

A footnote can also have multiple lines[^3].

[^1]: 第一个脚注明。 .  
[^2]: My reference.
[^3]: To add line breaks within a footnote, prefix new lines with 2 spaces.   This is a second line.这里脚注显示两行出现问题。

### 路径图 （在GH上都不能正确显示）

Here is a simple flow chart:

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

### 高亮选择的段落 （检查是否正确显示）

1. 用“==”在所选段落的前后 （这种方法在github不工作）
2. 用<mark>mark</mark>语言 （这个可以）

I need to highlight these ==very important words==.
我需要高亮==这段重要的话。==

我需要<mark>高亮这几个字</mark>。

### 点击展开更多内容：

<details>
<summary>这里copy了那个正确显示的table</summary>

| 第二栏目居右 | 第二栏目居左居左 | 第三栏目居中居中居中居中居中居中 |
|-----:|:--------------|:-----------:|
|     1|     靠左边     | 居中排列的话1 |
|     2|     靠左左     | 居中排列的话2 |
|     3|     左左左     | 居中排列的话3 |

</details>

上面点开显示的table格式有问题，这是copy前面能显示正确的table，放在这里却不能正常显示了。。。。这是一个需要解决的“问题”。。。

### 几种底色形式的notice

（在bootstrap里叫alert） （（在GH上能正确显示，通过GH转由netlify发布就不能正确显示，后来通过直接外接bootstrap的css就统一了。）

<div class="notice">
  <p>这是没有表明类别的notice</p>
</div>
<div class="notice--primary">
  <p>这是primary类的notice</p>
</div>
<div class="notice--info">
  <p>这是information类的notice</p>
</div>
<div class="notice--danger">
  <p>这是danger类的notice</p>
</div>
<div class="notice--success">
  <p>这是success类的notice</p>
</div>
<div class="notice--warning">
  <p>这是warning类的notice</p>
</div>
上面是自己在本地css的定义。。。下面是来自于bootstrap对alert的语法：

<div class="alert alert-primary" role="alert">
  This is a primary alert—check it out!
</div>
<div class="alert alert-secondary" role="alert">
  This is a secondary alert—check it out!
</div>
<div class="alert alert-success" role="alert">
  This is a success alert—check it out!
</div>
<div class="alert alert-danger" role="alert">
  This is a danger alert—check it out!
</div>
<div class="alert alert-warning" role="alert">
  This is a warning alert—check it out!
</div>
<div class="alert alert-info" role="alert">
  This is a info alert—check it out!
</div>
<div class="alert alert-light" role="alert">
  This is a light alert—check it out!
</div>
<div class="alert alert-dark" role="alert">
  This is a dark alert—check it out!
</div>

而GH DOC网站上记载的alert格式在GH上却不能正常显示😄。。。可能是设置相互冲突或missing。

> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.

去掉前面的括号看看行不行：（证明了，不行😄）

[!CAUTION]
Advises about risks or negative outcomes of certain actions.


### 按钮 （来自于bootstrap）

<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-dark">Dark</button>

<button type="button" class="btn btn-link">Link</button>

按钮group：

<div class="btn-group" role="group" aria-label="Basic example">
  <button type="button" class="btn btn-secondary">Left</button>
  <button type="button" class="btn btn-secondary">Middle</button>
  <button type="button" class="btn btn-secondary">Right</button>
</div>

### Badge

<h1>Example heading <span class="badge badge-secondary">New</span></h1>
<h2>Example heading <span class="badge badge-secondary">New</span></h2>
<h3>Example heading <span class="badge badge-secondary">New</span></h3>
<h4>Example heading <span class="badge badge-secondary">New</span></h4>
<h5>Example heading <span class="badge badge-secondary">New</span></h5>
<h6>Example heading <span class="badge badge-secondary">New</span></h6>

### Carousel
A slideshow component for cycling through elements—images or slides of text—like a carousel.

it requires util.js.

<div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
  <ol class="carousel-indicators">
    <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
  </ol>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="/assets/images/2024b/AI-20240808-comments-1.png" alt="First slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="/assets/images/2024b/AI-20240809-comments-1.png" alt="Second slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="/assets/images/2024b/AI-20240812-comments-1.png" alt="Third slide">
    </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>

### 用HTML代码
```
<h1>This is a heading</h1>
<p>Paragraph...</p>

<hr />

<img src="auto-generated-path-to-file-when-you-upload-image" width="200">
<a href="https://github.com/im-luka">Follow me on GitHub</a>

<br />
<br />

<p>Quick hack for <strong><em>centering image</em></strong>?</p>
<p align="center"><img src="auto-generated-path-to-file-when-you-upload-image" /></p>

<details>
  <summary>One more quick hack? 🎭</summary>
  
  → Easy  
  → And simple
</details>
``` 

### 显示颜色代码的三种方式：
hex，rgb， hsl

The background color is `#ffffff` for light mode and `rgb(9, 105, 218)` for blue and `hsl(212, 92%, 45%)`for  blue mode again.

### 其它
$H_2$ O, $X^2$, $Y^3$

$`H_2`$ O; $`3^4`$; （看看这种方法是否可行）

只有下面这种方式可以正确显示：(用sub sup)
5<sup>2</sup>; H<sub>2</sub>O

下面的全部在github page上不能正确显示但在vs code预览里面正确显示。（我把`$`符号前后加了一个\`符号，看看效果）

$`\alpha`$ 

$\alpha$ $\beta$ $\delta$ $\gamma$ $\epsilon$ $\zeta$ $\eta$ $\theta$ $\iota$ $\kappa$ $\lambda$ $\mu$ $\nu$ $\xi$ $\pi$ $\rho$ $\sigma$ $\tau$ $\upsilon$ $\phi$ $\chi$ $\psi$ $\omega$

$\infty$; $+\infty$; $-\infty$

$\frac{3+8a}{5b+6}$

$\sum{3x^n}$

$\sum_{n=1}^N{3x^n}$

$\prod{3x^n}$

$\prod_{n=1}^N{3x^n}$

$\sqrt[5]{100}$

$\int^5_1{f(x)}{\rm d}x$

$\iint^5_1{f(x)}{\rm d}x$

$\iiint^5_1{f(x)}{\rm d}x$

$\lim_{n\rightarrow+\infty} n$

$\geq$; $\leq$; $\subset$; $\supset$; $\in$; $\pm$; $\cdot$ $\times$ $\div$ $\not=$ $\not<$ $\not\supset$ $\log$ $\ln$ $\bot$ $\angle$ $30^\circ$ $\sin$ $\cos$ $\tan$ $\leftarrow$ $\rightarrow$ $\uparrow$ $\downarrow$ $\longrightarrow$ 

$\log_2{18}$ 

$
  \begin{matrix}
   1 & 2 & 3 \\\
   4 & 5 & 6 \\\
   7 & 8 & 9
  \end{matrix}
$

$
 \begin{Bmatrix}
   1 & 2 & 3 \\\
   4 & 5 & 6 \\\
   7 & 8 & 9
  \end{Bmatrix}
$

$
 \begin{bmatrix}
   1 & 2 & 3 \\\
   4 & 5 & 6 \\\
   7 & 8 & 9
  \end{bmatrix}
$

$
\left[
\begin{matrix}
 1      & 2      & \cdots & 4      \\\
 7      & 6      & \cdots & 5      \\\
 \vdots & \vdots & \ddots & \vdots \\\
 8      & 9      & \cdots & 0      \\\
\end{matrix}
\right]
$

$\begin{bmatrix}
{a_{11}}&{a_{12}}&{\cdots}&{a_{1n}}\\\
{a_{21}}&{a_{22}}&{\cdots}&{a_{2n}}\\\
{\vdots}&{\vdots}&{\ddots}&{\vdots}\\\
{a_{m1}}&{a_{m2}}&{\cdots}&{a_{mn}}\\\
\end{bmatrix}$

$\begin{cases}
a_1x+b_1y+c_1z=d_1\\\
a_2x+b_2y+c_2z=d_2\\\
a_3x+b_3y+c_3z=d_3\\\
\end{cases}
$


