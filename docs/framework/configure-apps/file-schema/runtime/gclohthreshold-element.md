---
description: 了解详细信息： GCLOHThreshold 元素
title: GCLOHThreshold 元素
ms.date: 11/20/2019
helpviewer_keywords:
- GCLOHThreshold element
- <GCLOHThreshold> element
ms.openlocfilehash: 5d4ef4e6aaf44642c2307dc27ac2e99e966d3ad0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652804"
---
# <a name="gclohthreshold-element"></a><span data-ttu-id="db922-103">GCLOHThreshold 元素</span><span class="sxs-lookup"><span data-stu-id="db922-103">GCLOHThreshold element</span></span>

<span data-ttu-id="db922-104">指定阈值大小（以字节为单位），垃圾回收器将对象放置在大型对象堆上 (LOH) 。</span><span class="sxs-lookup"><span data-stu-id="db922-104">Specifies the threshold size, in bytes, that causes the garbage collector to put objects on the large object heap (LOH).</span></span>

[\<configuration>](../configuration-element.md)\
&nbsp;&nbsp;[\<runtime>](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;\<GCLOHThreshold>

## <a name="syntax"></a><span data-ttu-id="db922-105">语法</span><span class="sxs-lookup"><span data-stu-id="db922-105">Syntax</span></span>

```xml
<GCLOHThreshold
   enabled="nnnn"/>
```

## <a name="attributes"></a><span data-ttu-id="db922-106">特性</span><span class="sxs-lookup"><span data-stu-id="db922-106">Attributes</span></span>

|<span data-ttu-id="db922-107">属性</span><span class="sxs-lookup"><span data-stu-id="db922-107">Attribute</span></span>|<span data-ttu-id="db922-108">描述</span><span class="sxs-lookup"><span data-stu-id="db922-108">Description</span></span>|
|---------------|-----------------|
|`enabled`|<span data-ttu-id="db922-109">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="db922-109">Required attribute.</span></span><br /><br /><span data-ttu-id="db922-110">指定导致对象在大型对象堆上的阈值大小。</span><span class="sxs-lookup"><span data-stu-id="db922-110">Specifies the threshold size that causes objects to go on the large object heap.</span></span>|

### <a name="enabled-attribute"></a><span data-ttu-id="db922-111">enabled 属性</span><span class="sxs-lookup"><span data-stu-id="db922-111">enabled attribute</span></span>

|<span data-ttu-id="db922-112">值</span><span class="sxs-lookup"><span data-stu-id="db922-112">Value</span></span>|<span data-ttu-id="db922-113">说明</span><span class="sxs-lookup"><span data-stu-id="db922-113">Description</span></span>|
|-----------|-----------------|
|`nnnn`|<span data-ttu-id="db922-114">导致对象在大型对象堆上的阈值大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="db922-114">The threshold size, in bytes, that causes objects to go on the large object heap.</span></span>|

## <a name="child-elements"></a><span data-ttu-id="db922-115">子元素</span><span class="sxs-lookup"><span data-stu-id="db922-115">Child elements</span></span>

<span data-ttu-id="db922-116">无。</span><span class="sxs-lookup"><span data-stu-id="db922-116">None.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="db922-117">父元素</span><span class="sxs-lookup"><span data-stu-id="db922-117">Parent elements</span></span>

|<span data-ttu-id="db922-118">元素</span><span class="sxs-lookup"><span data-stu-id="db922-118">Element</span></span>|<span data-ttu-id="db922-119">说明</span><span class="sxs-lookup"><span data-stu-id="db922-119">Description</span></span>|
|-------------|-----------------|
|`configuration`|<span data-ttu-id="db922-120">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="db922-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|
|`runtime`|<span data-ttu-id="db922-121">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="db922-121">Contains information about assembly binding and garbage collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="db922-122">备注</span><span class="sxs-lookup"><span data-stu-id="db922-122">Remarks</span></span>

<span data-ttu-id="db922-123">.NET Framework 4.8 中引入了此设置。</span><span class="sxs-lookup"><span data-stu-id="db922-123">This setting was introduced in .NET Framework 4.8.</span></span>

## <a name="see-also"></a><span data-ttu-id="db922-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="db922-124">See also</span></span>

- [<span data-ttu-id="db922-125">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="db922-125">Run-time settings schema</span></span>](index.md)
- [<span data-ttu-id="db922-126">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="db922-126">Configuration file schema</span></span>](../index.md)
- [<span data-ttu-id="db922-127">垃圾回收的基本知识</span><span class="sxs-lookup"><span data-stu-id="db922-127">Fundamentals of garbage collection</span></span>](../../../../standard/garbage-collection/fundamentals.md)
- [<span data-ttu-id="db922-128">用于 GC 的 NET Core 运行时配置选项</span><span class="sxs-lookup"><span data-stu-id="db922-128">NET Core run-time config options for GC</span></span>](../../../../core/run-time-config/garbage-collector.md)
