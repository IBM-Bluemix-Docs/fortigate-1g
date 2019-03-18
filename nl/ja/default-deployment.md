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

# Fortigate Security Appliance 1Gbps のデフォルト・デプロイメント
{: #default-deployment-of-a-fortigate-security-appliance-1gbps}

FortiGate Security Appliance (FSA) 1Gbps は、単一の仮想ドメイン (通常は firewall001) として専用アプライアンスにデプロイされます。 お客様は、アプライアンスのリソース (プロセッサー、メモリーなど) にフルアクセスできますが、デバイス・レベルの構成へのアクセスは制限されます。これは、IBM© Cloud でデバイスを効果的にサポートできるようにするためです。

FSA は、NAT モードでデプロイされ、パブリック・ネットワーク・インフラストラクチャー内の 2 つの VLAN/ネットワークに配備されます。 外部 VLAN は IBM Cloud パブリック VLAN で、ここでトラフィックはデータ・センターに入り、FSA にルーティングされます。 内部 VLAN は、お客様が割り当てた保護対象のパブリック FCR (フロントエンド・カスタマー・ルーター) VLAN で、ここにお客様のサーバー・リソースが配備されます。  

IBM Cloud では、プロビジョニング・プロセス中に、FSA と 2 つの結合 1G インターフェースが、これらの 2 つのネットワークそれぞれにデプロイされます。 また IBM Cloud では、デバイスのプロビジョニングおよびメンテナンスのための単一インターフェースもデプロイされます。お客様は、このインターフェースは利用できません。

このファイアウォールは、デプロイされた時点では、すべての IPv4 および IPv6 トラフィックが許可されます。これには、IBM Cloud の内部管理ネットワークがファイアウォールを経由してデバイスにアクセスするのを許可する目的の特定ルール (softlayer-admin) が含まれます。 サービス妨害の保護およびその他のほとんどのフィルターは、適用されないように構成されます。
