---
title: 如何使用 System.Text.Json 实例化 JsonSerializerOptions
description: 了解如何避免性能问题，以及如何对 JsonSerializerOptions 实例使用可用的构造函数。
ms.date: 12/02/2020
no-loc:
- System.Text.Json
- Newtonsoft.Json
zone_pivot_groups: dotnet-version
helpviewer_keywords:
- JSON serialization
- serializing objects
- serialization
- objects, serializing
ms.openlocfilehash: 5f32e1369e58dd9550f28abc822f187dee46c022
ms.sourcegitcommit: 81f1bba2c97a67b5ca76bcc57b37333ffca60c7b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2020
ms.locfileid: "97009828"
---
# <a name="how-to-instantiate-jsonserializeroptions-instances-with-no-locsystemtextjson"></a><span data-ttu-id="9c15e-103">如何使用 System.Text.Json 实例化 JsonSerializerOptions 实例</span><span class="sxs-lookup"><span data-stu-id="9c15e-103">How to instantiate JsonSerializerOptions instances with System.Text.Json</span></span>

<span data-ttu-id="9c15e-104">本文介绍如何避免在使用 <xref:System.Text.Json.JsonSerializerOptions> 时出现性能问题。</span><span class="sxs-lookup"><span data-stu-id="9c15e-104">This article explains how to avoid performance problems when you use <xref:System.Text.Json.JsonSerializerOptions>.</span></span> <span data-ttu-id="9c15e-105">还介绍了如何使用可用的参数化构造函数。</span><span class="sxs-lookup"><span data-stu-id="9c15e-105">It also shows how to use the parameterized constructors that are available.</span></span>

## <a name="reuse-jsonserializeroptions-instances"></a><span data-ttu-id="9c15e-106">重用 JsonSerializerOptions 实例</span><span class="sxs-lookup"><span data-stu-id="9c15e-106">Reuse JsonSerializerOptions instances</span></span>

<span data-ttu-id="9c15e-107">如果你通过相同的选项重复使用 `JsonSerializerOptions`，则请勿在每次使用时都创建新的 `JsonSerializerOptions` 实例。</span><span class="sxs-lookup"><span data-stu-id="9c15e-107">If you use `JsonSerializerOptions` repeatedly with the same options, don't create a new `JsonSerializerOptions` instance each time you use it.</span></span> <span data-ttu-id="9c15e-108">对每个调用重复使用同一实例。</span><span class="sxs-lookup"><span data-stu-id="9c15e-108">Reuse the same instance for every call.</span></span> <span data-ttu-id="9c15e-109">本指南适用于你为自定义转换器编写的代码，以及调用 <xref:System.Text.Json.JsonSerializer.Serialize%2A?displayProperty=nameWithType> 或 <xref:System.Text.Json.JsonSerializer.Deserialize%2A?displayProperty=nameWithType>时。</span><span class="sxs-lookup"><span data-stu-id="9c15e-109">This guidance applies to code you write for custom converters and when you call <xref:System.Text.Json.JsonSerializer.Serialize%2A?displayProperty=nameWithType> or <xref:System.Text.Json.JsonSerializer.Deserialize%2A?displayProperty=nameWithType>.</span></span>

<span data-ttu-id="9c15e-110">以下代码演示使用新的选项实例所带来的性能损失。</span><span class="sxs-lookup"><span data-stu-id="9c15e-110">The following code demonstrates the performance penalty for using new options instances.</span></span>

:::code language="csharp" source="snippets/system-text-json-configure-options/csharp/ReuseOptionsInstances.cs":::

<span data-ttu-id="9c15e-111">前面的代码使用相同的选项实例对一个小型对象进行了 100,000 次序列化。</span><span class="sxs-lookup"><span data-stu-id="9c15e-111">The preceding code serializes a small object 100,000 times using the same options instance.</span></span> <span data-ttu-id="9c15e-112">然后，它对相同的对象进行了相同次数的序列化，且每次都创建一个新的选项实例。</span><span class="sxs-lookup"><span data-stu-id="9c15e-112">Then it serializes the same object the same number of times and creates a new options instance each time.</span></span> <span data-ttu-id="9c15e-113">典型运行时的差值为 190 毫秒，而不是 40,140 毫秒。</span><span class="sxs-lookup"><span data-stu-id="9c15e-113">A typical run time difference is 190 compared to 40,140 milliseconds.</span></span> <span data-ttu-id="9c15e-114">如果增加迭代的次数，差值甚至越大。</span><span class="sxs-lookup"><span data-stu-id="9c15e-114">The difference is even greater if you increase the number of iterations.</span></span>

