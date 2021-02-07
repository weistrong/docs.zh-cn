---
description: 了解详细信息： <useManagedPresentation>
title: <useManagedPresentation>
ms.date: 03/30/2017
ms.assetid: 17a0dd77-af54-41db-a9d0-4b17ff42878f
ms.openlocfilehash: 9203daedcc0553c7a1308b2763b9e818ca6560c1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749033"
---
# \<useManagedPresentation>

<span data-ttu-id="2e750-102">一个绑定元素，用于与支持 WS-Trust 的 CardSpace 配置文件的 CardSpace 安全令牌服务进行通信。</span><span class="sxs-lookup"><span data-stu-id="2e750-102">A binding element used to communicate with a CardSpace Security Token Service that supports the CardSpace profile of WS-Trust.</span></span> <span data-ttu-id="2e750-103">此元素没有属性并且以空开关形式存在。</span><span class="sxs-lookup"><span data-stu-id="2e750-103">This element has no attribute and is present as an empty switch.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<useManagedPresentation>**  
  
## <a name="syntax"></a><span data-ttu-id="2e750-104">语法</span><span class="sxs-lookup"><span data-stu-id="2e750-104">Syntax</span></span>  
  
```xml  
<useManagedPresentation />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2e750-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="2e750-105">Attributes and Elements</span></span>  

 <span data-ttu-id="2e750-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2e750-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2e750-107">特性</span><span class="sxs-lookup"><span data-stu-id="2e750-107">Attributes</span></span>  

 <span data-ttu-id="2e750-108">无。</span><span class="sxs-lookup"><span data-stu-id="2e750-108">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="2e750-109">子元素</span><span class="sxs-lookup"><span data-stu-id="2e750-109">Child Elements</span></span>  

 <span data-ttu-id="2e750-110">无</span><span class="sxs-lookup"><span data-stu-id="2e750-110">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2e750-111">父元素</span><span class="sxs-lookup"><span data-stu-id="2e750-111">Parent Elements</span></span>  
  
|<span data-ttu-id="2e750-112">元素</span><span class="sxs-lookup"><span data-stu-id="2e750-112">Element</span></span>|<span data-ttu-id="2e750-113">说明</span><span class="sxs-lookup"><span data-stu-id="2e750-113">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="2e750-114">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="2e750-114">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2e750-115">备注</span><span class="sxs-lookup"><span data-stu-id="2e750-115">Remarks</span></span>  

 <span data-ttu-id="2e750-116">标识提供程序使用此元素，用以在它的策略中表明它支持 WS-Trust 的 CardSpace 配置文件这一事实。</span><span class="sxs-lookup"><span data-stu-id="2e750-116">This element is used by an identity provider to express in its policy the fact that it supports the CardSpace profile of WS-Trust.</span></span> <span data-ttu-id="2e750-117">发布这种策略断言的标识提供程序应该能够基于该 CardSpace 配置文件颁发令牌。</span><span class="sxs-lookup"><span data-stu-id="2e750-117">Identity providers that publish such a policy assertion should be able to issue tokens based on that CardSpace profile.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e750-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="2e750-118">See also</span></span>

- <xref:System.ServiceModel.Configuration.UseManagedPresentationElement>
- <xref:System.ServiceModel.Channels.UseManagedPresentationBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="2e750-119">绑定</span><span class="sxs-lookup"><span data-stu-id="2e750-119">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="2e750-120">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="2e750-120">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="2e750-121">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="2e750-121">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
