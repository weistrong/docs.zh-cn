---
description: 了解详细信息： <System.servicemodel>
title: < system.serviceModel.activation >
ms.date: 03/30/2017
ms.assetid: c0cae85f-56cb-4030-8807-6f96edff8d2d
ms.openlocfilehash: 4da87248426f5da3c53a03d5f307a174b2b0dfc7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682600"
---
# \<system.serviceModel.activation>

<span data-ttu-id="56a42-103">此配置节描述了 SMSvcHost.exe 工具的配置设置。</span><span class="sxs-lookup"><span data-stu-id="56a42-103">This configuration section represents the configuration settings for the SMSvcHost.exe tool.</span></span> <span data-ttu-id="56a42-104">配置元素可在 SMSvcHost.exe.config 文件中配置。</span><span class="sxs-lookup"><span data-stu-id="56a42-104">The configuration elements can be configured in the SMSvcHost.exe.config file.</span></span> <span data-ttu-id="56a42-105">具体地说，它包括计算机中所有必须配置的设置。</span><span class="sxs-lookup"><span data-stu-id="56a42-105">Specifically, it includes all machine-wide settings that must be configured.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;**\<system.serviceModel.activation>**  
  
## <a name="sample-configuration-file"></a><span data-ttu-id="56a42-106">示例配置文件</span><span class="sxs-lookup"><span data-stu-id="56a42-106">Sample Configuration File</span></span>  

 <span data-ttu-id="56a42-107">下面是侦听器进程 SMSvcHost.exe 所使用的示例配置文件 (SMSvcHost.exe.config)。</span><span class="sxs-lookup"><span data-stu-id="56a42-107">The following is a sample configuration file (SMSvcHost.exe.config), which is used by the listener process SMSvcHost.exe.</span></span>  
  
```xml  
<configuration>
  <runtime>
    <gcConcurrent enabled="false" />
  </runtime>
  <system.serviceModel.activation>
    <net.tcp listenBacklog="10"
             maxPendingAccepts="2"
             maxPendingConnections="100"
             receiveTimeout="00:00:10"
             teredoEnabled="false">
      <allowAccounts>
        <!-- LocalSystem account -->
        <add securityIdentifier="S-1-5-18"/>
        <!-- LocalService account -->
        <add securityIdentifier="S-1-5-19"/>
        <!-- Network Service account -->
        <add securityIdentifier="S-1-5-20"/>
        <!-- Administrators account -->
        <add securityIdentifier="S-1-5-32-544" />
        <!-- IIS_IUSRS account (Vista only) -->
        <add securityIdentifier="S-1-5-32-568"/>
      </allowAccounts>
    </net.tcp>
    <net.pipe maxConnectionsPendingDispatch="100"
              maxPendingAccepts="2"
              receiveTimeout="00:00:10">
      <allowAccounts>
        <!-- LocalSystem account -->
        <add securityIdentifier="S-1-5-18" />
        <!-- LocalService account -->
        <add securityIdentifier="S-1-5-19" />
        <!-- Network Service account -->
        <add securityIdentifier="S-1-5-20" />
        <!-- Administrators account -->
        <add securityIdentifier="S-1-5-32-544" />
        <!-- IIS_IUSRS account (Vista only) -->
        <add securityIdentifier="S-1-5-32-568" />
      </allowAccounts>
    </net.pipe>
    <diagnostics performanceCountersEnabled="true" />
  </system.serviceModel.activation>
</configuration>
```  
  
## <a name="see-also"></a><span data-ttu-id="56a42-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="56a42-108">See also</span></span>

- <xref:System.ServiceModel.Activation.Configuration>
