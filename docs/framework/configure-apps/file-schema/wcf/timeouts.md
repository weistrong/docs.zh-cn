---
description: 了解详细信息： <timeOuts>
title: <timeOuts>
ms.date: 03/30/2017
ms.assetid: 7fccd436-b326-48ec-8de1-c16817a09e0d
ms.openlocfilehash: 097569d1742f6486ddfb5fb3c3d98ba106424f45
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786585"
---
# \<timeOuts>

<span data-ttu-id="3f499-102">表示一个配置元素，该元素指定允许服务主机打开或关闭的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="3f499-102">Represents a configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<services>**](services.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<service>**](service.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<host>**](host.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<timeOuts>**  
  
## <a name="syntax"></a><span data-ttu-id="3f499-103">语法</span><span class="sxs-lookup"><span data-stu-id="3f499-103">Syntax</span></span>  
  
```xml  
<timeOuts closeTimeout="TimeSpan"
          openTimeout="TimeSpan" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3f499-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="3f499-104">Attributes and Elements</span></span>  

 <span data-ttu-id="3f499-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3f499-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3f499-106">特性</span><span class="sxs-lookup"><span data-stu-id="3f499-106">Attributes</span></span>  
  
|<span data-ttu-id="3f499-107">属性</span><span class="sxs-lookup"><span data-stu-id="3f499-107">Attribute</span></span>|<span data-ttu-id="3f499-108">说明</span><span class="sxs-lookup"><span data-stu-id="3f499-108">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="3f499-109">一个 <xref:System.TimeSpan> 值，指定为关闭服务主机预留的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="3f499-109">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to close.</span></span>|  
|`openTimeout`|<span data-ttu-id="3f499-110">一个 <xref:System.TimeSpan> 值，指定为打开或关闭服务主机预留的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="3f499-110">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to open.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3f499-111">子元素</span><span class="sxs-lookup"><span data-stu-id="3f499-111">Child Elements</span></span>  

 <span data-ttu-id="3f499-112">无。</span><span class="sxs-lookup"><span data-stu-id="3f499-112">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3f499-113">父元素</span><span class="sxs-lookup"><span data-stu-id="3f499-113">Parent Elements</span></span>  
  
|<span data-ttu-id="3f499-114">元素</span><span class="sxs-lookup"><span data-stu-id="3f499-114">Element</span></span>|<span data-ttu-id="3f499-115">说明</span><span class="sxs-lookup"><span data-stu-id="3f499-115">Description</span></span>|  
|-------------|-----------------|  
|[\<host>](host.md)|<span data-ttu-id="3f499-116">一个指定服务主机设置的配置元素。</span><span class="sxs-lookup"><span data-stu-id="3f499-116">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3f499-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="3f499-117">See also</span></span>

- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- [<span data-ttu-id="3f499-118">承载</span><span class="sxs-lookup"><span data-stu-id="3f499-118">Hosting</span></span>](../../../wcf/feature-details/hosting.md)
