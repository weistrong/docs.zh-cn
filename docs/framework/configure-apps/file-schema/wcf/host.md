---
description: 了解详细信息： <host>
title: <host>
ms.date: 03/30/2017
ms.assetid: be566d55-9d50-4b2e-985d-52a5cc26cbbb
ms.openlocfilehash: ff240c85af3aab7c1208a6a49b1943f3c6a8cd99
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802276"
---
# \<host>

<span data-ttu-id="23561-102">指定服务主机的设置。</span><span class="sxs-lookup"><span data-stu-id="23561-102">Specifies settings for a service host.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<services>**](services.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<service>**](service.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<host>**  
  
## <a name="syntax"></a><span data-ttu-id="23561-103">语法</span><span class="sxs-lookup"><span data-stu-id="23561-103">Syntax</span></span>  
  
```xml  
<host>
  <baseAddresses>
    <add baseAddress="string" />
  </baseAddresses>
  <timeOuts closeTimeout="TimeSpan"
            openTimeout="TimeSpan" />
</host>
```  
  
## <a name="type"></a><span data-ttu-id="23561-104">类型</span><span class="sxs-lookup"><span data-stu-id="23561-104">Type</span></span>  

 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="23561-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="23561-105">Attributes and Elements</span></span>  

 <span data-ttu-id="23561-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="23561-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="23561-107">特性</span><span class="sxs-lookup"><span data-stu-id="23561-107">Attributes</span></span>  

 <span data-ttu-id="23561-108">无。</span><span class="sxs-lookup"><span data-stu-id="23561-108">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="23561-109">子元素</span><span class="sxs-lookup"><span data-stu-id="23561-109">Child Elements</span></span>  
  
|<span data-ttu-id="23561-110">元素</span><span class="sxs-lookup"><span data-stu-id="23561-110">Element</span></span>|<span data-ttu-id="23561-111">说明</span><span class="sxs-lookup"><span data-stu-id="23561-111">Description</span></span>|  
|-------------|-----------------|  
|[\<baseAddresses>](baseaddresses.md)|<span data-ttu-id="23561-112">`baseAddress` 元素的集合，指定服务主机所使用的基址。</span><span class="sxs-lookup"><span data-stu-id="23561-112">A collection of `baseAddress` elements that specifies the base addresses used by the service host.</span></span>|  
|[\<timeOuts>](timeouts.md)|<span data-ttu-id="23561-113">一个配置元素，指定为打开或关闭服务主机预留的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="23561-113">A configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="23561-114">父元素</span><span class="sxs-lookup"><span data-stu-id="23561-114">Parent Elements</span></span>  
  
|<span data-ttu-id="23561-115">元素</span><span class="sxs-lookup"><span data-stu-id="23561-115">Element</span></span>|<span data-ttu-id="23561-116">说明</span><span class="sxs-lookup"><span data-stu-id="23561-116">Description</span></span>|  
|-------------|-----------------|  
|[\<service>](service.md)|<span data-ttu-id="23561-117">指定 Windows Communication Foundation (WCF) 服务的设置。</span><span class="sxs-lookup"><span data-stu-id="23561-117">Specifies the settings for a Windows Communication Foundation (WCF) service.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="23561-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="23561-118">See also</span></span>

- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- [<span data-ttu-id="23561-119">承载</span><span class="sxs-lookup"><span data-stu-id="23561-119">Hosting</span></span>](../../../wcf/feature-details/hosting.md)
