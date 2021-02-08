---
description: 了解详细信息： <Thread_UseAllCpuGroups> 元素
title: <Thread_UseAllCpuGroups> 元素
ms.date: 03/30/2017
ms.assetid: d30fe7c5-8469-46e2-b804-e3eec7b24256
ms.openlocfilehash: 3f11ba6855caab25bd261de71c80c78232f2690f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802406"
---
# <a name="thread_useallcpugroups-element"></a><span data-ttu-id="f3b0d-103">\<Thread_UseAllCpuGroups> 元素</span><span class="sxs-lookup"><span data-stu-id="f3b0d-103">\<Thread_UseAllCpuGroups> Element</span></span>

<span data-ttu-id="f3b0d-104">指定运行时是否跨所有 CPU 组分发托管的线程。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-104">Specifies whether the runtime distributes managed threads across all CPU groups.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<Thread_UseAllCpuGroups>**  

## <a name="syntax"></a><span data-ttu-id="f3b0d-105">语法</span><span class="sxs-lookup"><span data-stu-id="f3b0d-105">Syntax</span></span>

```xml
<Thread_UseAllCpuGroups
   enabled="true|false"/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f3b0d-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f3b0d-106">Attributes and Elements</span></span>

<span data-ttu-id="f3b0d-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="f3b0d-108">特性</span><span class="sxs-lookup"><span data-stu-id="f3b0d-108">Attributes</span></span>

|<span data-ttu-id="f3b0d-109">属性</span><span class="sxs-lookup"><span data-stu-id="f3b0d-109">Attribute</span></span>|<span data-ttu-id="f3b0d-110">描述</span><span class="sxs-lookup"><span data-stu-id="f3b0d-110">Description</span></span>|
|---------------|-----------------|
|`enabled`|<span data-ttu-id="f3b0d-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="f3b0d-112">指定运行时是否跨所有 CPU 组分发托管的线程。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-112">Specifies whether the runtime distributes managed threads across all CPU groups.</span></span>|

## <a name="enabled-attribute"></a><span data-ttu-id="f3b0d-113">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="f3b0d-113">enabled Attribute</span></span>

|<span data-ttu-id="f3b0d-114">值</span><span class="sxs-lookup"><span data-stu-id="f3b0d-114">Value</span></span>|<span data-ttu-id="f3b0d-115">说明</span><span class="sxs-lookup"><span data-stu-id="f3b0d-115">Description</span></span>|
|-----------|-----------------|
|`false`|<span data-ttu-id="f3b0d-116">运行时不会跨多个 CPU 组分发托管线程。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-116">The runtime does not distribute managed threads across multiple CPU groups.</span></span> <span data-ttu-id="f3b0d-117">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-117">This is the default.</span></span>|
|`true`|<span data-ttu-id="f3b0d-118">如果计算机具有多个 CPU 组并且元素已启用，则运行时将跨多个 CPU 组分发托管线程 [\<GCCpuGroup>](gccpugroup-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-118">The runtime distributes managed threads across multiple CPU groups, if the computer has multiple CPU groups and the [\<GCCpuGroup>](gccpugroup-element.md) element is enabled.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="f3b0d-119">子元素</span><span class="sxs-lookup"><span data-stu-id="f3b0d-119">Child Elements</span></span>

<span data-ttu-id="f3b0d-120">无。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-120">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="f3b0d-121">父元素</span><span class="sxs-lookup"><span data-stu-id="f3b0d-121">Parent Elements</span></span>

|<span data-ttu-id="f3b0d-122">元素</span><span class="sxs-lookup"><span data-stu-id="f3b0d-122">Element</span></span>|<span data-ttu-id="f3b0d-123">说明</span><span class="sxs-lookup"><span data-stu-id="f3b0d-123">Description</span></span>|
|-------------|-----------------|
|`configuration`|<span data-ttu-id="f3b0d-124">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-124">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|
|`runtime`|<span data-ttu-id="f3b0d-125">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-125">Contains information about assembly binding and garbage collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f3b0d-126">备注</span><span class="sxs-lookup"><span data-stu-id="f3b0d-126">Remarks</span></span>

<span data-ttu-id="f3b0d-127">如果计算机具有多个 CPU 组，则启用此元素会使运行时将托管线程分散到所有 CPU 组。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-127">When a computer has multiple CPU groups, enabling this element causes the runtime to distribute managed threads across all CPU groups.</span></span> <span data-ttu-id="f3b0d-128">若要使用此功能，还必须启用 [\<GCCpuGroup>](gccpugroup-element.md) 元素，该元素将垃圾回收扩展到所有 CPU 组，并在创建和平衡堆时考虑所有核心。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-128">To use this feature, you must also enable the [\<GCCpuGroup>](gccpugroup-element.md) element, which extends garbage collection to all CPU groups and takes all cores into account when creating and balancing heaps.</span></span> <span data-ttu-id="f3b0d-129">启用 [\<GCCpuGroup>](gccpugroup-element.md) 元素需要启用 [\<gcServer>](gcserver-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-129">Enabling the [\<GCCpuGroup>](gccpugroup-element.md) element requires enabling the [\<gcServer>](gcserver-element.md) element.</span></span> <span data-ttu-id="f3b0d-130">如果未启用这些元素，则启用 `<Thread_UseAllCpuGroups>` 元素不起作用。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-130">If these elements are not enabled, enabling the `<Thread_UseAllCpuGroups>` element has no effect.</span></span>

## <a name="example"></a><span data-ttu-id="f3b0d-131">示例</span><span class="sxs-lookup"><span data-stu-id="f3b0d-131">Example</span></span>

<span data-ttu-id="f3b0d-132">下面的示例演示如何启用对多个 CPU 组的支持。</span><span class="sxs-lookup"><span data-stu-id="f3b0d-132">The following example shows how to enable support for multiple CPU groups.</span></span>

```xml
<configuration>
   <runtime>
      <Thread_UseAllCpuGroups enabled="true"/>
      <GCCpuGroup enabled="true"/>
      <gcServer enabled="true"/>
   </runtime>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="f3b0d-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="f3b0d-133">See also</span></span>

- [<span data-ttu-id="f3b0d-134">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="f3b0d-134">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="f3b0d-135">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="f3b0d-135">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="f3b0d-136">\<GCCpuGroup> 元素</span><span class="sxs-lookup"><span data-stu-id="f3b0d-136">\<GCCpuGroup> Element</span></span>](gccpugroup-element.md)
