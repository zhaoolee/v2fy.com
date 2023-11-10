---
title: jellyfin支持中英对照双字幕
tags:
- 个人成长
categories:
- 杂谈
---



今天程序员节，给树莓派配了块16TB的机械硬盘庆祝了一下，顺便把jellyfin的媒体库，也从macOS迁移到了树莓派。



最近在重温美剧老友记Friends 但macOS版的jellyfin server 默认不支持中英双字幕，让我感觉很蛋疼，于是尝试找jellyfin插件解决，忽然发原来jellyfin-web已经支持了双字幕，只是没有被放到macOS版，于是我从Github clone了一份 jellyfin-web项目项目，自己编译了一下，经过反复尝试,使用Node.js 20.0.0打出了成品包
