---
description: 了解详细信息： <persistenceProvider>
title: <persistenceProvider>
ms.date: 03/30/2017
ms.assetid: a37049c5-a7ea-4519-94f2-912eeb010380
ms.openlocfilehash: 60ddaf9f26f496bd7d79ccab84f84135e46963d1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683549"
---
# \<persistenceProvider>

<span data-ttu-id="a6fa5-102">指定要使用的持久性提供程序实现的类型以及用于持久性操作的超时值。</span><span class="sxs-lookup"><span data-stu-id="a6fa5-102">Specifies the type of the persistence provider implementation to use, as well as the time-out to use for persistence operations.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<persistenceProvider>**  
  
## <a name="syntax"></a><span data-ttu-id="a6fa5-103">语法</span><span class="sxs-lookup"><span data-stu-id="a6fa5-103">Syntax</span></span>  
  
```xml  
<persistenceProvider persistenceOperationTimeout="TimeSpan"
                     type="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a6fa5-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="a6fa5-104">Attributes and Elements</span></span>  

 <span data-ttu-id="a6fa5-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a6fa5-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a6fa5-106">特性</span><span class="sxs-lookup"><span data-stu-id="a6fa5-106">Attributes</span></span>  
  
|<span data-ttu-id="a6fa5-107">属性</span><span class="sxs-lookup"><span data-stu-id="a6fa5-107">Attribute</span></span>|<span data-ttu-id="a6fa5-108">说明</span><span class="sxs-lookup"><span data-stu-id="a6fa5-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a6fa5-109">persistenceOperationTimeout</span><span class="sxs-lookup"><span data-stu-id="a6fa5-109">persistenceOperationTimeout</span></span>|<span data-ttu-id="a6fa5-110">一个 <xref:System.TimeSpan> 值，指定用于持久性操作的超时值。</span><span class="sxs-lookup"><span data-stu-id="a6fa5-110">A <xref:System.TimeSpan> value that specifies the time-out used for persistence operations.</span></span> <span data-ttu-id="a6fa5-111">默认值为 "00:00:30"。</span><span class="sxs-lookup"><span data-stu-id="a6fa5-111">The default is "00:00:30".</span></span>|  
|<span data-ttu-id="a6fa5-112">type</span><span class="sxs-lookup"><span data-stu-id="a6fa5-112">type</span></span>|<span data-ttu-id="a6fa5-113">一个字符串，指定要使用的永久性提供程序工厂的类型。</span><span class="sxs-lookup"><span data-stu-id="a6fa5-113">A string that specifies the type of the persistence provider factory to use.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a6fa5-114">子元素</span><span class="sxs-lookup"><span data-stu-id="a6fa5-114">Child Elements</span></span>  

 <span data-ttu-id="a6fa5-115">无。</span><span class="sxs-lookup"><span data-stu-id="a6fa5-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a6fa5-116">父元素</span><span class="sxs-lookup"><span data-stu-id="a6fa5-116">Parent Elements</span></span>  
  
|<span data-ttu-id="a6fa5-117">元素</span><span class="sxs-lookup"><span data-stu-id="a6fa5-117">Element</span></span>|<span data-ttu-id="a6fa5-118">说明</span><span class="sxs-lookup"><span data-stu-id="a6fa5-118">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="a6fa5-119">指定行为元素。</span><span class="sxs-lookup"><span data-stu-id="a6fa5-119">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a6fa5-120">备注</span><span class="sxs-lookup"><span data-stu-id="a6fa5-120">Remarks</span></span>  

 <span data-ttu-id="a6fa5-121">此元素指定要用于序列化 WCF 服务的状态的永久性提供程序。</span><span class="sxs-lookup"><span data-stu-id="a6fa5-121">This element specifies the persistence provider to be used to serialize the state of a WCF service.</span></span> <span data-ttu-id="a6fa5-122">它应该与 `wsHttpContextBinding` 一起使用，后者在 HTTP 头中传递状态信息。</span><span class="sxs-lookup"><span data-stu-id="a6fa5-122">It should be used together with the `wsHttpContextBinding` which passes state information in HTTP headers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6fa5-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="a6fa5-123">See also</span></span>

- <xref:System.ServiceModel.Configuration.PersistenceProviderElement>
- <xref:System.ServiceModel.Persistence.PersistenceProvider>
