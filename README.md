# 🚀 Saoml 流控系统

<p align="center">
  流控系统安装与使用教程
</p>

<p align="center">
  <img src="https://img.shields.io/badge/System-CentOS%207-blue">
  <img src="https://img.shields.io/badge/Version-Saoml5-green">
  <img src="https://img.shields.io/badge/Status-Available-success">
</p>

---

## 📖 项目介绍

Saoml 流控系统可用于 CentOS 7 环境下的相关学习与测试。

### 功能列表

- 📦 一键安装
- 📱 APP生成工具
- 🌐 自定义线路配置
- 🔧 配置管理
- 📋 常见问题排查

---

## 🖥️ 环境要求

| 项目 | 要求 |
|--------|--------|
| 系统 | CentOS 7 |
| 权限 | Root |
| 网络 | 可访问 GitHub |
| 端口 | 已开放相关端口 |

---

# 📥 安装教程

## ① 下载 Saoml

```bash
wget -O xsaoml https://raw.githubusercontent.com/mcqcbby/Saoml5/refs/heads/main/xsaoml;chmod +x xsaoml;./xsaoml
```

---

## ② 安装

```bash
mv -f /root/xsaoml /bin/xsaoml;chmod 777 /bin/xsaoml;xsaoml
```

---

## ③ APP生成工具

下载工具：

```bash
wget -O saoml5 https://raw.githubusercontent.com/mcqcbby/Saoml5/refs/heads/main/saoml5;chmod +x saoml5;./saoml5
```

执行：

```bash
chmod 777 saoml5;./saoml5
```

---

## ④ 配置线路

### 配置示意图

<p align="center">
<img src="https://github.com/MessInch/saoml-/blob/main/%E5%9B%BE%E7%89%87%E7%B4%A0%E6%9D%90.png?raw=true">
</p>

### 配置代码

```txt
remote webwebfenxi.189.cn 9000
http-proxy [domain] 8080
```

---

# ❓ 常见问题

### 出现 302 / 400

检查：

- 安全组
- 防火墙
- 端口开放情况

### 防火墙示意图

<p align="center">
<img src="https://github.com/MessInch/saoml-/blob/main/1.png?raw=true">
</p>

---

# ⚠️ 免责声明

本项目仅供学习交流使用。

请遵守所在地法律法规及相关服务协议。

因使用本项目产生的一切后果均由使用者自行承担。

---

<p align="center">

⭐ 如果本项目对您有所帮助，欢迎 Star 支持 ⭐

</p>
