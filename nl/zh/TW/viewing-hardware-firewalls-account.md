---

copyright:
  years: 2017,2018
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 檢視 Fortigate 防火牆
{: #viewing-your-fortigate-firewalls}

若要查看哪些 VLAN 受防火牆保護，並尋找個別防火牆的相關詳細資料，請移至 VLAN 頁面。

1. 從瀏覽器中，開啟[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window} 並登入您的帳戶。
2. 在「客戶入口網站」導覽中，選取**網路 > IP 管理 > VLAN**。

表格中的每一列代表基礎架構中的 VLAN。IBM© Cloud 會自動移入「VLAN 號碼」和「主要路由器」資訊，以指出真實的 VLAN 號碼及在其上所配置的路由器。「名稱」欄位可用來為 VLAN 提供一個可識別的名稱（例如 DMZ、內部網路、公用或資料庫）。

最右邊的直欄**閘道/防火牆**包含何種防火牆保護準備就緒的相關詳細資料，例如：

- **新增防火牆**表示此 VLAN 上的伺服器沒有防火牆準備就緒。
- **個別受保護的伺服器**表示一台以上的伺服器正在使用 Hardware Firewall (Shared)，而且沒有 Hardware Firewall (Dedicated)、FortiGate Security Appliance 或「網路閘道」準備就緒。VLAN 防火牆和網路閘道無法置於有個別受保護的伺服器的 VLAN 上。
- **Firewall-vlanXXXX.networklayer.com** 表示有 Hardware Firewall (Dedicated) 或 FortiGate Security Appliance 準備就緒。只有一個 VLAN 防火牆或「網路閘道」可以與 VLAN 相關聯，但可以透過 VLAN 防火牆在公用 VLAN 上保護伺服器，並在專用網路上與「網路閘道」相關聯。
- **閘道名稱**表示 VLAN 與「網路閘道」相關聯。

## 個別受保護的伺服器詳細資料

在**閘道/防火牆**欄位中，對於具有**個別受保護的伺服器**的 VLAN，您可以按一下相關聯的 VLAN 號碼鏈結來顯示 VLAN 的詳細資料，包括相關聯的裝置。

在相關聯的裝置清單中，您可以按一下每個裝置並捲動至「配置」標籤的底端。您會在附加元件區段中看到**防火牆**，狀態為**已安裝**或**未安裝**。

- **未安裝**表示此裝置沒有防火牆準備就緒。
- **已安裝**表示防火牆已準備就緒，而且在可以管理防火牆配置的裝置上您會有一個**防火牆**標籤可用。

## 專用的防火牆詳細資料

在**閘道/防火牆**欄位中，對於具有 **Firewall-vlanXXXX.networklayer.com** 的 VLAN，您可以按一下該防火牆鏈結來顯示「防火牆」的詳細資料。裝置詳細資料包括相關聯的路由器、VLAN、IPv4/IPv6 子網路、與該 VLAN 相關聯的裝置，以及穿過或圍繞防火牆路由資料流量的控制項。

FortiGate Security Appliance 會有管理 IP、使用者名稱及密碼。FortiGate Security Appliance 的管理會透過其自己的 GUI 或 SSH 型主控台來完成。

## 網路閘道詳細資料

在**閘道/防火牆**欄位中，對於具有「網路閘道」裝置名稱的 VLAN，您可以按一下該「網路閘道」名稱來顯示「網路閘道」的詳細資料。裝置詳細資料包括相關聯的前端 (FCR) 和後端 (BCR) VLAN 及「網路閘道」管理選項。
