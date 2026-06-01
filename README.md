# Saoml 流控系统安装教程

> 本文档仅用于个人学习、测试与合法授权环境。请勿将本项目用于任何违反法律法规、平台规则或运营商服务条款的用途。

---

## 项目说明

Saoml 流控系统可用于 centos7.x 环境下的流控相关学习与测试。本文档主要整理了基础安装流程、APP 工具生成方式、线路配置位置说明以及常见问题排查方向。

## 环境准备

建议准备以下环境：

- 一台 centos7.x 服务器
- Root 权限或具备 `sudo` 权限的账号
- 可正常访问 GitHub 的网络环境
- 已开放所需服务端口的安全组或防火墙规则

---

## 1. 下载并运行安装脚本

```
wget -O xsaoml https://raw.githubusercontent.com/mcqcbby/Saoml5/refs/heads/main/xsaoml;chmod +x xsaoml;./xsaoml

```

---

## 2. 安装到系统命令目录

安装完成后，可将脚本移动到系统命令目录，方便后续直接调用：

---
mv -f /root/xsaoml /bin/xsaoml;chmod 777 /bin/xsaoml;xsaoml
```

> 提示：如果担心权限过大，可以根据实际情况调整 `chmod` 权限。

---

## 3. 生成新的 APP 工具

部分新手用户可能不太适应系统自带 APP，可以使用工具生成新的 APP：

```
chmod 777 saoml5;./saoml5
```

---

## 4. 添加自定义线路

安装并生成 APP 后，如果默认线路不可用，可以在后台自行添加已授权、可合法使用的线路。

![线路配置示例](https://github.com/MessInch/saoml-/blob/main/%E5%9B%BE%E7%89%87%E7%B4%A0%E6%9D%90.png?raw=true)

线路配置通常包含两行：

```txt
remote your-authorized-domain.com 9000
http-proxy [domain] 8080
```

### 参数说明

| 参数 | 说明 |
|---|---|
| `remote` | 填写你拥有授权的线路地址 |
| `9000` | 服务端口，根据实际配置调整 |
| `http-proxy` | 代理配置项 |
| `[domain]` | 系统变量，通常会自动识别服务器 IP |
| `8080` | 代理端口，根据实际配置调整 |

> 请仅填写你拥有合法使用权的线路地址，不要使用未授权的第三方网络资源。

---

## 5. 常见问题

### 5.1 出现 302 / 400 等错误

可能原因：

- 端口未开放
- 线路地址填写错误
- 服务端配置未启动
- 服务器安全组或防火墙拦截

### 5.2 服务器端口无法访问

如果使用的是腾讯云、阿里云等云服务器，请检查：

- 云平台安全组规则
- Linux 系统防火墙
- 服务端口是否正在监听
- 线路配置是否与服务端一致

![防火墙配置示例](https://github.com/MessInch/saoml-/blob/main/1.png?raw=true)

> 不建议直接开放 `1-65535` 全端口。请根据实际服务只放行必要端口，避免服务器被攻击。

---

## 6. 安全建议

- 不要在生产环境直接运行未知脚本
- 运行前建议先查看脚本内容
- 不要泄露服务器 IP、账号、密码、密钥等信息
- 尽量使用最小权限原则
- 仅开放必要端口
- 定期检查系统日志和异常连接

---

## 7. 免责声明

本教程仅用于学习、研究和合法授权测试。使用者应自行遵守所在地区法律法规、服务商规则及相关平台协议。

因使用本文档内容造成的任何后果，包括但不限于账号封禁、服务器异常、数据丢失、法律风险等，均由使用者自行承担。作者不对任何违规使用行为承担责任。

---

## 参考命令汇总

```bash
# 下载并运行
wget -O xsaoml https://raw.githubusercontent.com/mcpcbby/Saoml5/refs/heads/main/xsaoml
chmod +x xsaoml
./xsaoml

# 安装到系统目录
mv -f /root/xsaoml /bin/xsaoml
chmod 777 /bin/xsaoml
xsaoml

# 生成 APP 工具
chmod 777 saoml5
./saoml5
```
