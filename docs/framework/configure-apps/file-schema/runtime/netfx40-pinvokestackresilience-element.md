---
description: 了解详细信息： <NetFx40_PInvokeStackResilience> 元素
title: <NetFx40_PInvokeStackResilience> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- <NetFx40_PInvokeStackResilience> element
- NetFx40_PInvokeStackResilience element
ms.assetid: 39fb1588-72a4-4479-af74-0605233b68bd
ms.openlocfilehash: 59e2a5845868ebfa186344c9a731871739a29c47
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782294"
---
# <a name="netfx40_pinvokestackresilience-element"></a><span data-ttu-id="a0321-103">\<NetFx40_PInvokeStackResilience> 元素</span><span class="sxs-lookup"><span data-stu-id="a0321-103">\<NetFx40_PInvokeStackResilience> Element</span></span>

<span data-ttu-id="a0321-104">指定运行时是否以减慢托管和非托管代码之间的转换速度为代价，在运行时自动修复不正确的平台调用声明。</span><span class="sxs-lookup"><span data-stu-id="a0321-104">Specifies whether the runtime automatically fixes incorrect platform invoke declarations at run time, at the cost of slower transitions between managed and unmanaged code.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<NetFx40_PInvokeStackResilience>**  

## <a name="syntax"></a><span data-ttu-id="a0321-105">语法</span><span class="sxs-lookup"><span data-stu-id="a0321-105">Syntax</span></span>

