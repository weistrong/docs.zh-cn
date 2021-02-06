---
description: 了解有关 <clear> 元素的详细 <claimTypeRequirements> 信息
title: <clear> of <claimTypeRequirements> 元素
ms.date: 03/30/2017
ms.assetid: ef42fde7-f292-4610-9111-9fea382c3b5f
ms.openlocfilehash: d25dad5afcec352f040ea4f8c08e5ffa2bc16d19
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638881"
---
# <a name="clear-of-claimtyperequirements-element"></a><span data-ttu-id="780d6-103">\<clear> of \<claimTypeRequirements> 元素</span><span class="sxs-lookup"><span data-stu-id="780d6-103">\<clear> of \<claimTypeRequirements> element</span></span>

<span data-ttu-id="780d6-104">指定所有声明类型都将从联合凭据中移除。</span><span class="sxs-lookup"><span data-stu-id="780d6-104">Specifies that all the claim types to be removed in the federated credential.</span></span> <span data-ttu-id="780d6-105">这样可以确保集合最初为空。</span><span class="sxs-lookup"><span data-stu-id="780d6-105">This ensures that the collection starts empty.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<wsFederationHttpBinding>**](wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<message>**](message-element-of-wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<claimTypeRequirements>**](claimtyperequirements-for-message.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**  
  
## <a name="syntax"></a><span data-ttu-id="780d6-106">语法</span><span class="sxs-lookup"><span data-stu-id="780d6-106">Syntax</span></span>  
  
```xml  
<claimTypeRequirements>
  <clear />
</claimTypeRequirements>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="780d6-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="780d6-107">Attributes and Elements</span></span>  

 <span data-ttu-id="780d6-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="780d6-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="780d6-109">特性</span><span class="sxs-lookup"><span data-stu-id="780d6-109">Attributes</span></span>  

 <span data-ttu-id="780d6-110">无。</span><span class="sxs-lookup"><span data-stu-id="780d6-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="780d6-111">子元素</span><span class="sxs-lookup"><span data-stu-id="780d6-111">Child Elements</span></span>  

 <span data-ttu-id="780d6-112">无。</span><span class="sxs-lookup"><span data-stu-id="780d6-112">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="780d6-113">父元素</span><span class="sxs-lookup"><span data-stu-id="780d6-113">Parent Elements</span></span>  
  
|<span data-ttu-id="780d6-114">元素</span><span class="sxs-lookup"><span data-stu-id="780d6-114">Element</span></span>|<span data-ttu-id="780d6-115">说明</span><span class="sxs-lookup"><span data-stu-id="780d6-115">Description</span></span>|  
|-------------|-----------------|  
|[\<claimTypeRequirements>](claimtyperequirements-for-message.md)|<span data-ttu-id="780d6-116">指定所需声明类型的集合。</span><span class="sxs-lookup"><span data-stu-id="780d6-116">Specifies a collection of required claim types.</span></span> <span data-ttu-id="780d6-117">每个元素的类型都为 <xref:System.ServiceModel.Configuration.ClaimTypeElement>。</span><span class="sxs-lookup"><span data-stu-id="780d6-117">Each element is of type <xref:System.ServiceModel.Configuration.ClaimTypeElement>.</span></span><br /><br /> <span data-ttu-id="780d6-118">在联合方案中，服务规定有关传入凭据的要求。</span><span class="sxs-lookup"><span data-stu-id="780d6-118">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="780d6-119">例如，传入凭据必须具有某组声明类型。</span><span class="sxs-lookup"><span data-stu-id="780d6-119">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="780d6-120">此集合中的每个元素都指定希望出现在联合凭据中的必选和可选的声明类型。</span><span class="sxs-lookup"><span data-stu-id="780d6-120">Each element in this collection specifies the types of required and optional claims expected to appear in a federated credential.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="780d6-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="780d6-121">See also</span></span>

- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Security.Tokens.ClaimTypeRequirement>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ClaimTypeElement>
