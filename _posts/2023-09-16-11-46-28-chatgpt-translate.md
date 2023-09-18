---
title: 内容出海，让ChatGPT将中文Markdown内容翻译为中英对照的格式
categories:
- 独立博客的方方面面
---


中文互联网内容环境审查越来越严，为了长久的发展，我决定探索一下内容出海。

内容出海的第一步是发布英语内容，我的策略是用ChatGPT将以前写的内容扎实的技术类文章，转换为中英对照的形式。

我的文章都用纯文本Markdown管理，这种纯文本很适合交给ChatGPT进行管理，以下是我将Markdown内容输入给ChatGPT进行处理的规则。



## 以下是我给ChatGPT定义的转换规则

请你扮演一位风趣幽默的翻译大师, 将提供的Markdown文本转换为**中英对照**的格式, 如果提供的Markdown格式换行不规范, 请对Markdown进行语法修复后再进行转换

转换要求:

1. Markdown标题翻译: 先中文后英文，中英文之间中间用` / `分割；

Markdown标题翻译示例输入: 
```
## 树莓派不吃灰
```
Markdown标题翻译示例输出
```
## 树莓派不吃灰 / Pi in Use
```

2. Markdown段落翻译: 要求中英对照, 分为4个步骤

Markdown段落翻译第1步骤: 输出原中文段落内容

Markdown段落翻译第2步骤: 输出两个换行符

Markdown段落翻译第3步骤: 在输出翻译的英文内容前先输出🌈, 然后输出翻译完成的英文内容, 这里的🌈是内容的一部分, 不要破坏原有的Markdown排版

Markdown段落翻译第4步骤: 输出两个换行符


Markdown段落示例输入:

```
前段时间, 有一台老式MacBook Pro被我改造成了影视资源解码主机, [《树莓派家庭服务器搭建指南》第十七期：树莓派配合性能更好的闲置笔记本搭建开源免费jellyfin私人影院](https://v2fy.com/p/2023-06-10-jellyfin-1686388142000/) , 我想通过远程桌面访问这台MacBook Pro, 发现Mac虽然原生支持VNC连接，但实际用起来经常画面撕裂，于是我找了一款开源的远程桌面程序rustdesk, 将其服务部署在树莓派上，实现局域网设备丝滑访问, 外网设备也可以通过内网穿透直接访问macOS

rustdesk的Github开源地址 https://github.com/rustdesk/rustdesk
```

Markdown段落示例输出:

```
前段时间, 有一台老式MacBook Pro被我改造成了影视资源解码主机, [《树莓派家庭服务器搭建指南》第十七期：树莓派配合性能更好的闲置笔记本搭建开源免费jellyfin私人影院](https://v2fy.com/p/2023-06-10-jellyfin-1686388142000/) , 我想通过远程桌面访问这台MacBook Pro, 发现Mac虽然原生支持VNC连接，但实际用起来经常画面撕裂，于是我找了一款开源的远程桌面程序rustdesk, 将其服务部署在树莓派上，实现局域网设备丝滑访问, 外网设备也可以通过内网穿透直接访问macOS

🌈A while ago, I transformed an old MacBook Pro into a video resource decoding host, [《Raspberry Pi Home Server Building Guide》Issue 17: Raspberry Pi combined with a better performing idle laptop to build an open-source free jellyfin private cinema](https://v2fy.com/p/2023-06-10-jellyfin-1686388142000/). I wanted to access this MacBook Pro via a remote desktop. Although Mac natively supports VNC connections, the actual use often results in screen tearing. So, I found an open-source remote desktop program called rustdesk and deployed its service on the Raspberry Pi, achieving silky smooth access for LAN devices. Devices outside the network can also directly access macOS through intranet penetration.

rustdesk的Github开源地址 https://github.com/rustdesk/rustdesk

🌈The open-source Github address for rustdesk: https://github.com/rustdesk/rustdesk

```

3. Markdown列表格式翻译: 要求中英对照, 分为4个步骤

Markdown列表格式翻译第1步骤: 输出原中文段落内容

Markdown列表格式翻译第2步骤: 输出两个换行符

Markdown列表格式翻译第3步骤: 输出`- 🌈{翻译后的英文内容}`, 注意格式, 不要遗漏🌈

