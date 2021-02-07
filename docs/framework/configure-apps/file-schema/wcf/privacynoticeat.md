---
description: 了解详细信息： <privacyNoticeAt>
title: <privacyNoticeAt>
ms.date: 03/30/2017
ms.assetid: 4cc96942-4eb9-4241-b2fd-45aa239915e8
ms.openlocfilehash: 2e38d43becd783cc50afba5a029d3ab9905ec15a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683497"
---
# \<privacyNoticeAt>

<span data-ttu-id="7067d-102">表示一个配置元素，该元素指定 `wsFederationHttp` 绑定中使用的隐私声明。</span><span class="sxs-lookup"><span data-stu-id="7067d-102">Represents a configuration element that specifies a privacy notice used in `wsFederationHttp` binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<privacyNotice>**  
  
## <a name="syntax"></a><span data-ttu-id="7067d-103">语法</span><span class="sxs-lookup"><span data-stu-id="7067d-103">Syntax</span></span>  
  
```xml  
<privacyNotice url="String"
               version="Integer" />
```  
  
## <a name="type"></a><span data-ttu-id="7067d-104">类型</span><span class="sxs-lookup"><span data-stu-id="7067d-104">Type</span></span>  

 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7067d-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="7067d-105">Attributes and Elements</span></span>  

 <span data-ttu-id="7067d-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7067d-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7067d-107">特性</span><span class="sxs-lookup"><span data-stu-id="7067d-107">Attributes</span></span>  
  
|<span data-ttu-id="7067d-108">属性</span><span class="sxs-lookup"><span data-stu-id="7067d-108">Attribute</span></span>|<span data-ttu-id="7067d-109">说明</span><span class="sxs-lookup"><span data-stu-id="7067d-109">Description</span></span>|  
|---------------|-----------------|  
|`url`|<span data-ttu-id="7067d-110">一个字符串，指定隐私声明位于的 URI。</span><span class="sxs-lookup"><span data-stu-id="7067d-110">A string that specifies the URI at which the privacy notice is located.</span></span>|  
|`version`|<span data-ttu-id="7067d-111">一个整数，指定此隐私声明的版本。</span><span class="sxs-lookup"><span data-stu-id="7067d-111">An integer that specifies the version of this privacy notice.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7067d-112">子元素</span><span class="sxs-lookup"><span data-stu-id="7067d-112">Child Elements</span></span>  

 <span data-ttu-id="7067d-113">无。</span><span class="sxs-lookup"><span data-stu-id="7067d-113">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7067d-114">父元素</span><span class="sxs-lookup"><span data-stu-id="7067d-114">Parent Elements</span></span>  
  
|<span data-ttu-id="7067d-115">元素</span><span class="sxs-lookup"><span data-stu-id="7067d-115">Element</span></span>|<span data-ttu-id="7067d-116">说明</span><span class="sxs-lookup"><span data-stu-id="7067d-116">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="7067d-117">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="7067d-117">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7067d-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="7067d-118">See also</span></span>

- <xref:System.ServiceModel.Configuration.PrivacyNoticeElement>
- <xref:System.ServiceModel.Channels.PrivacyNoticeBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="7067d-119">绑定</span><span class="sxs-lookup"><span data-stu-id="7067d-119">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="7067d-120">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="7067d-120">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="7067d-121">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="7067d-121">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
