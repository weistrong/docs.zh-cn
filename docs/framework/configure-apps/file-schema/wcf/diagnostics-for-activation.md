---
description: 了解详细信息： <diagnostics> 激活
title: <diagnostics> 用于激活
ms.date: 03/30/2017
ms.assetid: 1486e0eb-fe2a-46c3-b584-c924889477dd
ms.openlocfilehash: aa1529a478ac367ea89c8926571c6c6f2f57cf74
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698357"
---
# <a name="diagnostics-for-activation"></a><span data-ttu-id="0636c-103">\<diagnostics> 用于激活</span><span class="sxs-lookup"><span data-stu-id="0636c-103">\<diagnostics> for Activation</span></span>

<span data-ttu-id="0636c-104">配置 Windows Communication Foundation (WCF) 侦听器的诊断功能。</span><span class="sxs-lookup"><span data-stu-id="0636c-104">Configures Windows Communication Foundation (WCF) listener's diagnostics functionalities.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel.activation>**](system-servicemodel-activation.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<diagnostics>**  
  
## <a name="syntax"></a><span data-ttu-id="0636c-105">语法</span><span class="sxs-lookup"><span data-stu-id="0636c-105">Syntax</span></span>  
  
```xml  
<configuration>
  <system.serviceModel.activation>
    <diagnostics performanceCountersEnabled="Boolean" />
  </system.serviceModel.activation>
</configuration>
```  
  
## <a name="type"></a><span data-ttu-id="0636c-106">类型</span><span class="sxs-lookup"><span data-stu-id="0636c-106">Type</span></span>  

 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0636c-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="0636c-107">Attributes and Elements</span></span>  

 <span data-ttu-id="0636c-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0636c-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0636c-109">特性</span><span class="sxs-lookup"><span data-stu-id="0636c-109">Attributes</span></span>  
  
|<span data-ttu-id="0636c-110">属性</span><span class="sxs-lookup"><span data-stu-id="0636c-110">Attribute</span></span>|<span data-ttu-id="0636c-111">说明</span><span class="sxs-lookup"><span data-stu-id="0636c-111">Description</span></span>|  
|---------------|-----------------|  
|`performanceCountersEnabled`|<span data-ttu-id="0636c-112">一个布尔值，指示是否启用用于诊断目的的性能计数器。</span><span class="sxs-lookup"><span data-stu-id="0636c-112">A Boolean value that indicates whether performance counters are enabled for diagnostic purposes.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0636c-113">子元素</span><span class="sxs-lookup"><span data-stu-id="0636c-113">Child Elements</span></span>  

 <span data-ttu-id="0636c-114">无。</span><span class="sxs-lookup"><span data-stu-id="0636c-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0636c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="0636c-115">Parent Elements</span></span>  
  
|<span data-ttu-id="0636c-116">元素</span><span class="sxs-lookup"><span data-stu-id="0636c-116">Element</span></span>|<span data-ttu-id="0636c-117">说明</span><span class="sxs-lookup"><span data-stu-id="0636c-117">Description</span></span>|  
|-------------|-----------------|  
|[\<system.serviceModel.activation>](system-servicemodel-activation.md)|<span data-ttu-id="0636c-118">包含侦听器进程 SMSvcHost.exe 的配置设置。</span><span class="sxs-lookup"><span data-stu-id="0636c-118">Contains configuration settings for the listener process SMSvcHost.exe.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0636c-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="0636c-119">See also</span></span>

- <xref:System.ServiceModel.Activation.Configuration.DiagnosticSection>
