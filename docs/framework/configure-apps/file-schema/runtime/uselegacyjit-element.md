---
description: 了解详细信息： <useLegacyJit> 元素
title: <useLegacyJit> 元素
ms.date: 04/26/2017
ms.assetid: c2cf97f0-9262-4f1f-a754-5568b51110ad
ms.openlocfilehash: a1449cbc69f0aa1b91cc427fbfc5b984bf605169
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639999"
---
# <a name="uselegacyjit-element"></a><span data-ttu-id="74327-103">\<useLegacyJit> 元素</span><span class="sxs-lookup"><span data-stu-id="74327-103">\<useLegacyJit> Element</span></span>

<span data-ttu-id="74327-104">确定公共语言运行时是否使用实时编译的旧版 64 位 JIT 编译器。</span><span class="sxs-lookup"><span data-stu-id="74327-104">Determines whether the common language runtime uses the legacy 64-bit JIT compiler for just-in-time compilation.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<useLegacyJit>**  
  
## <a name="syntax"></a><span data-ttu-id="74327-105">语法</span><span class="sxs-lookup"><span data-stu-id="74327-105">Syntax</span></span>  
  
```xml
<useLegacyJit enabled=0|1 />
```

<span data-ttu-id="74327-106">元素名称 `useLegacyJit` 区分大小写。</span><span class="sxs-lookup"><span data-stu-id="74327-106">The element name `useLegacyJit` is case-sensitive.</span></span>
  
## <a name="attributes-and-elements"></a><span data-ttu-id="74327-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="74327-107">Attributes and elements</span></span>

<span data-ttu-id="74327-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="74327-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="74327-109">特性</span><span class="sxs-lookup"><span data-stu-id="74327-109">Attributes</span></span>  
  
| <span data-ttu-id="74327-110">属性</span><span class="sxs-lookup"><span data-stu-id="74327-110">Attribute</span></span> | <span data-ttu-id="74327-111">描述</span><span class="sxs-lookup"><span data-stu-id="74327-111">Description</span></span>                                                                                   |  
| --------- | --------------------------------------------------------------------------------------------- |  
| `enabled` | <span data-ttu-id="74327-112">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="74327-112">Required attribute.</span></span><br><br><span data-ttu-id="74327-113">指定运行时是否使用旧版64位 JIT 编译器。</span><span class="sxs-lookup"><span data-stu-id="74327-113">Specifies whether the runtime uses the legacy 64-bit JIT compiler.</span></span> |  
  
### <a name="enabled-attribute"></a><span data-ttu-id="74327-114">enabled 属性</span><span class="sxs-lookup"><span data-stu-id="74327-114">enabled attribute</span></span>  
  
| <span data-ttu-id="74327-115">值</span><span class="sxs-lookup"><span data-stu-id="74327-115">Value</span></span> | <span data-ttu-id="74327-116">说明</span><span class="sxs-lookup"><span data-stu-id="74327-116">Description</span></span>                                                                                                         |  
| ----- | ------------------------------------------------------------------------------------------------------------------- |  
| <span data-ttu-id="74327-117">0</span><span class="sxs-lookup"><span data-stu-id="74327-117">0</span></span>     | <span data-ttu-id="74327-118">公共语言运行时使用 .NET Framework 4.6 及更高版本中包含的新64位 JIT 编译器。</span><span class="sxs-lookup"><span data-stu-id="74327-118">The common language runtime uses the new 64-bit JIT compiler included in the .NET Framework 4.6 and later versions.</span></span> |  
| <span data-ttu-id="74327-119">1</span><span class="sxs-lookup"><span data-stu-id="74327-119">1</span></span>     | <span data-ttu-id="74327-120">公共语言运行时使用较旧的64位 JIT 编译器。</span><span class="sxs-lookup"><span data-stu-id="74327-120">The common language runtime uses the older 64-bit JIT compiler.</span></span>                                                     |  
  
### <a name="child-elements"></a><span data-ttu-id="74327-121">子元素</span><span class="sxs-lookup"><span data-stu-id="74327-121">Child elements</span></span>

<span data-ttu-id="74327-122">无</span><span class="sxs-lookup"><span data-stu-id="74327-122">None</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="74327-123">父元素</span><span class="sxs-lookup"><span data-stu-id="74327-123">Parent elements</span></span>  
  
