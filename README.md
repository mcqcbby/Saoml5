# 🚀 Saoml 流控系统安装教程

> ⚠️ 本文档仅用于个人学习、测试与合法授权环境。

---

## 项目说明

Saoml 流控系统可用于 CentOS 7 环境下的相关学习与测试。

---

## 环境准备

- 一台 CentOS 7 服务器
- Root 权限账号
- 可访问 GitHub 的网络环境
- 已开放所需服务端口

---

## 1️⃣ 下载 Saoml

```bash
wget -O xsaoml https://raw.githubusercontent.com/mcqcbby/Saoml5/refs/heads/main/xsaoml;chmod +x xsaoml;./xsaoml
```

---

## 2️⃣ 安装

```bash
mv -f /root/xsaoml /bin/xsaoml;chmod 777 /bin/xsaoml;xsaoml
```

---

## 3️⃣ 生成 APP

```bash
wget -O saoml5 https://raw.githubusercontent.com/mcqcbby/Saoml5/refs/heads/main/saoml5;chmod +x saoml5;./saoml5
```

```bash
chmod 777 saoml5;./saoml5
```

---

## 4️⃣ 配置说明

![image](https://github.com/MessInch/saoml-/blob/main/%E5%9B%BE%E7%89%87%E7%B4%A0%E6%9D%90.png?raw=true)

```text
remote webwebfenxi.189.cn 9000
http-proxy [domain] 8080
```

---

## 常见问题

![image](https://github.com/MessInch/saoml-/blob/main/1.png?raw=true)

---

## 责任声明

本项目仅供学习交流使用，请遵守当地法律法规。
