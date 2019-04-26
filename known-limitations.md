---

copyright:
  years: 2017
lastupdated: "2018-11-12"

keywords: known, limitations, problems, nlb, fsa

subcollection: fortigate-1g

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:note: .note}
{:important: .important}

# Known Limitations of Fortigate Security Appliance 1Gbps
{: #known-limitations-of-fortigate-security-appliance-1gbps}

The FortiGate Security Appliance (FSA) 1Gbps has the following known limitations:

* Incompatible with Windows Network Load Balancing (NLB) due to the way ARP is processed.

* High Availability failover functionality is not exposed to the user. If the master firewall malfunctions, but does not failover automatically, a support ticket will be required. Device monitoring for critical services is recommended to ensure that firewalls are appropriately passing traffic.

* A FortiGate Security Appliance cannot be deployed on a VLAN that is currently associated with a Network Gateway, Hardware Firewall, or another FortiGate Security Appliance.

* The FortiGate Security Appliance is associated with a single public customer VLAN (the "inside" VLAN) and cannot access the private network.

* Set Rules Bypass does not work on FSA 1Gbps. Set Rules Bypass applies to Hardware Firewall (Standard and Dedicated).
