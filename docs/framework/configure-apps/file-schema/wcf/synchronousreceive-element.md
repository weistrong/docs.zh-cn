---
description: 了解详细信息： <synchronousReceive> 元素
title: <synchronousReceive> 元素
ms.date: 03/30/2017
ms.assetid: cc070387-3d11-4b02-a952-bc08ad2df05a
ms.openlocfilehash: afcd10b4ad41bd6ff12dbf246f66ef7fac4e759a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682613"
---
# <a name="synchronousreceive-element"></a><span data-ttu-id="f400b-103">\<synchronousReceive> 元素</span><span class="sxs-lookup"><span data-stu-id="f400b-103">\<synchronousReceive> element</span></span>

<span data-ttu-id="f400b-104">此配置元素用于指定服务或客户端应用程序中用来接收消息的运行时行为。</span><span class="sxs-lookup"><span data-stu-id="f400b-104">This configuration element is used to specify run-time behavior for receiving messages in either a service or client application.</span></span> <span data-ttu-id="f400b-105">它不具有任何属性或子元素。</span><span class="sxs-lookup"><span data-stu-id="f400b-105">It does not have any attributes or child elements.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<synchronousReceive>**  
  
## <a name="syntax"></a><span data-ttu-id="f400b-106">语法</span><span class="sxs-lookup"><span data-stu-id="f400b-106">Syntax</span></span>  
  
```xml  
<synchronousReceive />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f400b-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f400b-107">Attributes and Elements</span></span>  

 <span data-ttu-id="f400b-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f400b-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f400b-109">特性</span><span class="sxs-lookup"><span data-stu-id="f400b-109">Attributes</span></span>  

 <span data-ttu-id="f400b-110">无。</span><span class="sxs-lookup"><span data-stu-id="f400b-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="f400b-111">子元素</span><span class="sxs-lookup"><span data-stu-id="f400b-111">Child Elements</span></span>  

 <span data-ttu-id="f400b-112">无。</span><span class="sxs-lookup"><span data-stu-id="f400b-112">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f400b-113">父元素</span><span class="sxs-lookup"><span data-stu-id="f400b-113">Parent Elements</span></span>  
  
|<span data-ttu-id="f400b-114">元素</span><span class="sxs-lookup"><span data-stu-id="f400b-114">Element</span></span>|<span data-ttu-id="f400b-115">说明</span><span class="sxs-lookup"><span data-stu-id="f400b-115">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="f400b-116">指定终结点行为。</span><span class="sxs-lookup"><span data-stu-id="f400b-116">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f400b-117">备注</span><span class="sxs-lookup"><span data-stu-id="f400b-117">Remarks</span></span>  

 <span data-ttu-id="f400b-118">使用此行为可指示通道侦听器使用同步接收，而非默认的异步接受。</span><span class="sxs-lookup"><span data-stu-id="f400b-118">Use this behavior to instruct the channel listener to use a synchronous receive rather than the default, asynchronous.</span></span> <span data-ttu-id="f400b-119">Windows Communication Foundation (WCF) 发出一个新线程，以便为每个接受的通道抽取。</span><span class="sxs-lookup"><span data-stu-id="f400b-119">Windows Communication Foundation (WCF) issues a new thread to pump for each accepted channel.</span></span> <span data-ttu-id="f400b-120">如果有许多通道，则可能出现线程溢出的情况。</span><span class="sxs-lookup"><span data-stu-id="f400b-120">If there are a lot of channels, there is the possibility of running out of threads.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f400b-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="f400b-121">See also</span></span>

- <xref:System.ServiceModel.Configuration.SynchronousReceiveElement>
- <xref:System.ServiceModel.Description.SynchronousReceiveBehavior>
