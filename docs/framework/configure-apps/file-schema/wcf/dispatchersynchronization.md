---
description: 了解详细信息： <dispatcherSynchronization>
title: <dispatcherSynchronization>
ms.date: 03/30/2017
ms.assetid: cc030f9c-4e38-4b14-94dc-9a0e41ec8e2d
ms.openlocfilehash: 93664dec3648ed58df7e3e5c0760f1694c60ba7e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749597"
---
# \<dispatcherSynchronization>
  
<span data-ttu-id="8ebc2-102">指定允许服务进行异步答复的终结点行为。</span><span class="sxs-lookup"><span data-stu-id="8ebc2-102">Specifies an endpoint behavior that enables a service to send replies asynchronously.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<dispatcherSynchronization>**  
  
## <a name="syntax"></a><span data-ttu-id="8ebc2-103">语法</span><span class="sxs-lookup"><span data-stu-id="8ebc2-103">Syntax</span></span>  
  
```xml  
<dispatcherSynchronizationBehavior asynchronousSendEnabled="Boolean"
                                   maxPendingReceives="Integer" />
```  
  
## <a name="type"></a><span data-ttu-id="8ebc2-104">类型</span><span class="sxs-lookup"><span data-stu-id="8ebc2-104">Type</span></span>  
  
`Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8ebc2-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="8ebc2-105">Attributes and elements</span></span>  
  
<span data-ttu-id="8ebc2-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8ebc2-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8ebc2-107">特性</span><span class="sxs-lookup"><span data-stu-id="8ebc2-107">Attributes</span></span>

| <span data-ttu-id="8ebc2-108">属性</span><span class="sxs-lookup"><span data-stu-id="8ebc2-108">Attribute</span></span>               | <span data-ttu-id="8ebc2-109">说明</span><span class="sxs-lookup"><span data-stu-id="8ebc2-109">Description</span></span>       |
| ----------------------- | ----------------- |
| <span data-ttu-id="8ebc2-110">asynchronousSendEnabled</span><span class="sxs-lookup"><span data-stu-id="8ebc2-110">asynchronousSendEnabled</span></span> | <span data-ttu-id="8ebc2-111">一个布尔值，指定是否启用异步发送行为。</span><span class="sxs-lookup"><span data-stu-id="8ebc2-111">A Boolean that specifies whether asynchronous send behavior is enabled.</span></span> |
| `maxPendingReceives`    | <span data-ttu-id="8ebc2-112">一个整数，指定可在每个通道上执行的并发接收数。</span><span class="sxs-lookup"><span data-stu-id="8ebc2-112">An integer that specifies the number of concurrent receives that can be issued on the channel.</span></span><br /><br /> <span data-ttu-id="8ebc2-113">仅当已正确配置服务限制行为之后，才能配置此值。</span><span class="sxs-lookup"><span data-stu-id="8ebc2-113">This value should be configured only after you have properly configured service throttling behavior.</span></span> |

### <a name="child-elements"></a><span data-ttu-id="8ebc2-114">子元素</span><span class="sxs-lookup"><span data-stu-id="8ebc2-114">Child elements</span></span>

<span data-ttu-id="8ebc2-115">无。</span><span class="sxs-lookup"><span data-stu-id="8ebc2-115">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="8ebc2-116">父元素</span><span class="sxs-lookup"><span data-stu-id="8ebc2-116">Parent elements</span></span>

| <span data-ttu-id="8ebc2-117">元素</span><span class="sxs-lookup"><span data-stu-id="8ebc2-117">Element</span></span> | <span data-ttu-id="8ebc2-118">说明</span><span class="sxs-lookup"><span data-stu-id="8ebc2-118">Description</span></span> |  
| ------- | ----------- |  
| [\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="8ebc2-119">指定终结点行为。</span><span class="sxs-lookup"><span data-stu-id="8ebc2-119">Specifies an endpoint behavior.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8ebc2-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="8ebc2-120">See also</span></span>

- <xref:System.ServiceModel.Configuration.DispatcherSynchronizationElement>
- <xref:System.ServiceModel.Description.DispatcherSynchronizationBehavior>
