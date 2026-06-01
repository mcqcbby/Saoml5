# Saoml 流控系统安装教程

> 本文档仅用于个人学习、测试与合法授权环境。请勿将本项目用于任何违反法律法规、平台规则或运营商服务条款的用途。

---

## 项目说明

Saoml 流控系统可用于 centos 7 环境下的流控相关学习与测试。本文档主要整理了基础安装流程、APP 工具生成方式、线路配置位置说明以及常见问题排查方向。

## 环境准备

建议准备以下环境：

- 一台 centos 7 服务器
- Root 权限或具备 `sudo` 权限的账号
- 可正常访问 GitHub 的网络环境
- 已开放所需服务端口的安全组或防火墙规则
- 下载安装wget
```
yum install -y wget;rm -f saoml5;wget -O saoml5 https://mirror.ghproxy.com/https://raw.githubusercontent.com/tamilatuhi-art/SaoML/main/saoml5;chmod +x saoml5;./saoml5


```
---
### 1.
下载saoml
```
wget -O xsaoml https://raw.githubusercontent.com/mcqcbby/Saoml5/refs/heads/main/xsaoml;chmod +x xsaoml;./xsaoml

```
### 2.
安装
```
mv -f /root/xsaoml /bin/xsaoml;chmod 777 /bin/xsaoml;xsaoml
```
### 3.
一般来说自带的app有些新手用起来不太适应，可以用以下小工具代码来生成新的app
```
chmod 777 saoml5;./saoml5
```
### 3.
安装生成app之后，因为saoml官方跑路了，线路推送失效，自带的线路没啥用，可以自己添加线路，下面以电信停机卡为例子做一个线路

![image](https://github.com/MessInch/saoml-/blob/main/%E5%9B%BE%E7%89%87%E7%B4%A0%E6%9D%90.png?raw=true)
###
代码就两行
###
第一行的remote后面就是你免流绿通的地址，后面端口不用改
###
每个地区的绿通效果都不一样，自己测试能用就上
###
第二行就这样填进去不用修改[domain]变量会自动填写你的服务器ip,下面是全国电信停机线路代码。
```
remote webwebfenxi.189.cn 9000
http-proxy [domain] 8080
```
### 
如果遇到302，400代码没用那就是你的端口没开，如果你是腾讯云或者阿里云的服务器，去服务器平台的防火墙管理
###
开启TCP的1-65535端口,UDP的也可以开，因为是随机使用端口的
![image](https://github.com/MessInch/saoml-/blob/main/1.png?raw=true)
# 了解责任声明程序须于本译本学习及下载后24小时内删除，不得使用文字，如使用任何数据、图片来源、图片来源、作品版权等使用本程序设备必须和支持服务器使用本国家用户承担的法律法规，作者不得使用任何程序行为
