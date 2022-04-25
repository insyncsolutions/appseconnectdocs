---
title: "Overview"
toc: true
tag: developers
category: "Deployment"
menus:
    deployment: 
        icon: fa fa-gg
        weight: 15
        title: "OverView"
        identifier: upgradationmigration              
---





Deployment primarly talks about APPSeCONNECT Agent which is your own on-premises tool which needs to be installed on your own server to start doing the actual sync operation.




## Hostnames and URLs of APPSeCONNECT

In addtion to secured connectivity, APPSeCONNECT requires a number of URLS and Ports for deploying
it on your environment for seemless connection between the agent and our cloud portal. 
|Destination|Url|Purpose|
|---|---|---|
|The Platform|[https://portal.appseconnect.com](https://portal.appseconnect.com)|The main portal where integration developer does every configuration.  iPaaS Platform.|
|The API|[https://admin.appseconnect.com](https://admin.appseconnect.com)|The API stack which is used to download User info and customer metadata.|
|Storage|[https://appsdrive.blob.core.windows.net/](https://appsdrive.blob.core.windows.net)|Represents configuration store, where most of the configuration created in Platform is stored.|
|Storage|[https://appsdatalake.blob.core.windows.net/](https://appsdatalake.blob.core.windows.net/)|Represents transactional store, where all metadata related to sync is uploaded.|
|Service Bus|[https://aec-prod.servicebus.windows.net ](https://aec-prod.servicebus.windows.net)|In Memory event hub, which tracks of any important event raised on the agent. It also uses _sb:\\_ protocol to communicate|
|Service Bus|[https://appseconnect.servicebus.windows.net](https://appseconnect.servicebus.windows.net)|Hook for Service bus, required to execute real-time proxies. Service Bus represents a brokered service communication architecture. It also uses _sb:\\_  protocol to communicate|
|SignalR Server|[https://services.appseconnect.com ](https://services.appseconnect.com/signalr)|Represents the real-time communication channel for web sockets. The Agent connects to the socket using _wss:\\_ protocol to the service.|
|Document Database|[https://aecprod.documents.azure.com/ ](https://aecprod.documents.azure.com/)|APPSeCONNECT document database, which is used by new Process flow engine.|
|Realtime Proxy URL|[https://(subdomain).appseconnectapi.com/](https://(subdomain).appseconnectapi.com/)|The Realtime communication channel is created to post messages to the agent in real-time. This url needs to be configured on application webhook such that the data could be passed in the url. The subdomain here is configured by the customer.|

**NOTE: We also require you to keep some of the Ports Open for APPSeCONNECT**     

# Real-Time Touchpoints
It is highly recommended to use Proxy to configure real-time configurations, but if you still require to communicate using local server’s public IP, you need to exempt 80 port of that machine, such that local port could be correctly opened. The port and the URL could be configured in settings of APPSeCONNECT agent or from Portal.

For proxy or API management, the URL will be in *.appseconnectapi.com format. The * is the subdomain chosen by the customer


# Ports For Exemption
In addition to these URLs, we also need local ports to be opened as follows:

- APPSeCONNECT Agent opens a listener at Port : 59050
- APPSeCONNECT Service opens a listener at Port : 59051

These ports need to be exempted from the firewall such that the Inter-process communication between the service and the local agent application could be made.

All communications are through HTTPS (256 BIT Encrypted) only.

**ProTip:** In any circumstance if you see OP Agent is in disabled state after meeting all the installation
criteria, ensure to check that FIPS (Federal Information Processing Standard) is disabled in that system/machine to enable the OP Agent.
{: .notice--info}

**Steps to FIPS Disablement is given in this [link](https://community.appseconnect.com/story-of-fips-and-appseconnect/)**

 