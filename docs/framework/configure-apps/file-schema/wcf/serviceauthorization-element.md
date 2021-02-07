---
description: 了解详细信息： <serviceAuthorization> 元素
title: <serviceAuthorization> 元素
ms.date: 03/30/2017
ms.assetid: 18cddad5-ddcb-4839-a0ac-1d6f6ab783ca
ms.openlocfilehash: ee447f487027ed12f829dd0fd364556ce095d7d3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682925"
---
# <a name="serviceauthorization-element"></a><span data-ttu-id="2f916-103">\<serviceAuthorization> 元素</span><span class="sxs-lookup"><span data-stu-id="2f916-103">\<serviceAuthorization> element</span></span>

<span data-ttu-id="2f916-104">指定用于授予服务操作访问权限的设置。</span><span class="sxs-lookup"><span data-stu-id="2f916-104">Specifies settings that authorize access to service operations</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<serviceAuthorization>**  

## <a name="syntax"></a><span data-ttu-id="2f916-105">语法</span><span class="sxs-lookup"><span data-stu-id="2f916-105">Syntax</span></span>

```xml
<serviceAuthorization impersonateCallerForAllOperations="Boolean"
                      principalPermissionMode="None/UseWindowsGroups/UseAspNetRoles/Custom"
                      roleProviderName="String"
                      serviceAuthorizationManagerType="String">
  <authorizationPolicies>
    <add policyType="String" />
  </authorizationPolicies>
</serviceAuthorization>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="2f916-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="2f916-106">Attributes and elements</span></span>

<span data-ttu-id="2f916-107">以下各节描述了特性、子元素和父元素：</span><span class="sxs-lookup"><span data-stu-id="2f916-107">The following sections describe attributes, child elements, and parent elements:</span></span>

### <a name="attributes"></a><span data-ttu-id="2f916-108">特性</span><span class="sxs-lookup"><span data-stu-id="2f916-108">Attributes</span></span>

|<span data-ttu-id="2f916-109">属性</span><span class="sxs-lookup"><span data-stu-id="2f916-109">Attribute</span></span>|<span data-ttu-id="2f916-110">说明</span><span class="sxs-lookup"><span data-stu-id="2f916-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2f916-111">impersonateCallerForAllOperations</span><span class="sxs-lookup"><span data-stu-id="2f916-111">impersonateCallerForAllOperations</span></span>|<span data-ttu-id="2f916-112">一个布尔值，指定是否服务中的所有操作都模拟调用方。</span><span class="sxs-lookup"><span data-stu-id="2f916-112">A Boolean value that specifies if all the operations in the service impersonate the caller.</span></span> <span data-ttu-id="2f916-113">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="2f916-113">The default is `false`.</span></span><br /><br /> <span data-ttu-id="2f916-114">当特定服务操作模拟调用方时，线程上下文会在执行指定服务前切换为调用方上下文。</span><span class="sxs-lookup"><span data-stu-id="2f916-114">When a specific service operation impersonates the caller, the thread context is switched to the caller context before executing the specified service.</span></span>|  
|<span data-ttu-id="2f916-115">principalPermissionMode</span><span class="sxs-lookup"><span data-stu-id="2f916-115">principalPermissionMode</span></span>|<span data-ttu-id="2f916-116">设置用于在服务器上执行操作的主体。</span><span class="sxs-lookup"><span data-stu-id="2f916-116">Sets the principal used to carry out operations on the server.</span></span> <span data-ttu-id="2f916-117">包括以下值：</span><span class="sxs-lookup"><span data-stu-id="2f916-117">Values include the following:</span></span><br /><br /> <span data-ttu-id="2f916-118">-无</span><span class="sxs-lookup"><span data-stu-id="2f916-118">-   None</span></span><br /><span data-ttu-id="2f916-119">-UseWindowsGroups</span><span class="sxs-lookup"><span data-stu-id="2f916-119">-   UseWindowsGroups</span></span><br /><span data-ttu-id="2f916-120">-UseAspNetRoles</span><span class="sxs-lookup"><span data-stu-id="2f916-120">-   UseAspNetRoles</span></span><br /><span data-ttu-id="2f916-121">-Custom</span><span class="sxs-lookup"><span data-stu-id="2f916-121">-   Custom</span></span><br /><br /> <span data-ttu-id="2f916-122">默认值为 UseWindowsGroups。</span><span class="sxs-lookup"><span data-stu-id="2f916-122">The default value is UseWindowsGroups.</span></span> <span data-ttu-id="2f916-123">此值的类型为 <xref:System.ServiceModel.Description.PrincipalPermissionMode>。</span><span class="sxs-lookup"><span data-stu-id="2f916-123">The value is of type <xref:System.ServiceModel.Description.PrincipalPermissionMode>.</span></span> <span data-ttu-id="2f916-124">有关使用此属性的详细信息，请参阅 [如何：使用 PrincipalPermissionAttribute 类限制访问权限](../../../wcf/how-to-restrict-access-with-the-principalpermissionattribute-class.md)。</span><span class="sxs-lookup"><span data-stu-id="2f916-124">For more information on using this attribute, see [How to: Restrict Access with the PrincipalPermissionAttribute Class](../../../wcf/how-to-restrict-access-with-the-principalpermissionattribute-class.md).</span></span>|  
|<span data-ttu-id="2f916-125">roleProviderName</span><span class="sxs-lookup"><span data-stu-id="2f916-125">roleProviderName</span></span>|<span data-ttu-id="2f916-126">一个字符串，指定为 Windows Communication Foundation (WCF) 应用程序提供角色信息的角色提供程序的名称。</span><span class="sxs-lookup"><span data-stu-id="2f916-126">A string that specifies the name of the role provider, which provides role information for a Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="2f916-127">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="2f916-127">The default is an empty string.</span></span>|  
|<span data-ttu-id="2f916-128">ServiceAuthorizationManagerType</span><span class="sxs-lookup"><span data-stu-id="2f916-128">ServiceAuthorizationManagerType</span></span>|<span data-ttu-id="2f916-129">一个包含服务授权管理器的类型的字符串。</span><span class="sxs-lookup"><span data-stu-id="2f916-129">A string containing the type of the service authorization manager.</span></span> <span data-ttu-id="2f916-130">有关详细信息，请参阅 <xref:System.ServiceModel.ServiceAuthorizationManager>。</span><span class="sxs-lookup"><span data-stu-id="2f916-130">For more information, see <xref:System.ServiceModel.ServiceAuthorizationManager>.</span></span>|  

### <a name="child-elements"></a><span data-ttu-id="2f916-131">子元素</span><span class="sxs-lookup"><span data-stu-id="2f916-131">Child elements</span></span>

|<span data-ttu-id="2f916-132">元素</span><span class="sxs-lookup"><span data-stu-id="2f916-132">Element</span></span>|<span data-ttu-id="2f916-133">说明</span><span class="sxs-lookup"><span data-stu-id="2f916-133">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2f916-134">authorizationPolicies</span><span class="sxs-lookup"><span data-stu-id="2f916-134">authorizationPolicies</span></span>|<span data-ttu-id="2f916-135">包含可使用 `add` 关键字添加的授权策略类型的集合。</span><span class="sxs-lookup"><span data-stu-id="2f916-135">Contains a collection of authorization policy types, which can be added using the `add` keyword.</span></span> <span data-ttu-id="2f916-136">每个授权类型都包含一个所需的 `policyType` 属性，此属性是一个字符串。</span><span class="sxs-lookup"><span data-stu-id="2f916-136">Each authorization policy contains a single required `policyType` attribute that is a string.</span></span> <span data-ttu-id="2f916-137">该属性指定一个授权策略，可以将一组输入声明转换为另一组声明。</span><span class="sxs-lookup"><span data-stu-id="2f916-137">The attribute specifies an authorization policy, which enables transformation of one set of input claims into another set of claims.</span></span> <span data-ttu-id="2f916-138">可以根据该授权策略来授予或拒绝访问控制。</span><span class="sxs-lookup"><span data-stu-id="2f916-138">Access control can be granted or denied based on that.</span></span> <span data-ttu-id="2f916-139">有关详细信息，请参阅 <xref:System.ServiceModel.Configuration.AuthorizationPolicyTypeElement>。</span><span class="sxs-lookup"><span data-stu-id="2f916-139">For more information, see <xref:System.ServiceModel.Configuration.AuthorizationPolicyTypeElement>.</span></span>|  

### <a name="parent-elements"></a><span data-ttu-id="2f916-140">父元素</span><span class="sxs-lookup"><span data-stu-id="2f916-140">Parent elements</span></span>

|<span data-ttu-id="2f916-141">元素</span><span class="sxs-lookup"><span data-stu-id="2f916-141">Element</span></span>|<span data-ttu-id="2f916-142">说明</span><span class="sxs-lookup"><span data-stu-id="2f916-142">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="2f916-143">包含服务行为的设置集合。</span><span class="sxs-lookup"><span data-stu-id="2f916-143">Contains a collection of settings for the behavior of a service.</span></span>|  

## <a name="remarks"></a><span data-ttu-id="2f916-144">备注</span><span class="sxs-lookup"><span data-stu-id="2f916-144">Remarks</span></span>

<span data-ttu-id="2f916-145">本节包含一些影响授权、自定义角色提供程序和模拟的元素。</span><span class="sxs-lookup"><span data-stu-id="2f916-145">This section contains elements affecting authorization, custom role providers, and impersonation.</span></span>  
  
<span data-ttu-id="2f916-146">`principalPermissionMode` 属性指定在授权使用受保护方法时要使用的用户组。</span><span class="sxs-lookup"><span data-stu-id="2f916-146">The `principalPermissionMode` attribute specifies the groups of users to use when authorizing use of a protected method.</span></span> <span data-ttu-id="2f916-147">默认值为 `UseWindowsGroups`，该值指定在 Windows 组（例如，“Administrators”或“Users”）中搜索试图访问某个资源的标识。</span><span class="sxs-lookup"><span data-stu-id="2f916-147">The default value is `UseWindowsGroups` and specifies that Windows groups, such as "Administrators" or "Users," are searched for an identity trying to access a resource.</span></span> <span data-ttu-id="2f916-148">你还可以指定 `UseAspNetRoles` 以使用在元素下配置的自定义角色提供程序 \<system.web> ，如以下代码所示：</span><span class="sxs-lookup"><span data-stu-id="2f916-148">You can also specify `UseAspNetRoles` to use a custom role provider that is configured under the \<system.web> element, as shown in the following code:</span></span>

```xml
<system.web>
  <membership defaultProvider="SqlProvider"
              userIsOnlineTimeWindow="15">
    <providers>
      <clear />
      <add name="SqlProvider"
           type="System.Web.Security.SqlMembershipProvider"
           connectionStringName="SqlConn"
           applicationName="MembershipProvider"
           enablePasswordRetrieval="false"
           enablePasswordReset="false"
           requiresQuestionAndAnswer="false"
           requiresUniqueEmail="true"
           passwordFormat="Hashed" />
    </providers>
  </membership>
  <!-- Other configuration code not shown. -->
