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

# FortiGate Security Appliance 1 Gbps の保護
{: #securing-the-fortigate-security-appliance-1-gbps}

セキュリティーおよびコンプライアンスの要件を満たすように FortiGate Security Appliance (FSA) 1Gbps を構成できます。 IBM© Cloud では、VDOM 管理者アカウントとランダムに割り当てられたパスワードが提供されます。お客様は、このパスワードを置き換えること、読み取り専用ユーザーを作成すること、および「トラステッド・ホスト」に基づいてアクセスを制限することができます。「トラステッド・ホスト」では、指定の送信元 IP (最大 3 つ) からのトラフィックのみ受け入れられます。 これらのアクティビティーを実行するには、以下のようにします。

1. [カスタマー・ポータル![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/){: new_window}の**「デバイスの詳細」**ページにある資格情報を使用して、アプライアンスにログインします。 資格情報を見つけるには、[FortiGate Security Appliance の管理方法](/docs/infrastructure/fortigate-1g?topic=fortigate-1g-managing-the-fortigate-security-appliance-1gbps)の指示に従います。
2. アプライアンスにログインした後、**「システム」>「管理」> 「管理者」**にナビゲートします。 すべてのアクセスおよび変更がログに記録されます。
3. 個々のインターフェースを構成するには、**「システム」>「ネットワーク」>「インターフェース」**にナビゲートします。

    管理インターフェースへのアクセスを、必要なプロトコル (通常は HTTPS と SSH。転送時の暗号化が提供されるため) に制限できます。また、追加のセキュリティーのために、管理インターフェースへの外部アクセスを無効にすることができます。 これは、「内部」インターフェース (お客様のパブリック VLAN があるインターフェース) で該当するプロトコルを有効にし、「外部」インターフェース (パブリック・インターネット・トラフィックを受信するインターフェース) ですべてのプロトコルを無効にすることで実現します。 この追加のセキュリティー手段では、ユーザーは、FSA の管理元の VLAN 内にサーバーを配置する必要があります。 
