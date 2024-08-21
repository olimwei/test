---
title: "创建Gallery"
layout: splash
classes: wide
excerpt: "创建一个Gallery"
header:
  image: /assets/images/unsplash-gallery-image-1.jpg
  teaser: assets/images/unsplash-gallery-image-1-th.jpg
sidebar:
  - title: 
    nav: XXX
gallery:
  - url: /assets/images/unsplash-gallery-image-1.jpg
    image_path: assets/images/unsplash-gallery-image-1-th.jpg
    alt: "placeholder image 1"
  - url: /assets/images/unsplash-gallery-image-2.jpg
    image_path: assets/images/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
  - url: /assets/images/unsplash-gallery-image-3.jpg
    image_path: assets/images/unsplash-gallery-image-3-th.jpg
    alt: "placeholder image 3"
---

第一组图片是原模版的方式：

{% include gallery caption="这是第一个用原模版建立的Gallery" %}

上面的方法需要在yml里自己设定好。

第二组gallery是增加的一个gallery script:

{::comment}用实际的目录替换test{:/comment}

{% include image-gallery.html folder="/assets/album/test" %} 

这个方法直接把文件放在相应的目录下，其他交给script去执行。