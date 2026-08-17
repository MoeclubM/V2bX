# V2bX

> **本项目已停止维护。**  
> 这是 [wyx2685/V2bX](https://github.com/wyx2685/V2bX) 的 fork，更新了 Sing-box 内核并适配新版 Xboard Machine API。  
> 如仍需节点服务端，请使用 [NodeRS](https://github.com/MoeclubM/NodeRS)。

[![](https://img.shields.io/badge/TgChat-UnOfficialV2Board%E4%BA%A4%E6%B5%81%E7%BE%A4-green)](https://t.me/unofficialV2board)
[![](https://img.shields.io/badge/TgChat-YuzukiProjects%E4%BA%A4%E6%B5%81%E7%BE%A4-blue)](https://t.me/YuzukiProjects)

A V2board node server based on Sing-box, modified from XrayR.  
一个基于Sing-box内核的V2board节点服务端，修改自XrayR，支持Vmess,Vless,Trojan,Shadowsocks,Hysteria,AnyTLS,Naive等协议。

**注意： 本项目需要搭配[修改版V2board](https://github.com/wyx2685/v2board)或[Xboard](https://github.com/cedar2025/Xboard)**

## 特点

* 永久开源且免费。
* 支持多种协议。
* 支持Vless和XTLS/AnyTLS等新特性。
* 支持单实例对接多节点，无需重复启动。
* 支持限制在线IP。
* 支持限制Tcp连接数。
* 支持节点端口级别、用户级别限速。
* 配置简单明了。
* 修改配置自动重启实例。
* 基于Sing-box内核。
* 支持条件编译。

## 功能介绍

| 功能特性 | Vmess | Vless | Trojan | Shadowsocks | Hysteria | AnyTLS |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| 自动申请 TLS | √ | √ | √ | √ | √ | √ |
| 自动续签 TLS | √ | √ | √ | √ | √ | √ |
| 在线人数统计 | √ | √ | √ | √ | √ | √ |
| 审计规则 | √ | √ | √ | √ | √ | √ |
| 自定义 DNS | √ | √ | √ | √ | √ | √ |
| 在线 IP 限制 | √ | √ | √ | √ | √ | √ |
| 连接数限制 | √ | √ | √ | √ | √ | √ |
| 跨节点 IP 限制 | √ | √ | √ | √ | √ | √ |
| 用户限速 | √ | √ | √ | √ | √ | X |
| 动态限速 | √ | √ | √ | √ | √ | X |

## TODO

- 实现动态限速
- 使用文档

## 软件安装

### 脚本安装

```
wget -N https://raw.githubusercontent.com/MoeclubM/V2bX-Script/master/install.sh && bash install.sh
```

### 手动安装

[手动安装教程](https://v2bx.v-50.me/v2bx/v2bx-xia-zai-he-an-zhuang/install/manual)

## 获取方式

推荐直接使用 Release 预编译文件或安装脚本，不需要在本地自行编译。

- 安装脚本：`https://raw.githubusercontent.com/MoeclubM/V2bX-Script/master/install.sh`
- Release 下载：`https://github.com/MoeclubM/V2bX/releases`
## 配置文件及详细使用教程

当前版本仅支持 Xboard 机器模式，本地配置只保留顶层 `Machines` 数组。每个机器最少需要配置 `ApiHost`、`ApiKey` 和 `MachineID`。

```json
{
  "Machines": [
    {
      "ApiHost": "https://panel.example.com",
      "ApiKey": "your-api-key",
      "MachineID": 1
    }
  ]
}
```

[详细使用教程](https://v2bx.v-50.me/)

## 免责声明

* 开源免费项目，不保证功能完美，出现问题请在Issues反馈。
* 不对任何人使用本项目造成的任何后果承担责任。
* 本项目可能会随想法或思路的变动随性更改项目结构或大规模重构代码，若不能接受请勿使用。

## Thanks

* [V2Fly](https://github.com/v2fly)
* [VNet-V2ray](https://github.com/ProxyPanel/VNet-V2ray)
* [Air-Universe](https://github.com/crossfw/Air-Universe)
* [XrayR](https://github.com/XrayR/XrayR)
* [sing-box](https://github.com/SagerNet/sing-box)
* [wyx2685/V2bX](https://github.com/wyx2685/V2bX)
