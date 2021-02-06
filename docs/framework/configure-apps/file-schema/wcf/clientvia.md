---
description: 了解详细信息： <clientVia>
title: <clientVia>
ms.date: 03/30/2017
ms.assetid: c27ee94e-babd-459b-9574-2a6d67d11314
ms.openlocfilehash: 651af0c310504f7672ca172d7df609365c319506
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638765"
---
# \<clientVia>

<span data-ttu-id="46269-102">指定应为其创建传输通道的 URI。</span><span class="sxs-lookup"><span data-stu-id="46269-102">Specifies the URI for which the transport channel should be created.</span></span> <span data-ttu-id="46269-103">有关详细信息，请参阅 <xref:System.ServiceModel.Description.ClientViaBehavior>。</span><span class="sxs-lookup"><span data-stu-id="46269-103">For more information, see <xref:System.ServiceModel.Description.ClientViaBehavior>.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<clientVia>**  
  
## <a name="syntax"></a><span data-ttu-id="46269-104">语法</span><span class="sxs-lookup"><span data-stu-id="46269-104">Syntax</span></span>  
  
```xml  
<clientVia viaUri="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="46269-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="46269-105">Attributes and Elements</span></span>  

 <span data-ttu-id="46269-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="46269-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="46269-107">特性</span><span class="sxs-lookup"><span data-stu-id="46269-107">Attributes</span></span>  
  
|<span data-ttu-id="46269-108">属性</span><span class="sxs-lookup"><span data-stu-id="46269-108">Attribute</span></span>|<span data-ttu-id="46269-109">说明</span><span class="sxs-lookup"><span data-stu-id="46269-109">Description</span></span>|  
|---------------|-----------------|  
|`viaUri`|<span data-ttu-id="46269-110">一个指定 URI 的字符串，此 URI 指示消息应采用的路由。</span><span class="sxs-lookup"><span data-stu-id="46269-110">A string that specifies a URI that indicates the route a message should take.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="46269-111">子元素</span><span class="sxs-lookup"><span data-stu-id="46269-111">Child Elements</span></span>  

 <span data-ttu-id="46269-112">无</span><span class="sxs-lookup"><span data-stu-id="46269-112">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="46269-113">父元素</span><span class="sxs-lookup"><span data-stu-id="46269-113">Parent Elements</span></span>  
  
|<span data-ttu-id="46269-114">元素</span><span class="sxs-lookup"><span data-stu-id="46269-114">Element</span></span>|<span data-ttu-id="46269-115">说明</span><span class="sxs-lookup"><span data-stu-id="46269-115">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="46269-116">指定终结点行为。</span><span class="sxs-lookup"><span data-stu-id="46269-116">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="46269-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="46269-117">See also</span></span>

- <xref:System.ServiceModel.Configuration.ClientViaElement>
- <xref:System.ServiceModel.Description.ClientViaBehavior>