<span data-ttu-id="9c15e-115">当向序列化程序传递新的选项实例时，在对象图中每种类型的第一次序列化期间，序列化程序将执行一个预热阶段。</span><span class="sxs-lookup"><span data-stu-id="9c15e-115">The serializer undergoes a warm-up phase during the first serialization of each type in the object graph when a new options instance is passed to it.</span></span> <span data-ttu-id="9c15e-116">此预热包括创建序列化所需的元数据的缓存。</span><span class="sxs-lookup"><span data-stu-id="9c15e-116">This warm-up includes creating a cache of metadata that is needed for serialization.</span></span> <span data-ttu-id="9c15e-117">元数据包括对属性 Getter 的委托、Setter、构造函数参数、指定特性等。</span><span class="sxs-lookup"><span data-stu-id="9c15e-117">The metadata includes delegates to property getters, setters, constructor arguments, specified attributes, and so forth.</span></span> <span data-ttu-id="9c15e-118">此元数据缓存存储在选项实例中。</span><span class="sxs-lookup"><span data-stu-id="9c15e-118">This metadata cache is stored in the options instance.</span></span> <span data-ttu-id="9c15e-119">相同的预热过程和缓存适用于反序列化。</span><span class="sxs-lookup"><span data-stu-id="9c15e-119">The same warm-up process and cache applies to deserialization.</span></span>

<span data-ttu-id="9c15e-120">`JsonSerializerOptions` 实例中元数据缓存的大小取决于要序列化的类型的数量。</span><span class="sxs-lookup"><span data-stu-id="9c15e-120">The size of the metadata cache in a `JsonSerializerOptions` instance depends on the number of types to be serialized.</span></span> <span data-ttu-id="9c15e-121">如果向序列化程序传递多种类型（例如动态生成的类型），缓存大小将继续增长，最终可导致 `OutOfMemoryException`。</span><span class="sxs-lookup"><span data-stu-id="9c15e-121">If you pass numerous types—for example, dynamically generated types—to the serializer, the cache size will continue to grow and can end up causing an `OutOfMemoryException`.</span></span>

## <a name="copy-jsonserializeroptions"></a><span data-ttu-id="9c15e-122">复制 JsonSerializerOptions</span><span class="sxs-lookup"><span data-stu-id="9c15e-122">Copy JsonSerializerOptions</span></span>

::: zone pivot="dotnet-5-0"
<span data-ttu-id="9c15e-123">存在 [JsonSerializerOptions constructor](xref:System.Text.Json.JsonSerializerOptions.%23ctor(System.Text.Json.JsonSerializerOptions)) ，可让你使用与现有实例相同的选项来创建新的实例，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="9c15e-123">There is a [JsonSerializerOptions constructor](xref:System.Text.Json.JsonSerializerOptions.%23ctor(System.Text.Json.JsonSerializerOptions)) that lets you create a new instance with the same options as an existing instance, as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/CopyOptions.cs" highlight="29":::
::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="9c15e-124">使用现有实例的 `JsonSerializerOptions` 构造函数在 .NET Core 3.1 中不可用。</span><span class="sxs-lookup"><span data-stu-id="9c15e-124">A `JsonSerializerOptions` constructor that takes an existing instance is not available in .NET Core 3.1.</span></span>
::: zone-end

## <a name="web-defaults-for-jsonserializeroptions"></a><span data-ttu-id="9c15e-125">JsonSerializerOptions 的 Web 默认值</span><span class="sxs-lookup"><span data-stu-id="9c15e-125">Web defaults for JsonSerializerOptions</span></span>

::: zone pivot="dotnet-5-0"
<span data-ttu-id="9c15e-126">下面是具有 Web 应用不同默认值的选项：</span><span class="sxs-lookup"><span data-stu-id="9c15e-126">Here are the options that have different defaults for web apps:</span></span>

* <xref:System.Text.Json.JsonSerializerOptions.PropertyNameCaseInsensitive%2A> = `true`
* <xref:System.Text.Json.JsonNamingPolicy> = <xref:System.Text.Json.JsonNamingPolicy.CamelCase>
* <xref:System.Text.Json.JsonSerializerOptions.NumberHandling%2A> = <xref:System.Text.Json.Serialization.JsonNumberHandling.AllowReadingFromString>

