---
description: 了解详细信息： <bufferReceive>
title: <bufferReceive>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: b23c3a54-10d4-4f13-ab6d-98b26b76f22a
ms.openlocfilehash: 8f5e58e0e72a81d8b3a20a68e0890be907c20d2b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698084"
---
# \<bufferReceive>

<span data-ttu-id="591a9-102">一种服务行为，允许服务使用缓冲接收处理，以使工作流服务能够处理无序消息。</span><span class="sxs-lookup"><span data-stu-id="591a9-102">A service behavior that enables a service to use buffered receive processing, which enables a workflow service to process out-of-order messages.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<bufferReceive>**  
  
## <a name="syntax"></a><span data-ttu-id="591a9-103">语法</span><span class="sxs-lookup"><span data-stu-id="591a9-103">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <bufferReceive maxPendingMessagesPerChannel="Integer" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="591a9-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="591a9-104">Attributes and Elements</span></span>  

 <span data-ttu-id="591a9-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="591a9-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="591a9-106">特性</span><span class="sxs-lookup"><span data-stu-id="591a9-106">Attributes</span></span>  
  
|<span data-ttu-id="591a9-107">属性</span><span class="sxs-lookup"><span data-stu-id="591a9-107">Attribute</span></span>|<span data-ttu-id="591a9-108">说明</span><span class="sxs-lookup"><span data-stu-id="591a9-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="591a9-109">maxPendingMessagesPerChannel</span><span class="sxs-lookup"><span data-stu-id="591a9-109">maxPendingMessagesPerChannel</span></span>|<span data-ttu-id="591a9-110">一个整数，指定每个通道允许的最大挂起消息数。</span><span class="sxs-lookup"><span data-stu-id="591a9-110">An integer that specifies the maximum number of pending messages allowed for each channel.</span></span> <span data-ttu-id="591a9-111">默认值为 512。</span><span class="sxs-lookup"><span data-stu-id="591a9-111">The default value is 512.</span></span> <span data-ttu-id="591a9-112">此属性限制工作流服务可接收的无序消息数。</span><span class="sxs-lookup"><span data-stu-id="591a9-112">This property limits the number of out-of-order messages that can be received by a workflow service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="591a9-113">子元素</span><span class="sxs-lookup"><span data-stu-id="591a9-113">Child Elements</span></span>  

 <span data-ttu-id="591a9-114">无。</span><span class="sxs-lookup"><span data-stu-id="591a9-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="591a9-115">父元素</span><span class="sxs-lookup"><span data-stu-id="591a9-115">Parent Elements</span></span>  
  
|<span data-ttu-id="591a9-116">元素</span><span class="sxs-lookup"><span data-stu-id="591a9-116">Element</span></span>|<span data-ttu-id="591a9-117">说明</span><span class="sxs-lookup"><span data-stu-id="591a9-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="591a9-118">\<serviceBehaviors> 的 \<behavior></span><span class="sxs-lookup"><span data-stu-id="591a9-118">\<behavior> of \<serviceBehaviors></span></span>](behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="591a9-119">指定行为元素。</span><span class="sxs-lookup"><span data-stu-id="591a9-119">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="591a9-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="591a9-120">See also</span></span>

- <xref:System.ServiceModel.Activities.Description.BufferedReceiveServiceBehavior>
- <xref:System.ServiceModel.Activities.Configuration.BufferedReceiveElement>
