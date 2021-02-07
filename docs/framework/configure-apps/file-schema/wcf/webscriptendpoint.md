---
description: 了解详细信息： <webScriptEndpoint>
title: <webScriptEndpoint>
ms.date: 03/30/2017
ms.assetid: 85cb5ecf-351b-45f3-aa29-aa2e4b64bcdd
ms.openlocfilehash: eef4eb8e8e7345492f967c85b6245f733a4c824f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682496"
---
# \<webScriptEndpoint>

<span data-ttu-id="febfd-102">此配置元素定义具有 [\<webHttpBinding>](webhttpbinding.md) 自动添加行为的固定绑定的标准终结点 [\<enableWebScript>](enablewebscript.md) 。</span><span class="sxs-lookup"><span data-stu-id="febfd-102">This configuration element defines a standard endpoint with a fixed [\<webHttpBinding>](webhttpbinding.md) binding that automatically adds the [\<enableWebScript>](enablewebscript.md) behavior.</span></span> <span data-ttu-id="febfd-103">在编写从 ASP.NET AJAX 应用程序中调用的服务时，请使用此终结点。</span><span class="sxs-lookup"><span data-stu-id="febfd-103">Use this endpoint when you are writing a service that is called from an ASP.NET AJAX application.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<standardEndpoints>**](standardendpoints.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<webScriptEndpoint>**  
  
## <a name="syntax"></a><span data-ttu-id="febfd-104">语法</span><span class="sxs-lookup"><span data-stu-id="febfd-104">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <webScriptEndpoint>
      <standardEndpoint webEndpointType="String" />
    </webScriptEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="febfd-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="febfd-105">Attributes and Elements</span></span>  

 <span data-ttu-id="febfd-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="febfd-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="febfd-107">特性</span><span class="sxs-lookup"><span data-stu-id="febfd-107">Attributes</span></span>  
  
|<span data-ttu-id="febfd-108">属性</span><span class="sxs-lookup"><span data-stu-id="febfd-108">Attribute</span></span>|<span data-ttu-id="febfd-109">说明</span><span class="sxs-lookup"><span data-stu-id="febfd-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="febfd-110">webEndpointType</span><span class="sxs-lookup"><span data-stu-id="febfd-110">webEndpointType</span></span>|<span data-ttu-id="febfd-111">一个字符串，指定终结点的类型。</span><span class="sxs-lookup"><span data-stu-id="febfd-111">A string that specifies the type of the endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="febfd-112">子元素</span><span class="sxs-lookup"><span data-stu-id="febfd-112">Child Elements</span></span>  

 <span data-ttu-id="febfd-113">无。</span><span class="sxs-lookup"><span data-stu-id="febfd-113">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="febfd-114">父元素</span><span class="sxs-lookup"><span data-stu-id="febfd-114">Parent Elements</span></span>  
  
|<span data-ttu-id="febfd-115">元素</span><span class="sxs-lookup"><span data-stu-id="febfd-115">Element</span></span>|<span data-ttu-id="febfd-116">说明</span><span class="sxs-lookup"><span data-stu-id="febfd-116">Description</span></span>|  
|-------------|-----------------|  
|[\<standardEndpoints>](standardendpoints.md)|<span data-ttu-id="febfd-117">具有一个或多个固定属性（地址、绑定和协定）的预定义终结点的标准终结点集合。</span><span class="sxs-lookup"><span data-stu-id="febfd-117">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="febfd-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="febfd-118">See also</span></span>

- <xref:System.ServiceModel.Description.WebScriptEndpoint>
- <xref:System.ServiceModel.Configuration.WebScriptEndpointElement>