<span data-ttu-id="9c15e-127">存在 [JsonSerializerOptions constructor](xref:System.Text.Json.JsonSerializerOptions.%23ctor(System.Text.Json.JsonSerializerDefaults)?view=net-5.0&preserve-view=true)，可让你通过 ASP.NET Core 对 Web 应用使用的默认选项创建新的实例，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="9c15e-127">There's a [JsonSerializerOptions constructor](xref:System.Text.Json.JsonSerializerOptions.%23ctor(System.Text.Json.JsonSerializerDefaults)?view=net-5.0&preserve-view=true) that lets you create a new instance with the default options that ASP.NET Core uses for web apps, as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/OptionsDefaults.cs" highlight="24":::
::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="9c15e-128">下面是具有 Web 应用不同默认值的选项：</span><span class="sxs-lookup"><span data-stu-id="9c15e-128">Here are the options that have different defaults for web apps:</span></span>

* <xref:System.Text.Json.JsonSerializerOptions.PropertyNameCaseInsensitive%2A> = `true`
* <xref:System.Text.Json.JsonNamingPolicy> = <xref:System.Text.Json.JsonNamingPolicy.CamelCase>

<span data-ttu-id="9c15e-129">指定一组默认值的 `JsonSerializerOptions` 构造函数在 .NET Core 3.1 中不可用。</span><span class="sxs-lookup"><span data-stu-id="9c15e-129">A `JsonSerializerOptions` constructor that specifies a set of defaults is not available in .NET Core 3.1.</span></span>
::: zone-end

## <a name="see-also"></a><span data-ttu-id="9c15e-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="9c15e-130">See also</span></span>

* [<span data-ttu-id="9c15e-131">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="9c15e-131">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="9c15e-132">如何对 JSON 进行序列化和反序列化</span><span class="sxs-lookup"><span data-stu-id="9c15e-132">How to serialize and deserialize JSON</span></span>](system-text-json-how-to.md)
* [<span data-ttu-id="9c15e-133">启用不区分大小写的匹配</span><span class="sxs-lookup"><span data-stu-id="9c15e-133">Enable case-insensitive matching</span></span>](system-text-json-character-casing.md)
* [<span data-ttu-id="9c15e-134">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="9c15e-134">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="9c15e-135">忽略属性</span><span class="sxs-lookup"><span data-stu-id="9c15e-135">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="9c15e-136">允许无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="9c15e-136">Allow invalid JSON</span></span>](system-text-json-invalid-json.md)
* [<span data-ttu-id="9c15e-137">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="9c15e-137">Handle overflow JSON</span></span>](system-text-json-handle-overflow.md)
* [<span data-ttu-id="9c15e-138">保留引用</span><span class="sxs-lookup"><span data-stu-id="9c15e-138">Preserve references</span></span>](system-text-json-preserve-references.md)
* [<span data-ttu-id="9c15e-139">不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="9c15e-139">Immutable types and non-public accessors</span></span>](system-text-json-immutability.md)
* [<span data-ttu-id="9c15e-140">多态序列化</span><span class="sxs-lookup"><span data-stu-id="9c15e-140">Polymorphic serialization</span></span>](system-text-json-polymorphism.md)
* [<span data-ttu-id="9c15e-141">从 Newtonsoft.Json 迁移到 System.Text.Json</span><span class="sxs-lookup"><span data-stu-id="9c15e-141">Migrate from Newtonsoft.Json to System.Text.Json</span></span>](system-text-json-migrate-from-newtonsoft-how-to.md)
* [<span data-ttu-id="9c15e-142">自定义字符编码</span><span class="sxs-lookup"><span data-stu-id="9c15e-142">Customize character encoding</span></span>](system-text-json-character-encoding.md)
* [<span data-ttu-id="9c15e-143">编写自定义序列化程序和反序列化程序</span><span class="sxs-lookup"><span data-stu-id="9c15e-143">Write custom serializers and deserializers</span></span>](write-custom-serializer-deserializer.md)
* [<span data-ttu-id="9c15e-144">编写用于 JSON 序列化的自定义转换器</span><span class="sxs-lookup"><span data-stu-id="9c15e-144">Write custom converters for JSON serialization</span></span>](system-text-json-converters-how-to.md)
* [<span data-ttu-id="9c15e-145">DateTime 和 DateTimeOffset 支持</span><span class="sxs-lookup"><span data-stu-id="9c15e-145">DateTime and DateTimeOffset support</span></span>](../datetime/system-text-json-support.md)
* <span data-ttu-id="9c15e-146">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="9c15e-146">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
* <span data-ttu-id="9c15e-147">[System.Text.Json.Serialization API 参考](xref:System.Text.Json.Serialization)</span><span class="sxs-lookup"><span data-stu-id="9c15e-147">[System.Text.Json.Serialization API reference](xref:System.Text.Json.Serialization)</span></span>
