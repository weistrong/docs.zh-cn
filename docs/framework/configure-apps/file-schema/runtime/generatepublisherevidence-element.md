---
description: 了解详细信息： <generatePublisherEvidence> 元素
title: <generatePublisherEvidence> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- generatePublisherEvidence element
- <generatePublisherEvidence> element
ms.assetid: 7d208f50-e8d5-4a42-bc1a-1cf3590706a8
ms.openlocfilehash: 2a949b52abe5ec10872d2cade49a0556063b2018
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754519"
---
# <a name="generatepublisherevidence-element"></a><span data-ttu-id="8a2d2-103">\<generatePublisherEvidence> 元素</span><span class="sxs-lookup"><span data-stu-id="8a2d2-103">\<generatePublisherEvidence> Element</span></span>

<span data-ttu-id="8a2d2-104">指定运行时是否 <xref:System.Security.Policy.Publisher> 为代码访问安全性 (CAS) 创建证据。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-104">Specifies whether the runtime creates <xref:System.Security.Policy.Publisher> evidence for code access security (CAS).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<generatePublisherEvidence>**  
  
## <a name="syntax"></a><span data-ttu-id="8a2d2-105">语法</span><span class="sxs-lookup"><span data-stu-id="8a2d2-105">Syntax</span></span>  
  
```xml  
<generatePublisherEvidence
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8a2d2-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="8a2d2-106">Attributes and Elements</span></span>  

 <span data-ttu-id="8a2d2-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8a2d2-108">特性</span><span class="sxs-lookup"><span data-stu-id="8a2d2-108">Attributes</span></span>  
  
|<span data-ttu-id="8a2d2-109">属性</span><span class="sxs-lookup"><span data-stu-id="8a2d2-109">Attribute</span></span>|<span data-ttu-id="8a2d2-110">描述</span><span class="sxs-lookup"><span data-stu-id="8a2d2-110">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="8a2d2-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="8a2d2-112">指定运行时是否创建 <xref:System.Security.Policy.Publisher> 证据。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-112">Specifies whether the runtime creates <xref:System.Security.Policy.Publisher> evidence.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="8a2d2-113">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="8a2d2-113">enabled Attribute</span></span>  
  
|<span data-ttu-id="8a2d2-114">值</span><span class="sxs-lookup"><span data-stu-id="8a2d2-114">Value</span></span>|<span data-ttu-id="8a2d2-115">说明</span><span class="sxs-lookup"><span data-stu-id="8a2d2-115">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="8a2d2-116">不创建 <xref:System.Security.Policy.Publisher> 证据。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-116">Does not create <xref:System.Security.Policy.Publisher> evidence.</span></span>|  
|`true`|<span data-ttu-id="8a2d2-117">创建 <xref:System.Security.Policy.Publisher> 证据。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-117">Creates <xref:System.Security.Policy.Publisher> evidence.</span></span> <span data-ttu-id="8a2d2-118">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-118">This is the default.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8a2d2-119">子元素</span><span class="sxs-lookup"><span data-stu-id="8a2d2-119">Child Elements</span></span>  

 <span data-ttu-id="8a2d2-120">无。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8a2d2-121">父元素</span><span class="sxs-lookup"><span data-stu-id="8a2d2-121">Parent Elements</span></span>  
  
|<span data-ttu-id="8a2d2-122">元素</span><span class="sxs-lookup"><span data-stu-id="8a2d2-122">Element</span></span>|<span data-ttu-id="8a2d2-123">说明</span><span class="sxs-lookup"><span data-stu-id="8a2d2-123">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="8a2d2-124">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-124">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="8a2d2-125">包含有关运行时初始化选项的信息。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-125">Contains information about runtime initialization options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8a2d2-126">备注</span><span class="sxs-lookup"><span data-stu-id="8a2d2-126">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="8a2d2-127">在 .NET Framework 4 及更高版本中，此元素对程序集加载时间没有影响。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-127">In the .NET Framework 4 and later, this element has no effect on assembly load times.</span></span> <span data-ttu-id="8a2d2-128">有关详细信息，请参阅 [安全更改](/previous-versions/dotnet/framework/security/security-changes)中的 "安全策略简化" 部分。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-128">For more information, see the "Security Policy Simplification" section in [Security Changes](/previous-versions/dotnet/framework/security/security-changes).</span></span>  
  
 <span data-ttu-id="8a2d2-129">公共语言运行时 (CLR) 尝试在加载时验证 Authenticode 签名，以创建 <xref:System.Security.Policy.Publisher> 程序集的证据。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-129">The common language runtime (CLR) tries to verify the Authenticode signature at load time to create <xref:System.Security.Policy.Publisher> evidence for the assembly.</span></span> <span data-ttu-id="8a2d2-130">但是，默认情况下，大多数应用程序不需要 <xref:System.Security.Policy.Publisher> 证据。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-130">However, by default, most applications do not need <xref:System.Security.Policy.Publisher> evidence.</span></span> <span data-ttu-id="8a2d2-131">标准 CAS 策略不依赖于 <xref:System.Security.Policy.PublisherMembershipCondition> 。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-131">Standard CAS policy does not rely on the <xref:System.Security.Policy.PublisherMembershipCondition>.</span></span> <span data-ttu-id="8a2d2-132">除非你的应用程序在具有自定义 CAS 策略的计算机上执行，或者要 <xref:System.Security.Permissions.PublisherIdentityPermission> 在部分信任环境中满足的要求，否则，应避免与验证发行者签名相关的不必要的启动成本。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-132">You should avoid the unnecessary startup cost associated with verifying the publisher signature unless your application executes on a computer with custom CAS policy, or is intending to satisfy demands for <xref:System.Security.Permissions.PublisherIdentityPermission> in a partial-trust environment.</span></span> <span data-ttu-id="8a2d2-133">在完全信任的环境中，标识权限的 (要求始终成功。 ) </span><span class="sxs-lookup"><span data-stu-id="8a2d2-133">(Demands for identity permissions always succeed in a full-trust environment.)</span></span>  
  
> [!NOTE]
> <span data-ttu-id="8a2d2-134">建议服务使用 `<generatePublisherEvidence>` 元素以提高启动性能。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-134">We recommend that services use the `<generatePublisherEvidence>` element to improve startup performance.</span></span>  <span data-ttu-id="8a2d2-135">使用此元素还有助于避免可能导致超时和取消服务启动的延迟。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-135">Using this element can also help avoid delays that can cause a time-out and the cancellation of the service startup.</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="8a2d2-136">配置文件</span><span class="sxs-lookup"><span data-stu-id="8a2d2-136">Configuration File</span></span>  

 <span data-ttu-id="8a2d2-137">此元素只能在应用程序配置文件中使用。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-137">This element can be used only in the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8a2d2-138">示例</span><span class="sxs-lookup"><span data-stu-id="8a2d2-138">Example</span></span>  

 <span data-ttu-id="8a2d2-139">下面的示例演示如何使用 `<generatePublisherEvidence>` 元素禁用应用程序的 CAS 发行者策略检查。</span><span class="sxs-lookup"><span data-stu-id="8a2d2-139">The following example shows how to use the `<generatePublisherEvidence>` element to disable checking for CAS publisher policy for an application.</span></span>  
  
```xml  
<configuration>  
    <runtime>  
        <generatePublisherEvidence enabled="false"/>  
    </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="8a2d2-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="8a2d2-140">See also</span></span>

- [<span data-ttu-id="8a2d2-141">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="8a2d2-141">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="8a2d2-142">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="8a2d2-142">Configuration File Schema</span></span>](../index.md)