| <span data-ttu-id="74327-124">元素</span><span class="sxs-lookup"><span data-stu-id="74327-124">Element</span></span>         | <span data-ttu-id="74327-125">说明</span><span class="sxs-lookup"><span data-stu-id="74327-125">Description</span></span>                                                                                                       |  
| --------------- | ----------------------------------------------------------------------------------------------------------------- |  
| `configuration` | <span data-ttu-id="74327-126">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="74327-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span> |  
| `runtime`       | <span data-ttu-id="74327-127">包含有关运行时初始化选项的信息。</span><span class="sxs-lookup"><span data-stu-id="74327-127">Contains information about runtime initialization options.</span></span>                                                        |  
  
## <a name="remarks"></a><span data-ttu-id="74327-128">备注</span><span class="sxs-lookup"><span data-stu-id="74327-128">Remarks</span></span>  

<span data-ttu-id="74327-129">从 .NET Framework 4.6 开始，公共语言运行时默认使用新的64位编译器来实时 (JIT) 编译。</span><span class="sxs-lookup"><span data-stu-id="74327-129">Starting with the .NET Framework 4.6, the common language runtime uses a new 64-bit compiler for Just-In-Time (JIT) compilation by default.</span></span> <span data-ttu-id="74327-130">在某些情况下，这可能会导致应用程序代码的行为与以前版本的64位 JIT 编译器进行 JIT 编译的行为不同。</span><span class="sxs-lookup"><span data-stu-id="74327-130">In some cases, this may result in a difference in behavior from application code that was JIT-compiled by the previous version of the 64-bit JIT compiler.</span></span> <span data-ttu-id="74327-131">通过将 `enabled` 元素的属性设置 `<useLegacyJit>` 为 `1` ，可以禁用新的64位 jit 编译器，而使用旧的64位 jit 编译器编译应用程序。</span><span class="sxs-lookup"><span data-stu-id="74327-131">By setting the `enabled` attribute of the `<useLegacyJit>` element to `1`, you can disable the new 64-bit JIT compiler and instead compile your app using the legacy 64-bit JIT compiler.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="74327-132">`<useLegacyJit>`元素仅影响64位 JIT 编译。</span><span class="sxs-lookup"><span data-stu-id="74327-132">The `<useLegacyJit>` element affects 64-bit JIT compilation only.</span></span> <span data-ttu-id="74327-133">与32位 JIT 编译器的编译不受影响。</span><span class="sxs-lookup"><span data-stu-id="74327-133">Compilation with the 32-bit JIT compiler is unaffected.</span></span>  
  
<span data-ttu-id="74327-134">您可以通过两种其他方法启用旧版64位 JIT 编译器，而不是使用配置文件设置：</span><span class="sxs-lookup"><span data-stu-id="74327-134">Instead of using a configuration file setting, you can enable the legacy 64-bit JIT compiler in two other ways:</span></span>  
  
- <span data-ttu-id="74327-135">设置环境变量</span><span class="sxs-lookup"><span data-stu-id="74327-135">Setting an environment variable</span></span>

  <span data-ttu-id="74327-136">将 `COMPLUS_useLegacyJit` 环境变量设置为 `0` (使用新的64位 jit 编译器) 或 `1` (使用较旧的64位 jit 编译器) ：</span><span class="sxs-lookup"><span data-stu-id="74327-136">Set the `COMPLUS_useLegacyJit` environment variable to either `0` (use the new 64-bit JIT compiler) or `1` (use the older 64-bit JIT compiler):</span></span>
  
  ```env  
  COMPLUS_useLegacyJit=0|1  
  ```  
  
  <span data-ttu-id="74327-137">环境变量具有 *全局作用域*，这意味着它会影响计算机上运行的所有应用程序。</span><span class="sxs-lookup"><span data-stu-id="74327-137">The environment variable has *global scope*, which means that it affects all applications run on the machine.</span></span> <span data-ttu-id="74327-138">如果已设置，则它可以被应用程序配置文件设置重写。</span><span class="sxs-lookup"><span data-stu-id="74327-138">If set, it can be overridden by the application configuration file setting.</span></span> <span data-ttu-id="74327-139">环境变量名称不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="74327-139">The environment variable name is not case-sensitive.</span></span>
  
