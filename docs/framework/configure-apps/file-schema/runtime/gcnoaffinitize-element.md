---
description: 了解详细信息： <GCNoAffinitize> 元素
title: GCNoAffinitize 元素
ms.date: 11/08/2019
helpviewer_keywords:
- gcNoAffinitize element
- <gcNoAffinitize> element
ms.openlocfilehash: 139c0fd9e1ec829a3569b77a85e6526bec765e21
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754545"
---
# <a name="gcnoaffinitize-element"></a><span data-ttu-id="bad8d-103">\<GCNoAffinitize> 元素</span><span class="sxs-lookup"><span data-stu-id="bad8d-103">\<GCNoAffinitize> element</span></span>

<span data-ttu-id="bad8d-104">指定是否关联服务器 GC 线程与 Cpu。</span><span class="sxs-lookup"><span data-stu-id="bad8d-104">Specifies whether or not to affinitize server GC threads with CPUs.</span></span>

\<configuration>\
&nbsp;&nbsp;\<runtime>\
&nbsp;&nbsp;&nbsp;&nbsp;\<GCNoAffinitize>

## <a name="syntax"></a><span data-ttu-id="bad8d-105">语法</span><span class="sxs-lookup"><span data-stu-id="bad8d-105">Syntax</span></span>

```xml
<GCNoAffinitize
   enabled="true|false"/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bad8d-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="bad8d-106">Attributes and elements</span></span>

<span data-ttu-id="bad8d-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bad8d-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="bad8d-108">特性</span><span class="sxs-lookup"><span data-stu-id="bad8d-108">Attributes</span></span>

|<span data-ttu-id="bad8d-109">属性</span><span class="sxs-lookup"><span data-stu-id="bad8d-109">Attribute</span></span>|<span data-ttu-id="bad8d-110">描述</span><span class="sxs-lookup"><span data-stu-id="bad8d-110">Description</span></span>|
|---------------|-----------------|
|`enabled`|<span data-ttu-id="bad8d-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="bad8d-111">Required attribute.</span></span><br /><br /><span data-ttu-id="bad8d-112">指定服务器 GC 线程/堆是否与计算机上可用的处理器关联。</span><span class="sxs-lookup"><span data-stu-id="bad8d-112">Specifies whether server GC threads/heaps are affinitized with the processors available on the machine.</span></span>|

#### <a name="enabled-attribute"></a><span data-ttu-id="bad8d-113">enabled 属性</span><span class="sxs-lookup"><span data-stu-id="bad8d-113">enabled attribute</span></span>

|<span data-ttu-id="bad8d-114">值</span><span class="sxs-lookup"><span data-stu-id="bad8d-114">Value</span></span>|<span data-ttu-id="bad8d-115">说明</span><span class="sxs-lookup"><span data-stu-id="bad8d-115">Description</span></span>|
|-----------|-----------------|
|`false`|<span data-ttu-id="bad8d-116">包含 Cpu 的关联服务器 GC 线程。</span><span class="sxs-lookup"><span data-stu-id="bad8d-116">Affinitizes server GC threads with CPUs.</span></span> <span data-ttu-id="bad8d-117">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="bad8d-117">This is the default.</span></span>|
|`true`|<span data-ttu-id="bad8d-118">不关联具有 Cpu 的服务器垃圾回收线程。</span><span class="sxs-lookup"><span data-stu-id="bad8d-118">Does not affinitize server GC threads with CPUs.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="bad8d-119">子元素</span><span class="sxs-lookup"><span data-stu-id="bad8d-119">Child elements</span></span>

<span data-ttu-id="bad8d-120">无。</span><span class="sxs-lookup"><span data-stu-id="bad8d-120">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="bad8d-121">父元素</span><span class="sxs-lookup"><span data-stu-id="bad8d-121">Parent elements</span></span>

|<span data-ttu-id="bad8d-122">元素</span><span class="sxs-lookup"><span data-stu-id="bad8d-122">Element</span></span>|<span data-ttu-id="bad8d-123">说明</span><span class="sxs-lookup"><span data-stu-id="bad8d-123">Description</span></span>|
|-------------|-----------------|
|`configuration`|<span data-ttu-id="bad8d-124">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="bad8d-124">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|
|`runtime`|<span data-ttu-id="bad8d-125">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="bad8d-125">Contains information about assembly binding and garbage collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="bad8d-126">备注</span><span class="sxs-lookup"><span data-stu-id="bad8d-126">Remarks</span></span>

<span data-ttu-id="bad8d-127">默认情况下，服务器 GC 线程使用各自的 Cpu 进行关联。</span><span class="sxs-lookup"><span data-stu-id="bad8d-127">By default, server GC threads are hard-affinitized with their respective CPUs.</span></span> <span data-ttu-id="bad8d-128">系统的每个可用处理器都有其自己的 GC 堆和线程。</span><span class="sxs-lookup"><span data-stu-id="bad8d-128">Each of the system's available processors has its own GC heap and thread.</span></span> <span data-ttu-id="bad8d-129">这通常是首选的设置，因为它会优化缓存使用量。</span><span class="sxs-lookup"><span data-stu-id="bad8d-129">This is typically the preferred setting since it optimizes cache usage.</span></span> <span data-ttu-id="bad8d-130">从 .NET Framework 4.6.2 开始，通过将 **GCNoAffinitize** 元素的 `enabled` 属性设置为 `true` ，可以指定服务器 GC 线程和 cpu 不应紧耦合。</span><span class="sxs-lookup"><span data-stu-id="bad8d-130">Starting with .NET Framework 4.6.2, by setting the **GCNoAffinitize** element's `enabled` attribute to `true`, you can specify that server GC threads and CPUs should not be tightly coupled.</span></span>

<span data-ttu-id="bad8d-131">您可以单独指定 **GCNoAffinitize** 配置元素，以不关联服务器 GC 线程与 cpu 一起工作。</span><span class="sxs-lookup"><span data-stu-id="bad8d-131">You can specify the **GCNoAffinitize** configuration element alone to not affinitize server GC threads with CPUs.</span></span> <span data-ttu-id="bad8d-132">你还可以将它与 [GCHeapCount](gcheapcount-element.md) 元素结合使用，以控制应用程序使用的垃圾回收堆和线程的数目。</span><span class="sxs-lookup"><span data-stu-id="bad8d-132">You can also use it along with the [GCHeapCount](gcheapcount-element.md) element to control the number of GC heaps and threads used by an application.</span></span>

<span data-ttu-id="bad8d-133">如果 `enabled` **GCNoAffinitize** 元素的属性 `false` (其默认值) ，则还可以使用 [GCHeapCount](gcheapcount-element.md) 元素来指定 gc 线程和堆的数目，以及 [GCHeapAffinitizeMask](gcheapaffinitizemask-element.md) 元素，以指定垃圾回收器线程和堆关联的处理器。</span><span class="sxs-lookup"><span data-stu-id="bad8d-133">If the `enabled` attribute of the **GCNoAffinitize** element is `false` (its default value), you can also use the [GCHeapCount](gcheapcount-element.md) element to specify the number of GC threads and heaps, along with the [GCHeapAffinitizeMask](gcheapaffinitizemask-element.md) element to specify the processors to which the GC threads and heaps are affinitized.</span></span>

## <a name="example"></a><span data-ttu-id="bad8d-134">示例</span><span class="sxs-lookup"><span data-stu-id="bad8d-134">Example</span></span>

<span data-ttu-id="bad8d-135">以下示例不关联服务器 GC 线程：</span><span class="sxs-lookup"><span data-stu-id="bad8d-135">The following example does not hard-affinitize server GC threads:</span></span>

```xml
<configuration>
   <runtime>
      <gcServer enabled="true"/>
      <GCNoAffinitize enabled="true"/>
   </runtime>
