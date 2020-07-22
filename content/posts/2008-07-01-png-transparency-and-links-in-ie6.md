---
date: 2008-07-01T12:12:43+08:00
title: PNG透明，IE6和链接
categories:
- tech
tags:
- ie
- png
---
PNG透明在IE6下可以通过AlphaImageLoader滤镜实现，可是如果是背景透明，经常会遇到链接失效的问题。

这种情况，可是尝试修改背景图片的尺寸，这是IE6,7的一个bug，在某些尺寸下，链接可点，在某些尺寸下，链接不可点。

<http://www.daltonlp.com/view/217>
