---

copyright:
  years: 2017
lastupdated: "2018-11-12"

keywords: bypass, firewall, enable

subcollection: fortigate-1g

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Bypassing the Firewall
{: #bypassing-the-firewall}

To bypass the firewall, perform the following procedure:

1. From your browser, open  [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} and log into your account.
2. In the Customer Portal navigation, go to **Network > IP Management > VLANs** and click on the firewall device you want to bypass.
3. In the **Device Details** page, you can use the **Actions** drop down menu to choose **Set Route Bypass** or in the **Status:** section, you can click on the **Route Around** button. Either way, you should get a confirmation dialog. Click **Yes** to confirm the action. Bypassing the route takes approximately two minutes to take effect. While in bypass mode, the "Status" will be "Routing AROUND firewall".

## Unbypass the Firewall
{: #unbypass-the-firewall}

To route the public network traffic back to the firewall, follow the instructions above to reach the **Configuration** tab of the device and click on the **Actions** dropdown menu and choose **Set Route Bypass** or in the **Status:** section, you can click on the **Route Through** button. You will get a confirmation dialog. Click **Yes** to confirm the action. The "Status" will change back to "Routing THROUGH firewall" within two minutes.