```xml
<NetFx40_PInvokeStackResilience  enabled="1|0"/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a0321-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="a0321-106">Attributes and Elements</span></span>

<span data-ttu-id="a0321-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a0321-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="a0321-108">特性</span><span class="sxs-lookup"><span data-stu-id="a0321-108">Attributes</span></span>

|<span data-ttu-id="a0321-109">属性</span><span class="sxs-lookup"><span data-stu-id="a0321-109">Attribute</span></span>|<span data-ttu-id="a0321-110">描述</span><span class="sxs-lookup"><span data-stu-id="a0321-110">Description</span></span>|
|---------------|-----------------|
|`enabled`|<span data-ttu-id="a0321-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="a0321-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="a0321-112">指定运行时是否检测到不正确的平台调用声明，并在运行时在32位平台上自动修复堆栈。</span><span class="sxs-lookup"><span data-stu-id="a0321-112">Specifies whether the runtime detects incorrect platform invoke declarations and automatically fixes the stack at run time on 32-bit platforms.</span></span>|

## <a name="enabled-attribute"></a><span data-ttu-id="a0321-113">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="a0321-113">enabled Attribute</span></span>

|<span data-ttu-id="a0321-114">值</span><span class="sxs-lookup"><span data-stu-id="a0321-114">Value</span></span>|<span data-ttu-id="a0321-115">说明</span><span class="sxs-lookup"><span data-stu-id="a0321-115">Description</span></span>|
|-----------|-----------------|
|`0`|<span data-ttu-id="a0321-116">运行时使用 .NET Framework 4 中引入的更快互操作封送处理体系结构，该体系结构不会检测并修复不正确的平台调用声明。</span><span class="sxs-lookup"><span data-stu-id="a0321-116">The runtime uses the faster interop marshaling architecture introduced in the .NET Framework 4, which does not detect and fix incorrect platform invoke declarations.</span></span> <span data-ttu-id="a0321-117">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="a0321-117">This is the default.</span></span>|
|`1`|<span data-ttu-id="a0321-118">运行时使用检测并修复不正确的平台调用声明的慢速转换。</span><span class="sxs-lookup"><span data-stu-id="a0321-118">The runtime uses slower transitions that detect and fix incorrect platform invoke declarations.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="a0321-119">子元素</span><span class="sxs-lookup"><span data-stu-id="a0321-119">Child Elements</span></span>

<span data-ttu-id="a0321-120">无。</span><span class="sxs-lookup"><span data-stu-id="a0321-120">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="a0321-121">父元素</span><span class="sxs-lookup"><span data-stu-id="a0321-121">Parent Elements</span></span>

|<span data-ttu-id="a0321-122">元素</span><span class="sxs-lookup"><span data-stu-id="a0321-122">Element</span></span>|<span data-ttu-id="a0321-123">说明</span><span class="sxs-lookup"><span data-stu-id="a0321-123">Description</span></span>|
|-------------|-----------------|
|`configuration`|<span data-ttu-id="a0321-124">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="a0321-124">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|
|`runtime`|<span data-ttu-id="a0321-125">包含有关运行时初始化选项的信息。</span><span class="sxs-lookup"><span data-stu-id="a0321-125">Contains information about runtime initialization options.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a0321-126">备注</span><span class="sxs-lookup"><span data-stu-id="a0321-126">Remarks</span></span>

<span data-ttu-id="a0321-127">此元素使您能够以更快的互操作封送处理为依据不正确的平台调用声明来处理运行时复原。</span><span class="sxs-lookup"><span data-stu-id="a0321-127">This element enables you to trade faster interop marshaling for run-time resilience against incorrect platform invoke declarations.</span></span>

<span data-ttu-id="a0321-128">从 .NET Framework 4 开始，简化的互操作封送处理体系结构可为从托管代码到非托管代码的转换提供显著的性能改进。</span><span class="sxs-lookup"><span data-stu-id="a0321-128">Starting with the .NET Framework 4, a streamlined interop marshaling architecture provides a significant performance improvement for transitions from managed code to unmanaged code.</span></span> <span data-ttu-id="a0321-129">在 .NET Framework 的早期版本中，封送层在32位平台上检测到不正确的平台调用声明，并自动修复堆栈。</span><span class="sxs-lookup"><span data-stu-id="a0321-129">In earlier versions of the .NET Framework, the marshaling layer detected incorrect platform invoke declarations on 32-bit platforms and automatically fixed the stack.</span></span> <span data-ttu-id="a0321-130">新的封送处理体系结构消除了此步骤。</span><span class="sxs-lookup"><span data-stu-id="a0321-130">The new marshaling architecture eliminates this step.</span></span> <span data-ttu-id="a0321-131">因此，转换速度非常快，但不正确的平台调用声明可能导致程序失败。</span><span class="sxs-lookup"><span data-stu-id="a0321-131">As a result, transitions are very fast, but an incorrect platform invoke declaration can cause a program failure.</span></span>

<span data-ttu-id="a0321-132">为了便于在开发期间检测到不正确的声明，Visual Studio 调试体验也得到了改进。</span><span class="sxs-lookup"><span data-stu-id="a0321-132">To make it easy to detect incorrect declarations during development, the Visual Studio debugging experience has been improved.</span></span> <span data-ttu-id="a0321-133">当应用程序在附加调试器中运行时， [pInvokeStackImbalance](../../../debug-trace-profile/pinvokestackimbalance-mda.md) 托管调试助手 (MDA) 通知您不正确的平台调用声明。</span><span class="sxs-lookup"><span data-stu-id="a0321-133">The [pInvokeStackImbalance](../../../debug-trace-profile/pinvokestackimbalance-mda.md) managed debugging assistant (MDA) notifies you of incorrect platform invoke declarations when your application is running with the debugger attached.</span></span>

<span data-ttu-id="a0321-134">若要解决您的应用程序使用无法重新编译的组件，并且具有不正确的平台调用声明的情况，可以使用 `NetFx40_PInvokeStackResilience` 元素。</span><span class="sxs-lookup"><span data-stu-id="a0321-134">To address scenarios where your application uses components that you cannot recompile, and that have incorrect platform invoke declarations, you can use the `NetFx40_PInvokeStackResilience` element.</span></span> <span data-ttu-id="a0321-135">将此元素添加到应用程序配置文件中，并将其 `enabled="1"` "导入" 到兼容模式，并且具有较早版本的 .NET Framework 的行为，代价是慢于转换。</span><span class="sxs-lookup"><span data-stu-id="a0321-135">Adding this element to your application configuration file with `enabled="1"` opts into a compatibility mode with the behavior of earlier versions of the .NET Framework, at the cost of slower transitions.</span></span> <span data-ttu-id="a0321-136">已针对早期版本的 .NET Framework 编译的程序集会自动选择进入此兼容模式，并且不需要此元素。</span><span class="sxs-lookup"><span data-stu-id="a0321-136">Assemblies that have been compiled against earlier versions of the .NET Framework are automatically opted into this compatibility mode, and do not need this element.</span></span>

## <a name="configuration-file"></a><span data-ttu-id="a0321-137">配置文件</span><span class="sxs-lookup"><span data-stu-id="a0321-137">Configuration File</span></span>

<span data-ttu-id="a0321-138">此元素只能在应用程序配置文件中使用。</span><span class="sxs-lookup"><span data-stu-id="a0321-138">This element can be used only in the application configuration file.</span></span>

## <a name="example"></a><span data-ttu-id="a0321-139">示例</span><span class="sxs-lookup"><span data-stu-id="a0321-139">Example</span></span>

<span data-ttu-id="a0321-140">下面的示例演示如何针对应用程序的不正确的平台调用声明提高复原能力，降低了托管和非托管代码之间的转换速度。</span><span class="sxs-lookup"><span data-stu-id="a0321-140">The following example shows how to opt into increased resilience against incorrect platform invoke declarations for an application, at the cost of slower transitions between managed and unmanaged code.</span></span>

```xml
<configuration>
   <runtime>
      <NetFx40_PInvokeStackResilience enabled="1"/>
   </runtime>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="a0321-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="a0321-141">See also</span></span>

- [<span data-ttu-id="a0321-142">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="a0321-142">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="a0321-143">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="a0321-143">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="a0321-144">pInvokeStackImbalance</span><span class="sxs-lookup"><span data-stu-id="a0321-144">pInvokeStackImbalance</span></span>](../../../debug-trace-profile/pinvokestackimbalance-mda.md)
