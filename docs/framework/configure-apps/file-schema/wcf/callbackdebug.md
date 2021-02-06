---
description: 了解详细信息： <callbackDebug>
title: <callbackDebug>
ms.date: 03/30/2017
ms.assetid: 4073feda-1857-4be4-9947-227afb847ced
ms.openlocfilehash: 911d738764baa800831c19f4e5d181118d1d3e00
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639206"
---
# \<callbackDebug>

<span data-ttu-id="b337f-102">指定 Windows Communication Foundation (WCF) 回调对象的服务调试。</span><span class="sxs-lookup"><span data-stu-id="b337f-102">Specifies service debugging for a Windows Communication Foundation (WCF) callback object.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<callbackDebug>**  
  
## <a name="syntax"></a><span data-ttu-id="b337f-103">语法</span><span class="sxs-lookup"><span data-stu-id="b337f-103">Syntax</span></span>  
  
```xml  
<callbackDebug includeExceptionDetailInFaults="Boolean" />
```  
  
## <a name="type"></a><span data-ttu-id="b337f-104">类型</span><span class="sxs-lookup"><span data-stu-id="b337f-104">Type</span></span>  

 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b337f-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="b337f-105">Attributes and Elements</span></span>  

 <span data-ttu-id="b337f-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b337f-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b337f-107">特性</span><span class="sxs-lookup"><span data-stu-id="b337f-107">Attributes</span></span>  
  
|<span data-ttu-id="b337f-108">属性</span><span class="sxs-lookup"><span data-stu-id="b337f-108">Attribute</span></span>|<span data-ttu-id="b337f-109">说明</span><span class="sxs-lookup"><span data-stu-id="b337f-109">Description</span></span>|  
|---------------|-----------------|  
|`includeExceptionDetailInFaults`|<span data-ttu-id="b337f-110">一个值，指定客户端回调对象是否向服务返回 SOAP 错误中的托管异常信息。</span><span class="sxs-lookup"><span data-stu-id="b337f-110">A value that specifies whether client callback objects return managed exception information in SOAP faults back to the service.</span></span><br /><br /> <span data-ttu-id="b337f-111">如果以编程方式将此属性设置为 `true`，则可以将客户端回调对象中的托管异常信息回流到服务，以便进行调试。</span><span class="sxs-lookup"><span data-stu-id="b337f-111">If you set this attribute to `true` programmatically, you can enable the flow of managed exception information in a client callback object back to the service for debugging purposes.</span></span> <span data-ttu-id="b337f-112">**警告：**  向客户端返回托管异常信息可能会带来安全风险。</span><span class="sxs-lookup"><span data-stu-id="b337f-112">**Caution:**  Returning managed exception information to clients can be a security risk.</span></span> <span data-ttu-id="b337f-113">这是因为，异常详细信息公开了有关内部服务实现的信息，这些信息可能被未经授权的客户端使用。</span><span class="sxs-lookup"><span data-stu-id="b337f-113">This is because exception details expose information about the internal service implementation that could be used by unauthorized clients.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b337f-114">子元素</span><span class="sxs-lookup"><span data-stu-id="b337f-114">Child Elements</span></span>  

 <span data-ttu-id="b337f-115">无。</span><span class="sxs-lookup"><span data-stu-id="b337f-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b337f-116">父元素</span><span class="sxs-lookup"><span data-stu-id="b337f-116">Parent Elements</span></span>  
  
|<span data-ttu-id="b337f-117">元素</span><span class="sxs-lookup"><span data-stu-id="b337f-117">Element</span></span>|<span data-ttu-id="b337f-118">说明</span><span class="sxs-lookup"><span data-stu-id="b337f-118">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="b337f-119">指定终结点行为。</span><span class="sxs-lookup"><span data-stu-id="b337f-119">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b337f-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="b337f-120">See also</span></span>

- <xref:System.ServiceModel.Configuration.CallbackDebugElement>
- <xref:System.ServiceModel.Description.CallbackDebugBehavior>
