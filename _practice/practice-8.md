---
title: "practice-8"
layout: splash
classes: wide
excerpt: "Ginger Gulp design system including logo mark, website design, and branding applications."
header:
  image: /assets/images/unsplash-gallery-image-3.jpg
  teaser: assets/images/unsplash-gallery-image-3-th.jpg
sidebar:
  - title: "Role"
    image: http://placehold.it/350x250
    image_alt: "logo"
    text: "Designer, Front-End Developer"
  - title: "Responsibilities"
    text: "Reuters try PR stupid commenters should isn't a business model"
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

{% include gallery caption="This is a sample gallery to go along with this case study." %}

第二组gallery是增加的一个gallery script:

{::comment}用实际的目录替换test{:/comment}

{% include image-gallery.html folder="/assets/album/test" %} 