---
description: 了解详细信息： <backupLists>
title: <backupLists>
ms.date: 03/30/2017
ms.assetid: 593b3390-f65b-4684-ad40-0596b62f0954
ms.openlocfilehash: 9647c507f85eba6bfd001b34dbf617bc881d3f2e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749696"
---
# \<backupLists>

<span data-ttu-id="c8c34-102">表示一个配置节，用于定义一组用来处理错误的备份服务。</span><span class="sxs-lookup"><span data-stu-id="c8c34-102">Represents a configuration section for defining a set of backup services used in error handling.</span></span> <span data-ttu-id="c8c34-103">每个子元素都是一个备份列表，用于枚举当无法到达主终结点时路由服务将使用的一组终结点。</span><span class="sxs-lookup"><span data-stu-id="c8c34-103">Each child element is a backup list that enumerates a set of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span> <span data-ttu-id="c8c34-104">如果列表中的第一个终结点关闭，则路由服务会自动故障转移到列表中的下一个终结点。</span><span class="sxs-lookup"><span data-stu-id="c8c34-104">If the first endpoint in the list is down, the Routing Service will automatically fail-over to the next one in the list.</span></span>  <span data-ttu-id="c8c34-105">这样，可以方便地提高应用程序的可靠性，而不必告诉客户端应用程序应如何处理复杂模式或所有服务的部署位置。</span><span class="sxs-lookup"><span data-stu-id="c8c34-105">This gives you a quick way to add reliability to your application without having to teach your client application how to handle complex patterns or where all of your services are deployed.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<routing>**](routing.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<backupLists>**  
  
## <a name="syntax"></a><span data-ttu-id="c8c34-106">语法</span><span class="sxs-lookup"><span data-stu-id="c8c34-106">Syntax</span></span>  
  
```xml  
<routing>
  <backupLists>
    <backupList name="String">
      <add endpointName="String" />
    </backupList>
  </backupLists>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c8c34-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="c8c34-107">Attributes and Elements</span></span>  

 <span data-ttu-id="c8c34-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c8c34-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c8c34-109">特性</span><span class="sxs-lookup"><span data-stu-id="c8c34-109">Attributes</span></span>  

 <span data-ttu-id="c8c34-110">无。</span><span class="sxs-lookup"><span data-stu-id="c8c34-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="c8c34-111">子元素</span><span class="sxs-lookup"><span data-stu-id="c8c34-111">Child Elements</span></span>  
  
|<span data-ttu-id="c8c34-112">元素</span><span class="sxs-lookup"><span data-stu-id="c8c34-112">Element</span></span>|<span data-ttu-id="c8c34-113">说明</span><span class="sxs-lookup"><span data-stu-id="c8c34-113">Description</span></span>|  
|-------------|-----------------|  
|[\<filter>](filter.md)|<span data-ttu-id="c8c34-114">包含当无法访问主终结点时路由服务将使用的终结点的列表。</span><span class="sxs-lookup"><span data-stu-id="c8c34-114">Contains a list of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span> <span data-ttu-id="c8c34-115">.</span><span class="sxs-lookup"><span data-stu-id="c8c34-115">.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c8c34-116">父元素</span><span class="sxs-lookup"><span data-stu-id="c8c34-116">Parent Elements</span></span>  
  
|<span data-ttu-id="c8c34-117">元素</span><span class="sxs-lookup"><span data-stu-id="c8c34-117">Element</span></span>|<span data-ttu-id="c8c34-118">说明</span><span class="sxs-lookup"><span data-stu-id="c8c34-118">Description</span></span>|  
|-------------|-----------------|  
|[\<routing>](routing.md)|<span data-ttu-id="c8c34-119">表示用于定义一组路由筛选器的配置节，这些筛选器确定计算传入消息时要使用的 Windows Communication Foundation 的类型 (WCF) ，以及用于 <xref:System.ServiceModel.Dispatcher.MessageFilter> 定义筛选器匹配时要将消息发送到的目标终结点的路由表。</span><span class="sxs-lookup"><span data-stu-id="c8c34-119">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c8c34-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="c8c34-120">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.BackupEndpointCollection?displayProperty=nameWithType>
