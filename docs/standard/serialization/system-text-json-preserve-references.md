---
title: 如何使用 System.Text.Json 保留引用
description: 了解在 .NET 中序列化为 JSON 和从 JSON 进行反序列化时如何保留引用并处理循环引用。
ms.date: 12/09/2020
no-loc:
- System.Text.Json
- Newtonsoft.Json
zone_pivot_groups: dotnet-version
helpviewer_keywords:
- JSON serialization
- serializing objects
- serialization
- objects, serializing
ms.openlocfilehash: d358c953c0979ca097c080fcd750d5ef95b07de0
ms.sourcegitcommit: 81f1bba2c97a67b5ca76bcc57b37333ffca60c7b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2020
ms.locfileid: "97008729"
---
# <a name="how-to-preserve-references-and-handle-circular-references-with-no-locsystemtextjson"></a><span data-ttu-id="b11fe-103">如何使用 System.Text.Json 保留引用并处理循环引用</span><span class="sxs-lookup"><span data-stu-id="b11fe-103">How to preserve references and handle circular references with System.Text.Json</span></span>

::: zone pivot="dotnet-5-0"

<span data-ttu-id="b11fe-104">若要保留引用并处理循环引用，请将 <xref:System.Text.Json.JsonSerializerOptions.ReferenceHandler%2A> 设置为 <xref:System.Text.Json.Serialization.ReferenceHandler.Preserve%2A>。</span><span class="sxs-lookup"><span data-stu-id="b11fe-104">To preserve references and handle circular references, set <xref:System.Text.Json.JsonSerializerOptions.ReferenceHandler%2A> to <xref:System.Text.Json.Serialization.ReferenceHandler.Preserve%2A>.</span></span> <span data-ttu-id="b11fe-105">此设置会导致以下行为：</span><span class="sxs-lookup"><span data-stu-id="b11fe-105">This setting causes the following behavior:</span></span>

* <span data-ttu-id="b11fe-106">在序列化时：</span><span class="sxs-lookup"><span data-stu-id="b11fe-106">On serialize:</span></span>

  <span data-ttu-id="b11fe-107">编写复杂类型时，序列化程序还会写入元数据属性（`$id`、`$values` 和 `$ref`）。</span><span class="sxs-lookup"><span data-stu-id="b11fe-107">When writing complex types, the serializer also writes metadata properties (`$id`, `$values`, and `$ref`).</span></span>

* <span data-ttu-id="b11fe-108">在反序列化时：</span><span class="sxs-lookup"><span data-stu-id="b11fe-108">On deserialize:</span></span>

  <span data-ttu-id="b11fe-109">需要元数据（虽然不是必需的），并且反序列化程序会尝试理解它。</span><span class="sxs-lookup"><span data-stu-id="b11fe-109">Metadata is expected (although not mandatory), and the deserializer tries to understand it.</span></span>

<span data-ttu-id="b11fe-110">下面的代码演示 `Preserve` 属性的用法。</span><span class="sxs-lookup"><span data-stu-id="b11fe-110">The following code illustrates use of the `Preserve` setting.</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/PreserveReferences.cs" highlight="34":::

<span data-ttu-id="b11fe-111">此功能不能用于保留值类型或不可变类型。</span><span class="sxs-lookup"><span data-stu-id="b11fe-111">This feature can't be used to preserve value types or immutable types.</span></span> <span data-ttu-id="b11fe-112">在反序列化时，将在读取整个有效负载后创建不可变类型的实例。</span><span class="sxs-lookup"><span data-stu-id="b11fe-112">On deserialization, the instance of an immutable type is created after the entire payload is read.</span></span> <span data-ttu-id="b11fe-113">因此，如果对同一实例的引用出现在 JSON 有效负载中，则无法对其进行反序列化。</span><span class="sxs-lookup"><span data-stu-id="b11fe-113">So it would be impossible to deserialize the same instance if a reference to it appears within the JSON payload.</span></span>

<span data-ttu-id="b11fe-114">对于值类型、不可变类型和数组，不会序列化任何引用元数据。</span><span class="sxs-lookup"><span data-stu-id="b11fe-114">For value types, immutable types, and arrays, no reference metadata is serialized.</span></span> <span data-ttu-id="b11fe-115">反序列化时，如果发现 `$ref` 或 `$id`，则会引发异常。</span><span class="sxs-lookup"><span data-stu-id="b11fe-115">On deserialization, an exception is thrown if `$ref` or `$id` is found.</span></span> <span data-ttu-id="b11fe-116">但是，值类型忽略 `$id`（对于集合，则为 `$values`），以便可以反序列化使用 Newtonsoft.Json 序列化的有效负载。</span><span class="sxs-lookup"><span data-stu-id="b11fe-116">However, value types ignore `$id` (and `$values` in the case of collections) to make it possible to deserialize payloads that were serialized by using Newtonsoft.Json.</span></span>  <span data-ttu-id="b11fe-117">Newtonsoft.Json 为此类类型序列化元数据。</span><span class="sxs-lookup"><span data-stu-id="b11fe-117">Newtonsoft.Json does serialize metadata for such types.</span></span>

