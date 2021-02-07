---
description: 了解详细信息： <bypassTrustedAppStrongNames> 元素
title: <bypassTrustedAppStrongNames> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- strong-name bypass feature
- bypassTrustedAppStrongNames element
- strong-named assemblies, loading into trusted application domains
- <bypassTrustedAppStrongNames> element
ms.assetid: 71b2ebf6-3843-41e2-ad52-ffa5cd083a40
ms.openlocfilehash: d23b9efa19481027480f2a1c7dab22bc97a05e13
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99719157"
---
# <a name="bypasstrustedappstrongnames-element"></a><span data-ttu-id="6d2b1-103">\<bypassTrustedAppStrongNames> 元素</span><span class="sxs-lookup"><span data-stu-id="6d2b1-103">\<bypassTrustedAppStrongNames> Element</span></span>

<span data-ttu-id="6d2b1-104">指定是否在加载到完全信任的完全信任程序集上绕过强名称验证 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-104">Specifies whether to bypass the validation of strong names on full-trust assemblies that are loaded into a full-trust <xref:System.AppDomain>.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<bypassTrustedAppStrongNames>**

## <a name="syntax"></a><span data-ttu-id="6d2b1-105">语法</span><span class="sxs-lookup"><span data-stu-id="6d2b1-105">Syntax</span></span>

