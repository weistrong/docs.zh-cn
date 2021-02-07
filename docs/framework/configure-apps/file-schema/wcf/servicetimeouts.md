---
description: 了解详细信息： <serviceTimeouts>
title: <serviceTimeouts>
ms.date: 03/30/2017
ms.assetid: ada536cf-97dc-4cd7-89ec-ed1466c1c557
ms.openlocfilehash: bc9ef99078f8c6fa3b441604e14df928eec054e1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682720"
---
# \<serviceTimeouts>

<span data-ttu-id="d1b30-102">指定服务的超时。</span><span class="sxs-lookup"><span data-stu-id="d1b30-102">Specifies the timeout for a service.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<serviceTimeouts>**  
  
## <a name="syntax"></a><span data-ttu-id="d1b30-103">语法</span><span class="sxs-lookup"><span data-stu-id="d1b30-103">Syntax</span></span>  
  
```xml  
<serviceTimeouts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="d1b30-104">类型</span><span class="sxs-lookup"><span data-stu-id="d1b30-104">Type</span></span>  

 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d1b30-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d1b30-105">Attributes and Elements</span></span>  

 <span data-ttu-id="d1b30-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d1b30-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d1b30-107">特性</span><span class="sxs-lookup"><span data-stu-id="d1b30-107">Attributes</span></span>  
  
|<span data-ttu-id="d1b30-108">属性</span><span class="sxs-lookup"><span data-stu-id="d1b30-108">Attribute</span></span>|<span data-ttu-id="d1b30-109">说明</span><span class="sxs-lookup"><span data-stu-id="d1b30-109">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="d1b30-110">一个 <xref:System.TimeSpan> 值，指定事务从客户端流动到服务器所必须经历的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="d1b30-110">A <xref:System.TimeSpan> value that specifies the interval of time a transaction must flow from client to server.</span></span> <span data-ttu-id="d1b30-111">默认值为 "00:00:00"。</span><span class="sxs-lookup"><span data-stu-id="d1b30-111">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d1b30-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d1b30-112">Child Elements</span></span>  

 <span data-ttu-id="d1b30-113">无。</span><span class="sxs-lookup"><span data-stu-id="d1b30-113">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d1b30-114">父元素</span><span class="sxs-lookup"><span data-stu-id="d1b30-114">Parent Elements</span></span>  
  
|<span data-ttu-id="d1b30-115">元素</span><span class="sxs-lookup"><span data-stu-id="d1b30-115">Element</span></span>|<span data-ttu-id="d1b30-116">说明</span><span class="sxs-lookup"><span data-stu-id="d1b30-116">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="d1b30-117">指定行为元素。</span><span class="sxs-lookup"><span data-stu-id="d1b30-117">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d1b30-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="d1b30-118">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
