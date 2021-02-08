---
description: 了解详细信息： <NetFx45_CultureAwareComparerGetHashCode_LongStrings> 元素
title: <NetFx45_CultureAwareComparerGetHashCode_LongStrings> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- NetFx45_CultureAwareComparerGetHashCode_LongStrings element
- <NetFx45_CultureAwareComparerGetHashCode_LongStrings> element
- GetHashCode method
- hash codes, calculating
ms.assetid: 3a5f38d1-ebc8-44de-aaeb-2929f6e6b48f
ms.openlocfilehash: ca4099d3bf812cb25e6a611b9b51b3752b1ad361
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782281"
---
# <a name="netfx45_cultureawarecomparergethashcode_longstrings-element"></a><span data-ttu-id="496e4-103">\<NetFx45_CultureAwareComparerGetHashCode_LongStrings> 元素</span><span class="sxs-lookup"><span data-stu-id="496e4-103">\<NetFx45_CultureAwareComparerGetHashCode_LongStrings> Element</span></span>

<span data-ttu-id="496e4-104">指定运行时是否使用固定的内存量来计算 <xref:System.StringComparer.GetHashCode%2A?displayProperty=nameWithType> 方法的哈希代码。</span><span class="sxs-lookup"><span data-stu-id="496e4-104">Specifies whether the runtime uses a fixed amount of memory to calculate hash codes for the <xref:System.StringComparer.GetHashCode%2A?displayProperty=nameWithType> method.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<NetFx45_CultureAwareComparerGetHashCode_LongStrings>**  

## <a name="syntax"></a><span data-ttu-id="496e4-105">语法</span><span class="sxs-lookup"><span data-stu-id="496e4-105">Syntax</span></span>

```xml
<NetFx45_CultureAwareComparerGetHashCode_LongStrings enabled="0|1">
```

## <a name="attributes-and-elements"></a><span data-ttu-id="496e4-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="496e4-106">Attributes and Elements</span></span>

<span data-ttu-id="496e4-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="496e4-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="496e4-108">特性</span><span class="sxs-lookup"><span data-stu-id="496e4-108">Attributes</span></span>

|<span data-ttu-id="496e4-109">属性</span><span class="sxs-lookup"><span data-stu-id="496e4-109">Attribute</span></span>|<span data-ttu-id="496e4-110">描述</span><span class="sxs-lookup"><span data-stu-id="496e4-110">Description</span></span>|
|---------------|-----------------|
|`enabled`|<span data-ttu-id="496e4-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="496e4-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="496e4-112">指定公共语言运行时是否在计算哈希代码时分配固定的内存量。</span><span class="sxs-lookup"><span data-stu-id="496e4-112">Specifies whether the common language runtime allocates a fixed amount of memory when calculating hash codes.</span></span>|

## <a name="enabled-attribute"></a><span data-ttu-id="496e4-113">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="496e4-113">enabled Attribute</span></span>

|<span data-ttu-id="496e4-114">值</span><span class="sxs-lookup"><span data-stu-id="496e4-114">Value</span></span>|<span data-ttu-id="496e4-115">说明</span><span class="sxs-lookup"><span data-stu-id="496e4-115">Description</span></span>|
|-----------|-----------------|
|<span data-ttu-id="496e4-116">0</span><span class="sxs-lookup"><span data-stu-id="496e4-116">0</span></span>|<span data-ttu-id="496e4-117">公共语言运行时为 <xref:System.StringComparer.GetHashCode%2A?displayProperty=nameWithType> 方法分配可变的内存量来计算哈希代码。</span><span class="sxs-lookup"><span data-stu-id="496e4-117">The common language runtime allocates a variable amount of memory for the <xref:System.StringComparer.GetHashCode%2A?displayProperty=nameWithType> method to calculate hash codes.</span></span> <span data-ttu-id="496e4-118">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="496e4-118">This is the default.</span></span>|
|<span data-ttu-id="496e4-119">1</span><span class="sxs-lookup"><span data-stu-id="496e4-119">1</span></span>|<span data-ttu-id="496e4-120">公共语言运行时为 <xref:System.StringComparer.GetHashCode%2A?displayProperty=nameWithType> 方法分配固定的内存量来计算哈希代码。</span><span class="sxs-lookup"><span data-stu-id="496e4-120">The common language runtime allocates a fixed amount of memory for the <xref:System.StringComparer.GetHashCode%2A?displayProperty=nameWithType> method to calculate hash codes.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="496e4-121">子元素</span><span class="sxs-lookup"><span data-stu-id="496e4-121">Child Elements</span></span>

<span data-ttu-id="496e4-122">无。</span><span class="sxs-lookup"><span data-stu-id="496e4-122">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="496e4-123">父元素</span><span class="sxs-lookup"><span data-stu-id="496e4-123">Parent Elements</span></span>

|<span data-ttu-id="496e4-124">元素</span><span class="sxs-lookup"><span data-stu-id="496e4-124">Element</span></span>|<span data-ttu-id="496e4-125">说明</span><span class="sxs-lookup"><span data-stu-id="496e4-125">Description</span></span>|
|-------------|-----------------|
|`configuration`|<span data-ttu-id="496e4-126">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="496e4-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|
|`runtime`|<span data-ttu-id="496e4-127">包含有关运行时初始化选项的信息。</span><span class="sxs-lookup"><span data-stu-id="496e4-127">Contains information about runtime initialization options.</span></span>|

## <a name="remarks"></a><span data-ttu-id="496e4-128">备注</span><span class="sxs-lookup"><span data-stu-id="496e4-128">Remarks</span></span>

<span data-ttu-id="496e4-129">默认情况下，公共语言运行时将为 <xref:System.StringComparer.GetHashCode%2A?displayProperty=nameWithType> 方法分配可变的内存量，当该方法尝试计算非常大的字符串（几百万个字符以上）的哈希代码时，会引发 <xref:System.ArgumentException> 。</span><span class="sxs-lookup"><span data-stu-id="496e4-129">By default, the common language runtime allocates a variable amount of memory for the <xref:System.StringComparer.GetHashCode%2A?displayProperty=nameWithType> method, and an <xref:System.ArgumentException> can be thrown when the method attempts to compute the hash code of very large strings (over several million characters long).</span></span> <span data-ttu-id="496e4-130">通过将此元素添加到应用程序配置文件并将其 `enabled` 特性设置为“1”，你可以指定 <xref:System.StringComparer.GetHashCode%2A?displayProperty=nameWithType> 方法使用可分配固定内存量以计算哈希代码的替代算法。</span><span class="sxs-lookup"><span data-stu-id="496e4-130">By adding this element to an application configuration file and setting its `enabled` attribute to "1", you can specify that the <xref:System.StringComparer.GetHashCode%2A?displayProperty=nameWithType> method use an alternate algorithm that allocates a fixed amount of memory for the computation of hash codes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="496e4-131">`<NetFx45_CultureAwareComparerGetHashCode_LongStrings>`Windows 8 及更高版本中不使用元素。</span><span class="sxs-lookup"><span data-stu-id="496e4-131">The `<NetFx45_CultureAwareComparerGetHashCode_LongStrings>` element is not used in Windows 8 and later versions.</span></span>

## <a name="see-also"></a><span data-ttu-id="496e4-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="496e4-132">See also</span></span>

- <xref:System.StringComparer.GetHashCode%2A?displayProperty=nameWithType>
- [<span data-ttu-id="496e4-133">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="496e4-133">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="496e4-134">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="496e4-134">Configuration File Schema</span></span>](../index.md)