Markdown列表格式翻译第4步骤: 输出两个换行符

Markdown列表格式示例1输入:

```
- 开源, 支持私有化部署

- 不限制连接数量

- 支持Windows, macOS, Linux, 一套方案搞定远程控制

- 通过内网映射的方案, 让你随时随地远程控制内网设备

- 内网访问丝滑流畅, 自动切换内外网流量
```

Markdown列表格式翻译示例1输出:

```
- 开源, 支持私有化部署

- 🌈Open source, supports private deployment

- 不限制连接数量

- 🌈No limit on the number of connections

- 支持Windows, macOS, Linux, 一套方案搞定远程控制

- 🌈Supports Windows, macOS, Linux, one solution for remote control

- 通过内网映射的方案, 让你随时随地远程控制内网设备

- 🌈Through the intranet mapping solution, you can remotely control intranet devices anytime, anywhere

- 内网访问丝滑流畅, 自动切换内外网流量

- 🌈Intranet access is silky smooth, automatically switches between intranet and extranet traffic

```


Markdown列表格式示例2输入:

```
- 内网访问丝滑流畅, 自动切换内外网流量
```

Markdown列表格式翻译示例2输出:

```
- 内网访问丝滑流畅, 自动切换内外网流量

- 🌈Intranet access is silky smooth, automatically switches between intranet and extranet traffic

```



3. 图片格式的文本不需要翻译，按原文输出即可, 也就是图片只需要输出一次, 如果图片alt描述部分存在内容, 请将其转换为`[中文 / 英语](图片url)`的格式

图片翻译示例1输入:

```
![](https://cdn.fangyuanxiaozhan.com/assets/1686388246080mDPR12E1.png)
```

图片翻译示例1输出:

```
![](https://cdn.fangyuanxiaozhan.com/assets/1686388246080mDPR12E1.png)
```

图片翻译示例2输入:

```
![钢铁侠](https://cdn.fangyuanxiaozhan.com/assets/1686388272416NjcfMTXC.png)
```

图片翻译示例2输出:

```
![钢铁侠 / Iron Man](https://cdn.fangyuanxiaozhan.com/assets/1686388272416NjcfMTXC.png)
```


4. Markdown超链接翻译规则: `()` 部分的内容无需翻译, 超链接描述`[]`部分需要翻译

Markdown超链接翻译示例输入:

```
[《树莓派家庭服务器搭建指南》第二十一期：部署开源远程桌面服务rustdesk,内网丝滑,外网流畅控制Windows,macOS,Linux主机](https://v2fy.com/p/2023-09-12-09-51-24-rustdesk/)
```

Markdown超链接翻译示例输出:

```
[《Raspberry Pi Home Server Building Guide》Issue 21 Deploy the open-source remote desktop service rustdesk, smoothly control Windows, macOS, Linux hosts in the intranet and fluently in the extranet](https://v2fy.com/p/2023-09-12-09-51-24-rustdesk/)
```

5. Markdown代码块翻译规则: 如果代码块不包含注释，按原文输出即可; 如果注释中出现单行注释, 则在中文注释后追加 `/` 和翻译为英语的注释即可

Markdown代码块翻译示例输入:

```
# 创建挂载目录
mkdir -p /opt/rustdesk
chmod 755 -R /opt/rustdesk
# 创建用于存放docker-compose.yml的目录
mkdir -p /opt/rustdesk-docker-compose-yml
chmod 755 -R /opt/rustdesk-docker-compose-yml
```

Markdown代码块翻译示例输出:
```
# 创建挂载目录 / Creating Mount Directory
mkdir -p /opt/rustdesk
chmod 755 -R /opt/rustdesk
# 创建用于存放docker-compose.yml的目录 / Creating Directory for docker-compose.yml
mkdir -p /opt/rustdesk-docker-compose-yml
chmod 755 -R /opt/rustdesk-docker-compose-yml
```




以下为需要使用翻译的Markdown中文内容:

(粘贴Markdown文本)

我用自己写的《树莓派不吃灰》系列最新的三篇，试了一下水，翻译的效果还不错，用不了多久，就能完成整个系列的翻译。

https://github.com/pi

![new](https://cdn.fangyuanxiaozhan.com/assets/16948557499963QXej1Kx.png)

