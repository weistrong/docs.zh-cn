---
description: 了解详细信息： <pnrpPeerResolver>
title: <pnrpPeerResolver>
ms.date: 03/30/2017
ms.assetid: c1b34f3b-68e5-4911-a367-de49fb61dbc6
ms.openlocfilehash: 4af6a63312fa300cfa33e578f01b8e07267ad3a1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683536"
---
# \<pnrpPeerResolver>

<span data-ttu-id="91766-102">指定要将 PNRP（对等名称解析协议）解析程序用作解析程序。</span><span class="sxs-lookup"><span data-stu-id="91766-102">Specifies that the PNRP (Peer Name Resolution Protocol) resolver is to be used as a resolver.</span></span> <span data-ttu-id="91766-103">此元素是可选的，因为 PNRP 是默认解析程序。</span><span class="sxs-lookup"><span data-stu-id="91766-103">This element is optional because PNRP is the default resolver.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<pnrpResolver>**  
  
## <a name="syntax"></a><span data-ttu-id="91766-104">语法</span><span class="sxs-lookup"><span data-stu-id="91766-104">Syntax</span></span>  
  
```xml  
<pnrpResolver resolverType="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="91766-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="91766-105">Attributes and Elements</span></span>  

 <span data-ttu-id="91766-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="91766-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="91766-107">特性</span><span class="sxs-lookup"><span data-stu-id="91766-107">Attributes</span></span>  
  
|<span data-ttu-id="91766-108">属性</span><span class="sxs-lookup"><span data-stu-id="91766-108">Attribute</span></span>|<span data-ttu-id="91766-109">说明</span><span class="sxs-lookup"><span data-stu-id="91766-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="91766-110">resolverType</span><span class="sxs-lookup"><span data-stu-id="91766-110">resolverType</span></span>|<span data-ttu-id="91766-111">一个字符串，指定要使用的解析程序。</span><span class="sxs-lookup"><span data-stu-id="91766-111">A string that specifies the resolver to be used.</span></span> <span data-ttu-id="91766-112">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="91766-112">This attribute is optional.</span></span> <span data-ttu-id="91766-113">如果不设置，或者将其设置为空字符串，则使用 PNRP。</span><span class="sxs-lookup"><span data-stu-id="91766-113">If it is not set, or if it is set to an empty string, PNRP is used.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="91766-114">子元素</span><span class="sxs-lookup"><span data-stu-id="91766-114">Child Elements</span></span>  

 <span data-ttu-id="91766-115">无</span><span class="sxs-lookup"><span data-stu-id="91766-115">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="91766-116">父元素</span><span class="sxs-lookup"><span data-stu-id="91766-116">Parent Elements</span></span>  
  
|<span data-ttu-id="91766-117">元素</span><span class="sxs-lookup"><span data-stu-id="91766-117">Element</span></span>|<span data-ttu-id="91766-118">说明</span><span class="sxs-lookup"><span data-stu-id="91766-118">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="91766-119">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="91766-119">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="91766-120">示例</span><span class="sxs-lookup"><span data-stu-id="91766-120">Example</span></span>  
  
```xml  
<pnrpResolver resolverType="String" />
```  
  
## <a name="see-also"></a><span data-ttu-id="91766-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="91766-121">See also</span></span>

- <xref:System.ServiceModel.Configuration.PnrpPeerResolverElement>
- <xref:System.ServiceModel.Channels.PnrpPeerResolverBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="91766-122">绑定</span><span class="sxs-lookup"><span data-stu-id="91766-122">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="91766-123">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="91766-123">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="91766-124">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="91766-124">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
- [<span data-ttu-id="91766-125">对等解析程序</span><span class="sxs-lookup"><span data-stu-id="91766-125">Peer Resolvers</span></span>](../../../wcf/feature-details/peer-resolvers.md)
