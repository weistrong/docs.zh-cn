---
description: 了解详细信息： <allowAccounts>
title: <allowAccounts>
ms.date: 03/30/2017
ms.assetid: 166923a9-a8ac-478f-92f9-529d9667f3a6
ms.openlocfilehash: 5211d694e5318faf0cfc31b404764acb405bd096
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749982"
---
# \<allowAccounts>

<span data-ttu-id="1f5f9-102">包含一个配置元素的集合，这些元素为承载 Windows Communication Foundation (WCF) 服务并向其授予对共享服务的连接访问权限的进程指定用户帐户。</span><span class="sxs-lookup"><span data-stu-id="1f5f9-102">Contains a collection of configuration elements that specify user accounts for processes that host Windows Communication Foundation (WCF) services, and are granted connection access to the sharing service.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel.activation>**](system-servicemodel-activation.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<net.pipe>**](net-pipe.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<allowAccounts>**  
  
## <a name="syntax"></a><span data-ttu-id="1f5f9-103">语法</span><span class="sxs-lookup"><span data-stu-id="1f5f9-103">Syntax</span></span>  
  
```xml  
<allowAccounts>
  <add securityIdentifier="String" />
</allowAccounts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1f5f9-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1f5f9-104">Attributes and Elements</span></span>  

 <span data-ttu-id="1f5f9-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1f5f9-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1f5f9-106">特性</span><span class="sxs-lookup"><span data-stu-id="1f5f9-106">Attributes</span></span>  

 <span data-ttu-id="1f5f9-107">无。</span><span class="sxs-lookup"><span data-stu-id="1f5f9-107">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="1f5f9-108">子元素</span><span class="sxs-lookup"><span data-stu-id="1f5f9-108">Child Elements</span></span>  
  
|<span data-ttu-id="1f5f9-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="1f5f9-109">Attribute</span></span>|<span data-ttu-id="1f5f9-110">说明</span><span class="sxs-lookup"><span data-stu-id="1f5f9-110">Description</span></span>|  
|---------------|-----------------|  
|[\<add>](add-of-allowaccounts.md)|<span data-ttu-id="1f5f9-111">为承载 WCF 服务且被授予对共享服务的连接访问权限的进程添加用户帐户</span><span class="sxs-lookup"><span data-stu-id="1f5f9-111">Adds a user account for processes that host WCF services, and are granted connection access to the sharing service</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1f5f9-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1f5f9-112">Parent Elements</span></span>  
  
|<span data-ttu-id="1f5f9-113">元素</span><span class="sxs-lookup"><span data-stu-id="1f5f9-113">Element</span></span>|<span data-ttu-id="1f5f9-114">说明</span><span class="sxs-lookup"><span data-stu-id="1f5f9-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1f5f9-115">[\<net.pipe>](net-pipe.md) 或 [\<net.tcp>](net-tcp.md)</span><span class="sxs-lookup"><span data-stu-id="1f5f9-115">[\<net.pipe>](net-pipe.md) or [\<net.tcp>](net-tcp.md)</span></span>|<span data-ttu-id="1f5f9-116">指定 Net Pipe 或 TCP 共享服务的配置设置。</span><span class="sxs-lookup"><span data-stu-id="1f5f9-116">Specifies configuration settings for the Net Pipe or TCP sharing services.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1f5f9-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="1f5f9-117">See also</span></span>

- <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
