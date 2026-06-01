🚀 Saoml 流控系统安装教程

«⚠️ 免责声明

本文档仅用于个人学习、测试与合法授权环境。

请勿将本项目用于任何违反法律法规、平台规则或运营商服务条款的用途。»

---

📋 目录

- "项目说明" (#项目说明)
- "环境准备" (#环境准备)
- "下载 Saoml" (#1-下载-saoml)
- "安装" (#2-安装)
- "生成 APP" (#3-生成-app)
- "线路配置" (#4-线路配置)
- "常见问题" (#常见问题)
- "责任声明" (#责任声明)

---

项目说明

Saoml 流控系统可用于 CentOS 7 环境下的流控相关学习与测试。

本文档主要整理了：

- 基础安装流程
- APP 工具生成方式
- 线路配置位置说明
- 常见问题排查方向

---

环境准备

建议准备以下环境：

- 一台 CentOS 7 服务器
- Root 权限或具备 "sudo" 权限的账号
- 可正常访问 GitHub 的网络环境
- 已开放所需服务端口的安全组或防火墙规则

---

1. 下载 Saoml

执行以下命令：

wget -O xsaoml https://raw.githubusercontent.com/mcqcbby/Saoml5/refs/heads/main/xsaoml;chmod +x xsaoml;./xsaoml

---

2. 安装

执行以下命令：

mv -f /root/xsaoml /bin/xsaoml;chmod 777 /bin/xsaoml;xsaoml

---

3. 生成 APP

一般来说，自带 APP 对部分新手用户可能不太适应，可以使用以下工具生成新的 APP。

下载生成工具

wget -O saoml5 https://raw.githubusercontent.com/mcqcbby/Saoml5/refs/heads/main/saoml5;chmod +x saoml5;./saoml5

或执行

chmod 777 saoml5;./saoml5

---

4. 线路配置

安装生成 APP 后，由于部分线路推送可能已经失效，因此需要根据实际情况自行配置线路。

配置示意图

"线路配置示意图" (https://github.com/MessInch/saoml-/blob/main/%E5%9B%BE%E7%89%87%E7%B4%A0%E6%9D%90.png?raw=true)

---

配置代码

remote webwebfenxi.189.cn 9000
http-proxy [domain] 8080

配置说明

«第一行的 "remote" 后面填写对应地址，后面的端口一般无需修改。»

«不同地区、不同网络环境效果可能存在差异，请根据实际情况测试。»

«第二行中的 "[domain]" 变量会自动填写服务器 IP。»

---

常见问题

出现 302、400 状态码

如果出现相关错误：

- 检查服务器端口是否开放
- 检查安全组配置
- 检查系统防火墙状态

对于腾讯云、阿里云等云服务器，请前往控制台检查安全组规则。

防火墙配置示意图

"防火墙配置" (https://github.com/MessInch/saoml-/blob/main/1.png?raw=true)

推荐配置

TCP：1-65535
UDP：1-65535

---

责任声明

«本程序仅供学习与研究用途。

使用者应遵守所在地法律法规及相关服务协议。

文档中涉及的文字、图片、数据及其他素材版权归原作者或相关权利人所有。

因使用本程序产生的一切后果及法律责任均由使用者自行承担，作者不承担任何直接或间接责任。»

---

<div align="center">⭐ 如果本项目对您有所帮助，欢迎点个 Star 支持一下

</div>