- <span data-ttu-id="74327-140">添加注册表项</span><span class="sxs-lookup"><span data-stu-id="74327-140">Adding a registry key</span></span>

  <span data-ttu-id="74327-141">可以通过将 `REG_DWORD` 值添加到 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework` 注册表中的或键来启用旧的64位 JIT 编译器 `HKEY_CURRENT_USER\SOFTWARE\Microsoft\.NETFramework` 。</span><span class="sxs-lookup"><span data-stu-id="74327-141">You can enable the legacy 64-bit JIT compiler by adding a `REG_DWORD` value to either the `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework` or `HKEY_CURRENT_USER\SOFTWARE\Microsoft\.NETFramework` key in the registry.</span></span> <span data-ttu-id="74327-142">此值的名称为 `useLegacyJit` 。</span><span class="sxs-lookup"><span data-stu-id="74327-142">The value is named `useLegacyJit`.</span></span> <span data-ttu-id="74327-143">如果该值为0，则使用新编译器。</span><span class="sxs-lookup"><span data-stu-id="74327-143">If the value is 0, the new compiler is used.</span></span> <span data-ttu-id="74327-144">如果值为1，则启用旧版64位 JIT 编译器。</span><span class="sxs-lookup"><span data-stu-id="74327-144">If the value is 1, the legacy 64-bit JIT compiler is enabled.</span></span> <span data-ttu-id="74327-145">注册表值名称不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="74327-145">The registry value name is not case-sensitive.</span></span>
  
  <span data-ttu-id="74327-146">将该值添加到 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework` 密钥会影响计算机上运行的所有应用。</span><span class="sxs-lookup"><span data-stu-id="74327-146">Adding the value to the `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework` key affects all apps running on the machine.</span></span> <span data-ttu-id="74327-147">将该值添加到 `HKEY_CURRENT_USER\SOFTWARE\Microsoft\.NETFramework` 密钥会影响当前用户运行的所有应用。</span><span class="sxs-lookup"><span data-stu-id="74327-147">Adding the value to the `HKEY_CURRENT_USER\SOFTWARE\Microsoft\.NETFramework` key affects all apps run by the current user.</span></span> <span data-ttu-id="74327-148">如果使用多个用户帐户配置了计算机，则只有当前用户运行的应用才会受到影响，除非还将该值添加到其他用户的注册表项。</span><span class="sxs-lookup"><span data-stu-id="74327-148">If a machine is configured with multiple user accounts, only apps run by the current user are affected, unless the value is added to the registry keys for other users as well.</span></span> <span data-ttu-id="74327-149">如果将 `<useLegacyJit>` 元素添加到配置文件中，将重写注册表设置（如果存在）。</span><span class="sxs-lookup"><span data-stu-id="74327-149">Adding the `<useLegacyJit>` element to a configuration file overrides the registry settings, if they're present.</span></span>  
  
## <a name="example"></a><span data-ttu-id="74327-150">示例</span><span class="sxs-lookup"><span data-stu-id="74327-150">Example</span></span>  

<span data-ttu-id="74327-151">下面的配置文件使用新的64位 JIT 编译器禁用编译，而改用旧的64位 JIT 编译器。</span><span class="sxs-lookup"><span data-stu-id="74327-151">The following configuration file disables compilation with the new 64-bit JIT compiler and instead uses the legacy 64-bit JIT compiler.</span></span>  
  
```xml  
<?xml version ="1.0"?>  
<configuration>  
  <runtime>  
    <useLegacyJit enabled="1" />  
  </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="74327-152">请参阅</span><span class="sxs-lookup"><span data-stu-id="74327-152">See also</span></span>

- [<span data-ttu-id="74327-153">\<runtime> 元素</span><span class="sxs-lookup"><span data-stu-id="74327-153">\<runtime> Element</span></span>](runtime-element.md)
- [<span data-ttu-id="74327-154">\<configuration> 元素</span><span class="sxs-lookup"><span data-stu-id="74327-154">\<configuration> Element</span></span>](../configuration-element.md)
- [<span data-ttu-id="74327-155">缓解：新的 64 位 JIT 编译器</span><span class="sxs-lookup"><span data-stu-id="74327-155">Mitigation: New 64-bit JIT Compiler</span></span>](../../../migration-guide/mitigation-new-64-bit-jit-compiler.md)