```xml
<bypassTrustedAppStrongNames
   enabled="true|false"/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="6d2b1-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6d2b1-106">Attributes and Elements</span></span>

<span data-ttu-id="6d2b1-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="6d2b1-108">特性</span><span class="sxs-lookup"><span data-stu-id="6d2b1-108">Attributes</span></span>

|<span data-ttu-id="6d2b1-109">属性</span><span class="sxs-lookup"><span data-stu-id="6d2b1-109">Attribute</span></span>|<span data-ttu-id="6d2b1-110">描述</span><span class="sxs-lookup"><span data-stu-id="6d2b1-110">Description</span></span>|
|---------------|-----------------|
|`enabled`|<span data-ttu-id="6d2b1-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="6d2b1-112">指定是否启用回避功能，以避免为完全信任程序集验证强名称。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-112">Specifies whether the bypass feature that avoids validating strong names for full-trust assemblies is enabled.</span></span> <span data-ttu-id="6d2b1-113">当启用此功能时，加载程序集时，不会验证强名称是否正确。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-113">When this feature is enabled, strong names are not validated for correctness when the assembly is loaded.</span></span> <span data-ttu-id="6d2b1-114">默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-114">The default is `true`.</span></span>|

## <a name="enabled-attribute"></a><span data-ttu-id="6d2b1-115">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="6d2b1-115">enabled Attribute</span></span>

|<span data-ttu-id="6d2b1-116">值</span><span class="sxs-lookup"><span data-stu-id="6d2b1-116">Value</span></span>|<span data-ttu-id="6d2b1-117">说明</span><span class="sxs-lookup"><span data-stu-id="6d2b1-117">Description</span></span>|
|-----------|-----------------|
|`true`|<span data-ttu-id="6d2b1-118">将程序集加载到完全信任时，不会验证完全信任程序集上的强名称签名 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-118">Strong-name signatures on full-trust assemblies are not validated when the assemblies are loaded into a full-trust <xref:System.AppDomain>.</span></span> <span data-ttu-id="6d2b1-119">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-119">This is the default.</span></span>|
|`false`|<span data-ttu-id="6d2b1-120">将程序集加载到完全信任时，会验证完全信任程序集上的强名称签名 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-120">Strong-name signatures on full-trust assemblies are validated when the assemblies are loaded into a full-trust <xref:System.AppDomain>.</span></span> <span data-ttu-id="6d2b1-121">仅对签名正确性检查强名称签名;与另一个匹配的强名称没有比较。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-121">The strong-name signature is checked only for signature correctness; it is not compared to another strong name for a match.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="6d2b1-122">子元素</span><span class="sxs-lookup"><span data-stu-id="6d2b1-122">Child Elements</span></span>

<span data-ttu-id="6d2b1-123">无。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-123">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="6d2b1-124">父元素</span><span class="sxs-lookup"><span data-stu-id="6d2b1-124">Parent Elements</span></span>

|<span data-ttu-id="6d2b1-125">元素</span><span class="sxs-lookup"><span data-stu-id="6d2b1-125">Element</span></span>|<span data-ttu-id="6d2b1-126">说明</span><span class="sxs-lookup"><span data-stu-id="6d2b1-126">Description</span></span>|
|-------------|-----------------|
|`configuration`|<span data-ttu-id="6d2b1-127">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-127">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|
|`runtime`|<span data-ttu-id="6d2b1-128">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-128">Contains information about assembly binding and garbage collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="6d2b1-129">备注</span><span class="sxs-lookup"><span data-stu-id="6d2b1-129">Remarks</span></span>

<span data-ttu-id="6d2b1-130">强名称跳过功能可避免完全信任程序集的强名称签名验证的系统开销。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-130">The strong-name bypass feature avoids the overhead of strong-name signature verification of full-trust assemblies.</span></span>

<span data-ttu-id="6d2b1-131">跳过功能适用于使用强名称进行签名及具有以下特征的任何程序集：</span><span class="sxs-lookup"><span data-stu-id="6d2b1-131">The bypass feature applies to any assembly that is signed with a strong name and that has the following characteristics:</span></span>

- <span data-ttu-id="6d2b1-132">完全受信任，无需 <xref:System.Security.Policy.StrongName> 证据 (例如，具有 `MyComputer` 区域证据) 。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-132">Fully trusted without the <xref:System.Security.Policy.StrongName> evidence (for example, has `MyComputer` zone evidence).</span></span>

- <span data-ttu-id="6d2b1-133">加载到完全受信任的 <xref:System.AppDomain>。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-133">Loaded into a fully trusted <xref:System.AppDomain>.</span></span>

- <span data-ttu-id="6d2b1-134">加载自该 <xref:System.AppDomain> 的 <xref:System.AppDomainSetup.ApplicationBase%2A> 属性下的某个位置。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-134">Loaded from a location under the <xref:System.AppDomainSetup.ApplicationBase%2A> property of that <xref:System.AppDomain>.</span></span>

- <span data-ttu-id="6d2b1-135">签名没有延迟。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-135">Not delay-signed.</span></span>

> [!NOTE]
> <span data-ttu-id="6d2b1-136">如果对计算机上的所有应用程序使用注册表项关闭了绕过功能，则此配置文件设置将不起作用。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-136">If the bypass feature has been turned off for all applications on the computer by using a registry key, this configuration file setting has no effect.</span></span> <span data-ttu-id="6d2b1-137">有关详细信息，请参阅 [如何：禁用 Strong-Name 绕过功能](../../../../standard/assembly/disable-strong-name-bypass-feature.md)。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-137">For more information, see [How to: Disable the Strong-Name Bypass Feature](../../../../standard/assembly/disable-strong-name-bypass-feature.md).</span></span>

## <a name="example"></a><span data-ttu-id="6d2b1-138">示例</span><span class="sxs-lookup"><span data-stu-id="6d2b1-138">Example</span></span>

<span data-ttu-id="6d2b1-139">下面的示例演示如何指定对完全信任程序集的强名称签名进行验证的行为。</span><span class="sxs-lookup"><span data-stu-id="6d2b1-139">The following example shows how to specify the behavior that validates the strong-name signature on full-trust assemblies.</span></span>

```xml
<configuration>
   <runtime>
      <bypassTrustedAppStrongNames enabled="false"/>
   </runtime>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="6d2b1-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="6d2b1-140">See also</span></span>

- [<span data-ttu-id="6d2b1-141">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="6d2b1-141">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="6d2b1-142">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="6d2b1-142">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="6d2b1-143">如何：禁用强名称跳过功能</span><span class="sxs-lookup"><span data-stu-id="6d2b1-143">How to: Disable the strong-name bypass feature</span></span>](../../../../standard/assembly/disable-strong-name-bypass-feature.md)
