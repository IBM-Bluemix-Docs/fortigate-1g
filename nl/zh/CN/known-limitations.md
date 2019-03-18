---

copyright:
  years: 2017
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# FortiGate Security Appliance (FSA) 1Gbps 已知限制
{: #known-limitations-of-fortigate-security-appliance-1gbps}

FortiGate Security Appliance (FSA) 1Gbps 具有以下已知限制：

* 处理 ARP 的方式导致与 Windows 网络负载均衡 (NLB) 不兼容。

* 高可用性故障转移功能未向用户公开。如果主防火墙发生故障，但未自动故障转移，那么需要提交支持凭单。建议对关键服务进行设备监视，以确保防火墙可正确传递流量。

* 无法将 FortiGate Security Appliance 部署在当前与网关、Hardware Firewall 或其他 FortiGate Security Appliance 相关联的 VLAN 上。

* FortiGate Security Appliance 与单个公用客户 VLAN（“内部”VLAN）相关联，无法访问专用网络。