</system.web>
```
  
<span data-ttu-id="2f916-149">下面的代码演示了 `roleProviderName` 与属性一起使用的 `principalPermissionMode` ：</span><span class="sxs-lookup"><span data-stu-id="2f916-149">The following code shows the `roleProviderName` used with the `principalPermissionMode` attribute:</span></span>
  
```xml
<behaviors>
  <behavior name="ServiceBehaviour">
    <serviceAuthorization principalPermissionMode ="UseAspNetRoles"
                          roleProviderName ="SqlProvider" />
  </behavior>
  <!-- Other configuration code not shown. -->
</behaviors>
```

<span data-ttu-id="2f916-150">有关使用此配置元素的详细示例，请参阅 [授权访问服务操作](../../../wcf/samples/authorizing-access-to-service-operations.md) 和 [授权策略](../../../wcf/samples/authorization-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="2f916-150">For a detailed example of using this configuration element, see [Authorizing Access to Service Operations](../../../wcf/samples/authorizing-access-to-service-operations.md) and [Authorization Policy](../../../wcf/samples/authorization-policy.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f916-151">请参阅</span><span class="sxs-lookup"><span data-stu-id="2f916-151">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceAuthorizationElement>
- <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior>
- [<span data-ttu-id="2f916-152">安全行为</span><span class="sxs-lookup"><span data-stu-id="2f916-152">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="2f916-153">授予对服务操作的访问权限</span><span class="sxs-lookup"><span data-stu-id="2f916-153">Authorizing Access to Service Operations</span></span>](../../../wcf/samples/authorizing-access-to-service-operations.md)
- [<span data-ttu-id="2f916-154">如何：为服务创建自定义授权管理器</span><span class="sxs-lookup"><span data-stu-id="2f916-154">How to: Create a Custom Authorization Manager for a Service</span></span>](../../../wcf/extending/how-to-create-a-custom-authorization-manager-for-a-service.md)
- [<span data-ttu-id="2f916-155">如何：使用 PrincipalPermissionAttribute 类限制访问</span><span class="sxs-lookup"><span data-stu-id="2f916-155">How to: Restrict Access with the PrincipalPermissionAttribute Class</span></span>](../../../wcf/how-to-restrict-access-with-the-principalpermissionattribute-class.md)
- [<span data-ttu-id="2f916-156">授权策略</span><span class="sxs-lookup"><span data-stu-id="2f916-156">Authorization Policy</span></span>](../../../wcf/samples/authorization-policy.md)
