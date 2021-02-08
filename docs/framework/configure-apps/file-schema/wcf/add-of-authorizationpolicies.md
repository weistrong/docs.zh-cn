---
description: 了解详细 <add> 信息： <authorizationPolicies>
title: <add> 的 <authorizationPolicies>
ms.date: 03/30/2017
ms.assetid: 613a03d8-4384-4556-bce2-8c23286c0bb0
ms.openlocfilehash: 616f09abfad51f41348b0ffa8557a4fd54492437
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99804096"
---
# <a name="add-of-authorizationpolicies"></a><span data-ttu-id="74558-103">\<add> 的 \<authorizationPolicies></span><span class="sxs-lookup"><span data-stu-id="74558-103">\<add> of \<authorizationPolicies></span></span>

<span data-ttu-id="74558-104">指定声明转换的授权策略。</span><span class="sxs-lookup"><span data-stu-id="74558-104">Specifies an authorization policy for claim transformation.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceAuthorization>**](serviceauthorization-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<authorizationPolicies>**](authorizationpolicies.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="74558-105">语法</span><span class="sxs-lookup"><span data-stu-id="74558-105">Syntax</span></span>  
  
```xml  
<authorizationPolicies>
  <add policyType="String" />
</authorizationPolicies>
```  
  
## <a name="type"></a><span data-ttu-id="74558-106">类型</span><span class="sxs-lookup"><span data-stu-id="74558-106">Type</span></span>  

 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="74558-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="74558-107">Attributes and Elements</span></span>  

 <span data-ttu-id="74558-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="74558-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="74558-109">特性</span><span class="sxs-lookup"><span data-stu-id="74558-109">Attributes</span></span>  
  
|<span data-ttu-id="74558-110">属性</span><span class="sxs-lookup"><span data-stu-id="74558-110">Attribute</span></span>|<span data-ttu-id="74558-111">说明</span><span class="sxs-lookup"><span data-stu-id="74558-111">Description</span></span>|  
|---------------|-----------------|  
|`policyType`|<span data-ttu-id="74558-112">必需的字符串属性。</span><span class="sxs-lookup"><span data-stu-id="74558-112">A required String attribute.</span></span><br /><br /> <span data-ttu-id="74558-113">Windows Communication Foundation (WCF) 访问控制模型支持将一组授权策略作为类型进行设置。</span><span class="sxs-lookup"><span data-stu-id="74558-113">The Windows Communication Foundation (WCF) access control model supports provisioning a set of authorization policies as types.</span></span> <span data-ttu-id="74558-114">此属性指定一个授权策略，使得可以将一组输入声明转换为另一组声明。</span><span class="sxs-lookup"><span data-stu-id="74558-114">This attribute specifies an authorization policy, which enables transformation of one set of input claims into another set of claims.</span></span> <span data-ttu-id="74558-115">可以根据该授权策略来授予或拒绝访问控制。</span><span class="sxs-lookup"><span data-stu-id="74558-115">Access control can be granted or denied based on that.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="74558-116">子元素</span><span class="sxs-lookup"><span data-stu-id="74558-116">Child Elements</span></span>  

 <span data-ttu-id="74558-117">无。</span><span class="sxs-lookup"><span data-stu-id="74558-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="74558-118">父元素</span><span class="sxs-lookup"><span data-stu-id="74558-118">Parent Elements</span></span>  
  
|<span data-ttu-id="74558-119">元素</span><span class="sxs-lookup"><span data-stu-id="74558-119">Element</span></span>|<span data-ttu-id="74558-120">说明</span><span class="sxs-lookup"><span data-stu-id="74558-120">Description</span></span>|  
|-------------|-----------------|  
|[\<authorizationPolicies>](authorizationpolicies.md)|<span data-ttu-id="74558-121">指定一个授权策略类型集合。</span><span class="sxs-lookup"><span data-stu-id="74558-121">Specifies a collection of authorization policy types.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="74558-122">备注</span><span class="sxs-lookup"><span data-stu-id="74558-122">Remarks</span></span>  

 <span data-ttu-id="74558-123">每个授权类型都包含一个所需的 `policyType` 属性，此属性是一个字符串。</span><span class="sxs-lookup"><span data-stu-id="74558-123">Each authorization policy contains a single required `policyType` attribute that is a string.</span></span> <span data-ttu-id="74558-124">该属性指定一个授权策略，可以将一组输入声明转换为另一组声明。</span><span class="sxs-lookup"><span data-stu-id="74558-124">The attribute specifies an authorization policy, which enables transformation of one set of input claims into another set of claims.</span></span> <span data-ttu-id="74558-125">可以根据该授权策略来授予或拒绝访问控制。</span><span class="sxs-lookup"><span data-stu-id="74558-125">Access control can be granted or denied based on that.</span></span> <span data-ttu-id="74558-126">有关授权策略工作方式的详细信息，请参阅 <xref:System.IdentityModel.Policy.IAuthorizationPolicy> 和 [授权策略](../../../wcf/samples/authorization-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="74558-126">For more information on how an authorization policy works, see <xref:System.IdentityModel.Policy.IAuthorizationPolicy> and [Authorization Policy](../../../wcf/samples/authorization-policy.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74558-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="74558-127">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceAuthorizationElement>
- <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior.ExternalAuthorizationPolicies%2A>
- <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior>
- <xref:System.ServiceModel.Configuration.AuthorizationPolicyTypeElement>
- <xref:System.ServiceModel.Configuration.ServiceAuthorizationElement.AuthorizationPolicies%2A>
- <xref:System.ServiceModel.Configuration.AuthorizationPolicyTypeElementCollection>
- <xref:System.IdentityModel.Policy.IAuthorizationPolicy>
- [<span data-ttu-id="74558-128">授予对服务操作的访问权限</span><span class="sxs-lookup"><span data-stu-id="74558-128">Authorizing Access to Service Operations</span></span>](../../../wcf/samples/authorizing-access-to-service-operations.md)
- [<span data-ttu-id="74558-129">如何：为服务创建自定义授权管理器</span><span class="sxs-lookup"><span data-stu-id="74558-129">How to: Create a Custom Authorization Manager for a Service</span></span>](../../../wcf/extending/how-to-create-a-custom-authorization-manager-for-a-service.md)
- [\<add>](add-of-authorizationpolicies.md)
- [<span data-ttu-id="74558-130">授权策略</span><span class="sxs-lookup"><span data-stu-id="74558-130">Authorization Policy</span></span>](../../../wcf/samples/authorization-policy.md)
