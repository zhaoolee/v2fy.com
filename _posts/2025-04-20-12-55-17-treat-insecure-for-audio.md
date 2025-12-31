---
title: Chrome浏览器在http网页上支持打开麦克风
tags:
- 个人成长
categories:
- 杂谈
---



在开发过程中，可能会用到在http服务使用麦克风，Chrome浏览器默认禁止了http网页使用麦克风，如果需要在本地浏览器允许麦克风，需要将ip写入浏览器，方法如下



```
chrome://flags/#unsafely-treat-insecure-origin-as-secure
```



![image-20250420125711229](./2025-04-20-12-55-17-treat-insecure-for-audio.assets/1745125031712RKe4zD0E.png)

修改完成后，重启浏览器即可！