<span data-ttu-id="b11fe-118">为了确定对象是否相等，System.Text.Json 在比较两个对象实例时使用引用相等性 (<xref:System.Object.ReferenceEquals(System.Object,System.Object)?displayProperty=nameWithType>) 而不是值相等性 (<xref:System.Object.Equals(System.Object)?displayProperty=nameWithType> 的 <xref:System.Collections.Generic.ReferenceEqualityComparer.Instance%2A?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="b11fe-118">To determine if objects are equal, System.Text.Json uses <xref:System.Collections.Generic.ReferenceEqualityComparer.Instance%2A?displayProperty=nameWithType>, which uses reference equality (<xref:System.Object.ReferenceEquals(System.Object,System.Object)?displayProperty=nameWithType>) instead of value equality (<xref:System.Object.Equals(System.Object)?displayProperty=nameWithType> when comparing two object instances.</span></span>

<span data-ttu-id="b11fe-119">有关如何序列化和反序列化引用的详细信息，请参阅 <xref:System.Text.Json.Serialization.ReferenceHandler.Preserve%2A?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="b11fe-119">For more information about how references are serialized and deserialized, see <xref:System.Text.Json.Serialization.ReferenceHandler.Preserve%2A?displayProperty=nameWithType>.</span></span>

<span data-ttu-id="b11fe-120"><xref:System.Text.Json.Serialization.ReferenceResolver> 类定义在序列化和反序列化过程中保留引用的行为。</span><span class="sxs-lookup"><span data-stu-id="b11fe-120">The <xref:System.Text.Json.Serialization.ReferenceResolver> class defines the behavior of preserving references on serialization and deserialization.</span></span> <span data-ttu-id="b11fe-121">创建派生类以指定自定义行为。</span><span class="sxs-lookup"><span data-stu-id="b11fe-121">Create a derived class to specify custom behavior.</span></span> <span data-ttu-id="b11fe-122">有关示例，请参阅 [GuidReferenceResolver](https://github.com/dotnet/docs/blob/9d5e88edbd7f12be463775ffebbf07ac8415fe18/docs/standard/serialization/snippets/system-text-json-how-to-5-0/csharp/GuidReferenceResolverExample.cs)。</span><span class="sxs-lookup"><span data-stu-id="b11fe-122">For an example, see [GuidReferenceResolver](https://github.com/dotnet/docs/blob/9d5e88edbd7f12be463775ffebbf07ac8415fe18/docs/standard/serialization/snippets/system-text-json-how-to-5-0/csharp/GuidReferenceResolverExample.cs).</span></span>

::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="b11fe-123">.NET Core 3.1 中的 System.Text.Json 仅支持按值进行进行序列化，并对循环引用引发异常。</span><span class="sxs-lookup"><span data-stu-id="b11fe-123">System.Text.Json in .NET Core 3.1 only supports serialization by value and throws an exception for circular references.</span></span>
::: zone-end

## <a name="see-also"></a><span data-ttu-id="b11fe-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="b11fe-124">See also</span></span>

* [<span data-ttu-id="b11fe-125">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="b11fe-125">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="b11fe-126">如何对 JSON 进行序列化和反序列化</span><span class="sxs-lookup"><span data-stu-id="b11fe-126">How to serialize and deserialize JSON</span></span>](system-text-json-how-to.md)
* [<span data-ttu-id="b11fe-127">对 JsonSerializerOptions 实例进行实例化</span><span class="sxs-lookup"><span data-stu-id="b11fe-127">Instantiate JsonSerializerOptions instances</span></span>](system-text-json-configure-options.md)
* [<span data-ttu-id="b11fe-128">启用不区分大小写的匹配</span><span class="sxs-lookup"><span data-stu-id="b11fe-128">Enable case-insensitive matching</span></span>](system-text-json-character-casing.md)
* [<span data-ttu-id="b11fe-129">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="b11fe-129">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="b11fe-130">忽略属性</span><span class="sxs-lookup"><span data-stu-id="b11fe-130">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="b11fe-131">允许无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="b11fe-131">Allow invalid JSON</span></span>](system-text-json-invalid-json.md)
* [<span data-ttu-id="b11fe-132">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="b11fe-132">Handle overflow JSON</span></span>](system-text-json-handle-overflow.md)
* [<span data-ttu-id="b11fe-133">不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="b11fe-133">Immutable types and non-public accessors</span></span>](system-text-json-immutability.md)
* [<span data-ttu-id="b11fe-134">多态序列化</span><span class="sxs-lookup"><span data-stu-id="b11fe-134">Polymorphic serialization</span></span>](system-text-json-polymorphism.md)
* [<span data-ttu-id="b11fe-135">从 Newtonsoft.Json 迁移到 System.Text.Json</span><span class="sxs-lookup"><span data-stu-id="b11fe-135">Migrate from Newtonsoft.Json to System.Text.Json</span></span>](system-text-json-migrate-from-newtonsoft-how-to.md)
* [<span data-ttu-id="b11fe-136">自定义字符编码</span><span class="sxs-lookup"><span data-stu-id="b11fe-136">Customize character encoding</span></span>](system-text-json-character-encoding.md)
* [<span data-ttu-id="b11fe-137">编写自定义序列化程序和反序列化程序</span><span class="sxs-lookup"><span data-stu-id="b11fe-137">Write custom serializers and deserializers</span></span>](write-custom-serializer-deserializer.md)
* [<span data-ttu-id="b11fe-138">编写用于 JSON 序列化的自定义转换器</span><span class="sxs-lookup"><span data-stu-id="b11fe-138">Write custom converters for JSON serialization</span></span>](system-text-json-converters-how-to.md)
* [<span data-ttu-id="b11fe-139">DateTime 和 DateTimeOffset 支持</span><span class="sxs-lookup"><span data-stu-id="b11fe-139">DateTime and DateTimeOffset support</span></span>](../datetime/system-text-json-support.md)
* <span data-ttu-id="b11fe-140">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="b11fe-140">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
* <span data-ttu-id="b11fe-141">[System.Text.Json.Serialization API 参考](xref:System.Text.Json.Serialization)</span><span class="sxs-lookup"><span data-stu-id="b11fe-141">[System.Text.Json.Serialization API reference](xref:System.Text.Json.Serialization)</span></span>
