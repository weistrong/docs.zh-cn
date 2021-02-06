---
description: 了解详细信息： <callbackTimeouts>
title: <callbackTimeouts>
ms.date: 03/30/2017
ms.assetid: d7fcfc5f-6d35-491e-8fa6-2f964c1e792f
ms.openlocfilehash: 8e2e05ad23f661c38430ccddc615c37705e6fc44
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639193"
---
# \<callbackTimeouts>

<span data-ttu-id="d362c-102">在双工回调协定方案中指定使事务从服务器流动到客户端时的超时值。</span><span class="sxs-lookup"><span data-stu-id="d362c-102">Specifies the timeout value when flowing transactions from server to client.in a duplex callback contract scenario.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<callbackTimeOuts>**  
  
## <a name="syntax"></a><span data-ttu-id="d362c-103">语法</span><span class="sxs-lookup"><span data-stu-id="d362c-103">Syntax</span></span>  
  
```xml  
<callbackTimeOuts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="d362c-104">类型</span><span class="sxs-lookup"><span data-stu-id="d362c-104">Type</span></span>  

 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d362c-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d362c-105">Attributes and Elements</span></span>  

 <span data-ttu-id="d362c-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d362c-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d362c-107">特性</span><span class="sxs-lookup"><span data-stu-id="d362c-107">Attributes</span></span>  
  
|<span data-ttu-id="d362c-108">属性</span><span class="sxs-lookup"><span data-stu-id="d362c-108">Attribute</span></span>|<span data-ttu-id="d362c-109">说明</span><span class="sxs-lookup"><span data-stu-id="d362c-109">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="d362c-110">一个 <xref:System.TimeSpan> 值，指定时间间隔，事务必须在此期间完成，否则会自动终止。</span><span class="sxs-lookup"><span data-stu-id="d362c-110">A <xref:System.TimeSpan> value that specifies the interval of time within which transactions must complete or be automatically terminated.</span></span> <span data-ttu-id="d362c-111">默认值为 "00:00:00"。</span><span class="sxs-lookup"><span data-stu-id="d362c-111">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d362c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d362c-112">Child Elements</span></span>  

 <span data-ttu-id="d362c-113">无。</span><span class="sxs-lookup"><span data-stu-id="d362c-113">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d362c-114">父元素</span><span class="sxs-lookup"><span data-stu-id="d362c-114">Parent Elements</span></span>  
  
|<span data-ttu-id="d362c-115">元素</span><span class="sxs-lookup"><span data-stu-id="d362c-115">Element</span></span>|<span data-ttu-id="d362c-116">说明</span><span class="sxs-lookup"><span data-stu-id="d362c-116">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="d362c-117">指定终结点行为。</span><span class="sxs-lookup"><span data-stu-id="d362c-117">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d362c-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="d362c-118">See also</span></span>

- <xref:System.ServiceModel.Configuration.CallbackTimeoutsElement>
