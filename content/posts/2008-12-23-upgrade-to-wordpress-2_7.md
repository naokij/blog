---
date: 2008-12-23T23:20:07+08:00
title: 升级到WordPress 2.7
categories:
- tech
tags:
- wordpress
- tool
---
刚刚upgrade好，前台全变乱码了。折腾了半天，终于弄好了：

修改wp-config.php

define('DB_COLLATE', 'ascii-bin');

一般人都用的utf8-general-ci，我的只有ascii-bin才能正常，搞不懂。
