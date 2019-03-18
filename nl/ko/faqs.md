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
{:faq: data-hd-content-type='faq'}

# FSA(FortiGate Security Appliance) 1Gbps에 대한 FAQ
{: #faqs-for-fortigate-security-appliance-1gbps}

다음은 FSA(FortiGate Security Appliance) 1Gbps 방화벽을 사용하여 작업할 때 자주 묻는 질문입니다.

## 방화벽이란 무엇입니까?
{:faq}

방화벽은 서버에서 상위로 연결된 네트워크 디바이스입니다. 방화벽은 트래픽이 서버에 도달하기 전에 서버에서 원하지 않는 트래픽을 차단합니다.

## 방화벽을 사용해야 하는 이유는 무엇입니까?
{:faq}

방화벽 사용의 주요한 장점은 서버가 "양호한" 트래픽 처리에만 집중할 수 있다는 점입니다. 즉, 리소스가 원하지 않는 트래픽까지 처리하는 대신 의도된 목적대로만 사용됩니다.

## IBM©에서 제공하는 방화벽 제품
{:faq}

[이 주제](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-exploring-firewalls)를 검토하여 IBM Cloud에서 제공되는 모든 방화벽 제품에 대한 상세한 비교를 볼 수 있습니다. 

## FortiGate Security Appliance 1Gbps가 IBM의 로드 밸런서 제품과 호환 가능합니까?
{:faq}

예, 그렇습니다. FSA 1Gbps는 Citrix Netscaler VPX 및 MPX뿐만 아니라 클라우드 로드 밸런싱 서비스, 로컬 로드 밸런서와 호환 가능합니다.

## 퍼블릭 트래픽이 내 로드 밸런서 또는 방화벽 중 어디를 먼저 통과합니까?
{:faq}

 공용 인터넷에서 오는 경우 로드 밸런싱 제품이 첫 번째, Hardware Firewall 제품이 그 다음, 그리고 NetScaler 제품이 (고객 서버와 함께) 마지막입니다.

## IBM에서 방화벽 대역폭에 대해 비용을 청구합니까?
{:faq}

FortiGate Security Appliance 1Gbps는 대역폭으로 측정되지 않습니다. 또한 FSA는 서버가 응답해야 하는 트래픽을 제한하여 대역폭 총 사용량을 줄일 수 있습니다.
{:faq}

## 내 Windows 방화벽에서 비활성화되는 포트는 무엇입니까?
{:faq}

IBM Cloud에서는 Evault, SNMP 및 Nagios 모니터링을 포함하여 서버와 함께 활용할 수 있는 다양한 서비스를 제공합니다. 이러한 서비스를 사용하려면 당사의 내부 시스템이 사용자의 서버와 정해진 기준 이상으로 통신할 수 있어야 합니다. 예외 목록에 표시되는 비활성화된 포트는 내부 네트워크 포트용으로만 열린 포트입니다. 공용(인터넷) 네트워크 연결에 대해서는 계속 차단됩니다. 내부 네트워크는 보안 네트워크이므로 해당 포트를 여는 것이 안전한 것으로 간주됩니다.

이러한 포트는 일반적으로 수정될 수 없습니다. 단, 방화벽 규칙을 재설정하는 경우 포트가 예외 목록에서 지워집니다. 방화벽 규칙을 재설정하면 이러한 추가 서비스에 부작용이 발생할 수 있으며 서버 구성에 따라 다른 문제가 발생할 수도 있습니다.

## 방화벽을 통해 허용되는 IP 범위는 무엇입니까?
{:faq}

방화벽을 통해 허용되는 IP 주소 및 IP 범위 목록을 보려면 [여기](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-ibm-cloud-ip-ranges)로 이동하십시오. 

## FortiGate Security Appliance 1Gbps가 보호할 수 있는 최대 서버 수는 몇 개입니까?
{:faq}

FortiGate Security Appliance 1Gbps는 공용 VLAN 상의 모든 서버를 보호할 수 있습니다. 단, 이러한 방화벽 디바이스는 2Gbps 업링크에 연결되므로 애플리케이션의 성능 요구를 충족하도록 방화벽 인스턴스의 수를 조정하도록 권장합니다. 추가 방화벽 및 연관된 컴퓨팅 리소스가 추가될 수 있도록 Pod 내에 추가 공용 VLAN 방화벽을 배치하여 이를 수행할 수 있습니다.

## 각 방화벽 제품에 포함된 VPN 옵션은 무엇입니까?
{:faq}

모든 방화벽이 VPN을 제공하는 것은 아니며 모든 VPN 옵션이 동일하지도 않습니다. VPN에 대한 일반 옵션은 다음과 같습니다.

* 각 고객이 당사 사설 네트워크에 대한 무제한 SSL VPN 연결을 수신합니다. 이러한 연결은 고객 포털에 로그인한 동안 페이지의 맨 위에 있는 VPN 링크를 클릭하여 설정할 수 있습니다.
* 고객이 계정당 하나의 PPTP VPN을 수신합니다. 매월 5달러의 추가 요금을 지불하면 다섯 개 한 묶음의 계정에 대해 추가적으로 PPTP VPN 사용자를 추가할 수 있습니다.
* IBM Cloud 또한 기본 멀티-테넌트 IPSec VPN 서비스를 제공합니다.
* FortiGate Security Appliance 1Gbps는 공용 네트워크 액세스만 가능한 SSL 및 IPSec VPN 옵션을 제공합니다(IBM Cloud 사설 네트워크에 대한 액세스 불가).
* 네트워크 게이트웨이는 공용 또는 사설 네트워크에 대한 SSL, IPSec 및 OpenVPN 기능을 제공합니다.
* NetScaler 제품은 공용 또는 사설 네트워크에 대한 SSL 및 IPSec VPN을 제공할 수 있습니다.
* 또한 고객이 IBM Cloud 환경 내의 서버에 VPN 솔루션을 배치할 수 있습니다.

## 고가용성 옵션을 선택한 경우, 이 기능을 활용하기 위해 수행해야 하는 단계는 무엇입니까?
{:faq}

없음. HA로 주문한 경우 IBM Cloud가 자동으로 HA 구성에서 어플라이언스를 프로비저닝합니다.  1차 디바이스가 실패하는 경우 2차 수동 디바이스가 1차 활성 인스턴스를 대체하여 트래픽 전달을 시작합니다. 일반적으로 이 장애 복구는 자동으로 발생하므로 서버를 모니터링하고 트래픽이 성공적으로 전달되는지 확인하는 것이 최선입니다.

## 공용 대 사설 NAT 및/또는 사설 VLAN 세그먼트화를 지원하는 방화벽 제품은 무엇입니까?
{:faq}

Hardware Firewall 제품 중 사설 네트워크에 대한 액세스 권한이 있는 제품은 없습니다.  이러한 인라인 기능을 제공하려면 네트워크 게이트웨이가 필요하며 NetScaler 제품이 퍼블릭 및 사설 네트워크에 둘 다에 대한 액세스 권한을 가집니다.
