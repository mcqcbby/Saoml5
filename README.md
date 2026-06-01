🚀 Saoml 流控系统安装教程

«⚠️ 免责声明

本文档仅供个人学习、测试及合法授权环境使用。

请勿将本项目用于任何违反法律法规、平台规则或运营商服务条款的用途。使用者应自行承担相关责任。»

---

📖 项目说明

Saoml 流控系统可用于 CentOS 7 环境下的相关学习与测试。

本文档主要包含以下内容：

- 基础安装流程
- APP 工具生成方式
- 线路配置位置说明
- 常见问题排查

---

🖥️ 环境准备

建议提前准备以下环境：

- 一台 CentOS 7 服务器
- Root 权限或具备 "sudo" 权限的账号
- 可正常访问 GitHub 的网络环境
- 已开放所需服务端口的安全组或防火墙规则

---

① 下载 Saoml

执行以下命令：

wget -O xsaoml https://raw.githubusercontent.com/mcqcbby/Saoml5/refs/heads/main/xsaoml;chmod +x xsaoml;./xsaoml

---

② 安装

执行以下命令：

mv -f /root/xsaoml /bin/xsaoml;chmod 777 /bin/xsaoml;xsaoml

---

③ 生成 APP

一般来说，自带 APP 对部分新手用户可能不太友好，可以使用以下工具生成新的 APP。

wget -O saoml5 https://raw.githubusercontent.com/mcqcbby/Saoml5/refs/heads/main/saoml5;chmod +x saoml5;./saoml5

或：

chmod 777 saoml5;./saoml5

---

④ 线路配置说明

安装并生成 APP 后，由于部分线路推送可能已经失效，因此需要根据实际情况自行配置线路。

配置示意图

"image" (https://github.com/MessInch/saoml-/blob/main/%E5%9B%BE%E7%89%87%E7%B4%A0%E6%9D%90.png?raw=true)

配置代码

remote webwebfenxi.189.cn 9000
http-proxy [domain] 8080

参数说明

- 第一行 "remote" 后填写对应地址
- 后方端口一般无需修改
- 不同地区、不同网络环境效果可能存在差异
- 第二行中的 "[domain]" 变量会自动填写服务器 IP 地址

---

🔧 常见问题

出现 302、400 等状态码

如果出现相关错误，可优先检查：

- 服务器端口是否开放
- 安全组规则是否正确配置
- 防火墙是否正常放行相关端口

如果使用腾讯云、阿里云等云服务器，请前往控制台检查安全组设置。

防火墙示意图

"image" (https://github.com/MessInch/saoml-/blob/main/1.png?raw=true)

端口配置

TCP：1 - 65535
UDP：1 - 65535

部分场景可能会使用随机端口，请根据实际情况进行配置。

---

⚠️ 责任声明

本程序及相关资料仅供学习与研究用途。

请在遵守当地法律法规、服务协议及相关规定的前提下使用本项目。

文档中涉及的图片、文字、数据及其他素材，其版权归原作者或相关权利人所有。

使用本程序所产生的一切后果及法律责任均由使用者自行承担，作者不对任何直接或间接损失承担责任。

---

📌 最终说明

- 仅供学习交流使用
- 请遵守当地法律法规
- 请遵守相关服务协议
- 请勿用于任何非法用途

感谢支持。
