---
title: 内容出海，让ChatGPT将中文Markdown内容翻译为中英对照的格式
categories:
- 独立博客的方方面面
---

中文互联网内容环境审查越来越严，为了长久的发展，我需要探索一下内容出海。

内容出海的第一步是生产英语内容，我的策略是用ChatGPT将以前写的内容扎实的技术类文章，转换为中英对照的形式。

我的文章都用纯文本Markdown管理，这种纯文本很适合交给ChatGPT进行管理，以下是我将Markdown内容输入给ChatGPT进行处理的规则。


===


输入：简体中文Markdown文本

请你扮演一位风趣幽默的翻译大师, 将提供的Markdown文本转换为中英对照的格式

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

Markdown段落翻译第1步骤: 输入中文段落

Markdown段落翻译第2步骤: 输出两个换行符

Markdown段落翻译第3步骤: 输出 🌈+翻译完成的英文段落

Markdown段落翻译第4步骤: 输出两个换行符

Markdown段落翻译示例输入:

```
树莓派使用ARM架构的处理器，功耗极低，即使要负责给外接硬盘供电，最高功耗也不会超过15W
- 树莓派接口丰富，提供了2个USB 2.0接口, 2个USB 3.0接口，两个micro-HDMI接口，1个Type-C接口，1个极为先进的耳机接口， 一个网线接口，40个GPIO引脚；
```

Markdown段落翻译示例输出:

```
树莓派使用ARM架构的处理器，功耗极低，即使要负责给外接硬盘供电，最高功耗也不会超过15W

🌈Raspberry Pi uses an ARM architecture processor, with extremely low power consumption. Even if it is responsible for powering the external hard drive, the maximum power consumption will not exceed 15W.

- 树莓派接口丰富，提供了2个USB 2.0接口, 2个USB 3.0接口，两个micro-HDMI接口，1个Type-C接口，1个极为先进的耳机接口， 一个网线接口，40个GPIO引脚；

- 🌈Raspberry Pi has a rich interface, providing 2 USB 2.0 ports, 2 USB 3.0 ports, two micro-HDMI ports, 1 Type-C port, 1 extremely advanced headphone port, one Ethernet port, 40 GPIO pins.

```

3. 图片格式的文本不需要翻译，按原文输出即可;

4. Markdown超链接翻译规则: `[]`内部的内容, 输出格式为 `[中文原文 / 英语]`, `()` 部分的内容无需翻译

Markdown超链接翻译示例输入:
```
[《树莓派家庭服务器搭建指南》第二十一期：部署开源远程桌面服务rustdesk,内网丝滑,外网流畅控制Windows,macOS,Linux主机](https://v2fy.com/p/2023-09-12-09-51-24-rustdesk/)
```

Markdown超链接翻译示例输出:
```
[《树莓派家庭服务器搭建指南》第二十一期：部署开源远程桌面服务rustdesk,内网丝滑,外网流畅控制Windows,macOS,Linux主机 / 《Raspberry Pi Home Server Building Guide》Issue 21 Deploy the open-source remote desktop service rustdesk, smoothly control Windows, macOS, Linux hosts in the intranet and fluently in the extranet](https://v2fy.com/p/2023-09-12-09-51-24-rustdesk/)
```

5. Markdown代码块翻译规则: 如果输入markdown内容中包含代码块，按原文输出即可;


以下为需要使用翻译的Markdown中文内容:




我的天翼云服务器有`/opt` 和 `/usr/share/nginx`两个目录, 用来存储网站的内容, 数据无价, 为了避免珍贵的数据丢失，我决定使用树莓派运行 rsnapshot, 为网站内容做定期备份。


# 为什么选择rsnapshot？

- rsnapshot是基于rsync的开源软件, 原理简单，无后门, 无需强制加密, 备份后的数据所见即所得
- rsnapshot通过硬链接管理文件, 处于不同文件夹的同一个文件, 只占用一份存储空间, 节省磁盘 
- rsnapshot默认进行增量备份, 节省带宽。
- rsnapshot长期维护(从2015年开始维护), 功能稳定，在Github的开源仓库`https://github.com/rsnapshot/rsnapshot` 有2.9k Star，广受好评

## 安装rsnapshot

```
sudo apt install rsnapshot
```

![image-20230817161316501](https://cdn.fangyuanxiaozhan.com/assets/16922599974820YyapFbm.png)



## 配置树莓派免密登录云服务器



```
cd ~/.ssh
ssh-keygen
```

![image-20230817162637385](https://cdn.fangyuanxiaozhan.com/assets/1692260798024ikRi3ATB.png)



```
# 设置密钥权限 
# 公钥644
sudo chmod 644  ~/.ssh/fangyuanxiaozhan.com.pub
# 私钥600
sudo chmod 600  ~/.ssh/fangyuanxiaozhan.com
```



![image-20230817163241171](https://cdn.fangyuanxiaozhan.com/assets/1692261161591whEwecbf.png)

