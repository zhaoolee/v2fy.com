---
title: 让Linux Ubuntu KDE桌面smb拷贝更快，提升Plex server影视服务器读取效率
tags:
- 个人成长
categories:
- ubuntu
---



## 安装软件包

```
sudo apt-get install cifs-utils -y
```

## 创建挂载点



```
mkdir -p ~/home-smb
```



## 创建密码凭据文件

```
sudo vim /etc/credentials
```



在凭据文件中添加内容

```
username='smb登陆用户名'
password='smb登陆密码'
```

## 修改权限

```
sudo chmod 600 /etc/credentials
```

## 挂载smb服务路径文档

```
sudo mount -t cifs //192.168.66.217/root ~/home-smb -o credentials=/etc/credentials
```



有用的挂载选项：

- `uid=1000,gid=1000` - 设置挂载后的文件所有者

- `dir_mode=0755,file_mode=0644` - 设置目录和文件权限

- `vers=3.0` - 指定`SMB`协议版本

- `iocharset=utf8` - 设置字符编码



## 实现开机自动挂载





我在ubuntu系统的管理员用户名`zhaoolee`, 也会创建同名用户组`zhaoolee`



在 `/etc/fstab` 尾部添加以下内容

```
//192.168.66.217/root /home/zhaoolee/home-smb cifs credentials=/etc/credentials,iocharset=utf8 0 0

# 如果想要权限更开放
//192.168.66.217/root /home/zhaoolee/home-smb cifs credentials=/etc/credentials,iocharset=utf8,uid=zhaoolee,gid=zhaoolee,file_mode=0777,dir_mode=0777,noperm 0 0
```



## 测试是否顺利挂载

```
# 取消挂载
sudo umount /home/zhaoolee/home-smb
# 测试挂载
sudo systemctl daemon-reload
```





## 使用Plex server



```
# 查看plex所在用户组
groups plex

# 查看当前用户所在用户组
groups $(whoami) 


# 将plex加入zhaoolee用户组
sudo usermod -aG zhaoolee plex

sudo systemctl restart plexmediaserver
```



Plex server可以读取`zhaoolee`可以读取的文件了

