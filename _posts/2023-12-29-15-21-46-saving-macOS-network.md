---
title: 如何拯救macOS的Chrome在一些特定Wifi下访问url频繁报错ERR_NETWORK_CHANGED Your connection was interrupted ,但刷一下网页又能访问的情况
tags:
- 个人成长
categories:
- 极客实用技巧
---

最近我在特定wifi环境下，使用macOS的Chrome浏览器访问网页时，时不时会打不开网页，然后白屏报错，但是隔几秒钟，刷一下网页，又好了，非常烦人。

![image-20231229155652757](https://cdn.fangyuanxiaozhan.com/assets/1703836613297R4FHTksH.png)

```
Your connection was interrupted
A network change was detected.
ERR_NETWORK_CHANGED
```

这个现象的奇妙之处在于，并不是纯粹的网络问题，因为换用macOS版的Safari访问各种url完全没有问题，只有Chrome才有问题。



于是我在网络上查找攻略，都是讲重启路由器，检查网络什么的，但实际并不生效，



最后我在某位Github老哥的留言下，找到了答案 https://github.com/brave/brave-browser/issues/5958



![image-20231229152747393](https://cdn.fangyuanxiaozhan.com/assets/1703834867923ApJWa5wz.png)

最后的治疗措施是，打开macOS终端，输入以下命令后，回车即可生效

```
networksetup -setv6off "Wi-Fi"
```
![image-20231229153750565](https://cdn.fangyuanxiaozhan.com/assets/1703835470932CwD1ZS1Z.png)

最后打开系统偏好设置，在`Wi-Fi` 的Details下查看`TCP/IP`， `Configure IPv6` 被设置为`Off`则表示ipv6确实被禁止了。 



![image-20231229153118916](https://cdn.fangyuanxiaozhan.com/assets/1703835079271sFNjH773.png)

![image-20231229153027933](https://cdn.fangyuanxiaozhan.com/assets/1703835028300rZ5dkGFe.png)

最后重启一下macOS，Chrome的报错`ERR_NETWORK_CHANGED` 就不会出现了。
