---
date: 2007-10-18T21:13:45+08:00
title: ipod touch/iphone 视频转换脚本
categories:
- tech
tags:
- iphone
- tool
- script
- video
---
ipod touch入手好几天了，终于找到一个速度不错的linux下的转换方案，拿出来分享一下。
这个脚本需要先安装mencoder,gpac
linux版
```
#!/bin/bash
mencoder -ofps 24000/1001  -ovc lavc -lavcopts vcodec=mpeg4:vhq:vbitrate=600 -vf scale=480:-11,pullup,softskip,harddup -oac faac -faacopts mpeg=4:br=128:object=2 -channels 2 -srate 48000 "$1" -o "$1".avi
MP4Box -aviraw audio "$1".avi
MP4Box -aviraw video "$1".avi
mv "$1"_video.FMP4 "$1".m4v
mv "$1"_audio.raw "$1".aac
MP4Box -add "$1".aac -add "$1".m4v:fps=23.976 "$1".mp4
rm "$1".avi
rm "$1".aac
rm "$1".m4v
```
