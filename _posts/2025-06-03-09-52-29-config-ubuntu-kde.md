---
title:  让KDE输入法更好用的配置Fcitx5 + Rime（中州韵）
tags:
- 个人成长
categories:
- ubuntu
---





### ✅ 在 Ubuntu 的 KDE 桌面环境下 **KDE输入法推荐：Fcitx5 + Rime（中州韵）**

#### 📌 优点：/

- **系统集成好**：Fcitx5 在 KDE（Plasma）下兼容性非常好，界面美观，响应迅速。
- **Rime 输入法引擎**：支持拼音、双拼、仓颉、五笔等各种方案，极其灵活，支持自定义词库、输入风格。
- **KDE 配套支持完善**：托盘图标清晰，输入法切换稳定。

#### 🔧 安装命令（适用于 Ubuntu 20.04/22.04/24.04）：

```bash
sudo apt update
sudo apt install fcitx5 fcitx5-chinese-addons fcitx5-rime
```

然后设置环境变量：

```bash
im-config -n fcitx5
```

注销或重启。

#### 🚀 启动配置工具（可视化设置）：

```bash
fcitx5-configtool
```