</configuration>
```

<span data-ttu-id="bad8d-136">以下示例不关联服务器 GC 线程，并将 GC 堆/线程数限制为10：</span><span class="sxs-lookup"><span data-stu-id="bad8d-136">The following example does not affinitize server GC threads and limits the number of GC heaps/threads to 10:</span></span>

```xml
<configuration>
   <runtime>
      <gcServer enabled="true"/>
      <GCHeapCount enabled="10"/>
      <GCNoAffinitize enabled="true"/>
   </runtime>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="bad8d-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="bad8d-137">See also</span></span>

- <xref:System.Runtime.GCSettings.IsServerGC%2A?displayProperty=nameWithType>
- [<span data-ttu-id="bad8d-138">GCHeapAffinitizeMask 元素</span><span class="sxs-lookup"><span data-stu-id="bad8d-138">GCHeapAffinitizeMask element</span></span>](gcheapaffinitizemask-element.md)
- [<span data-ttu-id="bad8d-139">GCHeapCount 元素</span><span class="sxs-lookup"><span data-stu-id="bad8d-139">GCHeapCount element</span></span>](gcheapcount-element.md)
- [<span data-ttu-id="bad8d-140">垃圾回收的基本知识</span><span class="sxs-lookup"><span data-stu-id="bad8d-140">Fundamentals of garbage collection</span></span>](../../../../standard/garbage-collection/fundamentals.md)
- [<span data-ttu-id="bad8d-141">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="bad8d-141">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="bad8d-142">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="bad8d-142">Configuration File Schema</span></span>](../index.md)
