---
description: 了解有关 <remove> 元素的详细 <claimTypeRequirements> 信息
title: <remove> of <claimTypeRequirements> 元素
ms.date: 03/30/2017
ms.assetid: 8ef05bc4-1950-4ee4-95c5-1c6a394eff7e
ms.openlocfilehash: 2ec917d27966954382e5b091fd538168b48b5ffb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786897"
---
# <a name="remove-of-claimtyperequirements-element"></a><span data-ttu-id="b4f5d-103">\<remove> of \<claimTypeRequirements> 元素</span><span class="sxs-lookup"><span data-stu-id="b4f5d-103">\<remove> of \<claimTypeRequirements> element</span></span>

<span data-ttu-id="b4f5d-104">指定要从联合凭据中移除的声明的类型。</span><span class="sxs-lookup"><span data-stu-id="b4f5d-104">Specifies the types of claims to be removed in the federated credential.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<wsFederationHttpBinding>**](wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<message>**](message-element-of-wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<claimTypeRequirements>**](claimtyperequirements-for-message.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**  
  
## <a name="syntax"></a><span data-ttu-id="b4f5d-105">语法</span><span class="sxs-lookup"><span data-stu-id="b4f5d-105">Syntax</span></span>  
  
```xml  
<claimTypeRequirements>
  <remove claimType="URI" />
</claimTypeRequirements>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b4f5d-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="b4f5d-106">Attributes and Elements</span></span>  

 <span data-ttu-id="b4f5d-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b4f5d-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b4f5d-108">特性</span><span class="sxs-lookup"><span data-stu-id="b4f5d-108">Attributes</span></span>  
  
|<span data-ttu-id="b4f5d-109">属性</span><span class="sxs-lookup"><span data-stu-id="b4f5d-109">Attribute</span></span>|<span data-ttu-id="b4f5d-110">说明</span><span class="sxs-lookup"><span data-stu-id="b4f5d-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b4f5d-111">claimType</span><span class="sxs-lookup"><span data-stu-id="b4f5d-111">claimType</span></span>|<span data-ttu-id="b4f5d-112">一个 URI，定义要移除的声明的类型。</span><span class="sxs-lookup"><span data-stu-id="b4f5d-112">A URI that defines the type of a claim to be removed.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b4f5d-113">子元素</span><span class="sxs-lookup"><span data-stu-id="b4f5d-113">Child Elements</span></span>  

 <span data-ttu-id="b4f5d-114">无。</span><span class="sxs-lookup"><span data-stu-id="b4f5d-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b4f5d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b4f5d-115">Parent Elements</span></span>  
  
|<span data-ttu-id="b4f5d-116">元素</span><span class="sxs-lookup"><span data-stu-id="b4f5d-116">Element</span></span>|<span data-ttu-id="b4f5d-117">说明</span><span class="sxs-lookup"><span data-stu-id="b4f5d-117">Description</span></span>|  
|-------------|-----------------|  
|[\<claimTypeRequirements>](claimtyperequirements-for-message.md)|<span data-ttu-id="b4f5d-118">指定所需声明类型的集合。</span><span class="sxs-lookup"><span data-stu-id="b4f5d-118">Specifies a collection of required claim types.</span></span> <span data-ttu-id="b4f5d-119">每个元素的类型都为 <xref:System.ServiceModel.Configuration.ClaimTypeElement>。</span><span class="sxs-lookup"><span data-stu-id="b4f5d-119">Each element is of type <xref:System.ServiceModel.Configuration.ClaimTypeElement>.</span></span><br /><br /> <span data-ttu-id="b4f5d-120">在联合方案中，服务规定有关传入凭据的要求。</span><span class="sxs-lookup"><span data-stu-id="b4f5d-120">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="b4f5d-121">例如，传入凭据必须具有某组声明类型。</span><span class="sxs-lookup"><span data-stu-id="b4f5d-121">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="b4f5d-122">此集合中的每个元素都指定希望出现在联合凭据中的必选和可选的声明类型。</span><span class="sxs-lookup"><span data-stu-id="b4f5d-122">Each element in this collection specifies the types of required and optional claims expected to appear in a federated credential.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b4f5d-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="b4f5d-123">See also</span></span>

- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Security.Tokens.ClaimTypeRequirement>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ClaimTypeElement>
