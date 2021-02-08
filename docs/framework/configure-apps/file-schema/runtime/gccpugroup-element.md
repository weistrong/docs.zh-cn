---
description: 了解详细信息： <GCCpuGroup> 元素
title: <GCCpuGroup> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- GCCpuGroup element
- <GCCpuGroup> element
ms.assetid: c1fc7d6c-7220-475c-a312-5b8b201f66e0
ms.openlocfilehash: d4b3aa7084cbc2cb23b273bea95ffaec6e3a74d6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786988"
---
# <a name="gccpugroup-element"></a><span data-ttu-id="2b4d8-103">\<GCCpuGroup> 元素</span><span class="sxs-lookup"><span data-stu-id="2b4d8-103">\<GCCpuGroup> Element</span></span>

<span data-ttu-id="2b4d8-104">指定垃圾回收是否支持多个 CPU 组。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-104">Specifies whether garbage collection supports multiple CPU groups.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<GCCpuGroup>**

## <a name="syntax"></a><span data-ttu-id="2b4d8-105">语法</span><span class="sxs-lookup"><span data-stu-id="2b4d8-105">Syntax</span></span>

```xml
<GCCpuGroup
   enabled="true|false"/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="2b4d8-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="2b4d8-106">Attributes and Elements</span></span>

<span data-ttu-id="2b4d8-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="2b4d8-108">特性</span><span class="sxs-lookup"><span data-stu-id="2b4d8-108">Attributes</span></span>

|<span data-ttu-id="2b4d8-109">属性</span><span class="sxs-lookup"><span data-stu-id="2b4d8-109">Attribute</span></span>|<span data-ttu-id="2b4d8-110">描述</span><span class="sxs-lookup"><span data-stu-id="2b4d8-110">Description</span></span>|
|---------------|-----------------|
|`enabled`|<span data-ttu-id="2b4d8-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="2b4d8-112">指定垃圾回收是否支持多个 CPU 组。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-112">Specifies whether garbage collection supports multiple CPU groups.</span></span>|

## <a name="enabled-attribute"></a><span data-ttu-id="2b4d8-113">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="2b4d8-113">enabled Attribute</span></span>

|<span data-ttu-id="2b4d8-114">值</span><span class="sxs-lookup"><span data-stu-id="2b4d8-114">Value</span></span>|<span data-ttu-id="2b4d8-115">说明</span><span class="sxs-lookup"><span data-stu-id="2b4d8-115">Description</span></span>|
|-----------|-----------------|
|`false`|<span data-ttu-id="2b4d8-116">垃圾回收不支持多个 CPU 组。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-116">Garbage collection does not support multiple CPU groups.</span></span> <span data-ttu-id="2b4d8-117">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-117">This is the default.</span></span>|
|`true`|<span data-ttu-id="2b4d8-118">如果启用了服务器垃圾回收，则垃圾回收支持多个 CPU 组。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-118">Garbage collection supports multiple CPU groups, if server garbage collection is enabled.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="2b4d8-119">子元素</span><span class="sxs-lookup"><span data-stu-id="2b4d8-119">Child Elements</span></span>

<span data-ttu-id="2b4d8-120">无。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-120">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="2b4d8-121">父元素</span><span class="sxs-lookup"><span data-stu-id="2b4d8-121">Parent Elements</span></span>

|<span data-ttu-id="2b4d8-122">元素</span><span class="sxs-lookup"><span data-stu-id="2b4d8-122">Element</span></span>|<span data-ttu-id="2b4d8-123">说明</span><span class="sxs-lookup"><span data-stu-id="2b4d8-123">Description</span></span>|
|-------------|-----------------|
|`configuration`|<span data-ttu-id="2b4d8-124">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-124">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|
|`runtime`|<span data-ttu-id="2b4d8-125">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-125">Contains information about assembly binding and garbage collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2b4d8-126">备注</span><span class="sxs-lookup"><span data-stu-id="2b4d8-126">Remarks</span></span>

<span data-ttu-id="2b4d8-127">如果计算机具有多个 CPU 组并且启用了服务器垃圾回收 (请参阅 [\<gcServer>](gcserver-element.md) 元素) ，启用此元素可跨所有 CPU 组扩展垃圾回收，并在创建和平衡堆时考虑所有内核。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-127">When a computer has multiple CPU groups and server garbage collection is enabled (see the [\<gcServer>](gcserver-element.md) element), enabling this element extends garbage collection across all CPU groups and takes all cores into account when creating and balancing heaps.</span></span>

> [!NOTE]
> <span data-ttu-id="2b4d8-128">此元素仅适用于垃圾回收线程。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-128">This element applies only to garbage collection threads.</span></span> <span data-ttu-id="2b4d8-129">若要使运行时能够在所有 CPU 组之间分配用户线程，还必须启用该 [\<Thread_UseAllCpuGroups>](thread-useallcpugroups-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-129">To enable the runtime to distribute user threads across all CPU groups, you must also enable the [\<Thread_UseAllCpuGroups>](thread-useallcpugroups-element.md) element.</span></span>

## <a name="example"></a><span data-ttu-id="2b4d8-130">示例</span><span class="sxs-lookup"><span data-stu-id="2b4d8-130">Example</span></span>

<span data-ttu-id="2b4d8-131">下面的示例演示如何为多个 CPU 组启用垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="2b4d8-131">The following example shows how to enable garbage collection for multiple CPU groups.</span></span>

```xml
<configuration>
   <runtime>
      <GCCpuGroup enabled="true"/>
      <gcServer enabled="true"/>
   </runtime>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="2b4d8-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="2b4d8-132">See also</span></span>

- [<span data-ttu-id="2b4d8-133">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="2b4d8-133">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="2b4d8-134">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="2b4d8-134">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="2b4d8-135">禁用并发垃圾回收</span><span class="sxs-lookup"><span data-stu-id="2b4d8-135">Disable concurrent garbage collection</span></span>](gcconcurrent-element.md#to-disable-background-garbage-collection)
- [<span data-ttu-id="2b4d8-136">工作站和服务器垃圾回收</span><span class="sxs-lookup"><span data-stu-id="2b4d8-136">Workstation and server garbage collection</span></span>](../../../../standard/garbage-collection/workstation-server-gc.md)
