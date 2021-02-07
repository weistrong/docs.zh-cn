---
description: 了解详细信息： <workflowControlEndpoint>
title: <workflowControlEndpoint>
ms.date: 03/30/2017
ms.assetid: 6c89e76c-643b-4b6a-9b25-628f753d7027
ms.openlocfilehash: 5205edf159bd947531231e69fd23f6cdf9c77d2d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682340"
---
# \<workflowControlEndpoint>

<span data-ttu-id="8d999-102">此配置元素定义用于控制工作流实例的执行（创建、运行、挂起、终止等）的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8d999-102">This configuration element defines a standard endpoint for controlling the execution of workflow instances (create, run, suspend, terminate, etc).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<standardEndpoints>**](standardendpoints.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<workflowControlEndpoint>**  
  
## <a name="syntax"></a><span data-ttu-id="8d999-103">语法</span><span class="sxs-lookup"><span data-stu-id="8d999-103">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <workflowControlEndpoint>
      <standardEndpoint name="String" />
    </workflowControlEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8d999-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="8d999-104">Attributes and Elements</span></span>  

 <span data-ttu-id="8d999-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8d999-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8d999-106">特性</span><span class="sxs-lookup"><span data-stu-id="8d999-106">Attributes</span></span>  
  
|<span data-ttu-id="8d999-107">属性</span><span class="sxs-lookup"><span data-stu-id="8d999-107">Attribute</span></span>|<span data-ttu-id="8d999-108">说明</span><span class="sxs-lookup"><span data-stu-id="8d999-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8d999-109">name</span><span class="sxs-lookup"><span data-stu-id="8d999-109">name</span></span>|<span data-ttu-id="8d999-110">一个字符串，指定标准终结点的配置的名称。</span><span class="sxs-lookup"><span data-stu-id="8d999-110">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="8d999-111">此名称在服务终结点的 `endpointConfiguration` 特性中用于将标准终结点链接到其配置。</span><span class="sxs-lookup"><span data-stu-id="8d999-111">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8d999-112">子元素</span><span class="sxs-lookup"><span data-stu-id="8d999-112">Child Elements</span></span>  

 <span data-ttu-id="8d999-113">无。</span><span class="sxs-lookup"><span data-stu-id="8d999-113">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8d999-114">父元素</span><span class="sxs-lookup"><span data-stu-id="8d999-114">Parent Elements</span></span>  
  
|<span data-ttu-id="8d999-115">元素</span><span class="sxs-lookup"><span data-stu-id="8d999-115">Element</span></span>|<span data-ttu-id="8d999-116">说明</span><span class="sxs-lookup"><span data-stu-id="8d999-116">Description</span></span>|  
|-------------|-----------------|  
|[\<standardEndpoints>](standardendpoints.md)|<span data-ttu-id="8d999-117">具有一个或多个固定属性（地址、绑定和协定）的预定义终结点的标准终结点集合。</span><span class="sxs-lookup"><span data-stu-id="8d999-117">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8d999-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="8d999-118">See also</span></span>

- <xref:System.ServiceModel.Activities.WorkflowControlEndpoint>
