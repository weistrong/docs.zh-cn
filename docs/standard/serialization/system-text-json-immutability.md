---
title: 如何通过 System.Text.Json 使用不可变类型和非公共访问器
description: 了解在 .NET 中序列化为 JSON 和从 JSON 进行反序列化时如何使用不可变类型和非公共访问器。
ms.date: 11/30/2020
no-loc:
- System.Text.Json
- Newtonsoft.Json
zone_pivot_groups: dotnet-version
helpviewer_keywords:
- JSON serialization
- serializing objects
- serialization
- objects, serializing
ms.openlocfilehash: ff8ecec0d70c877b7cbbd0297b85f0d9578ab828
ms.sourcegitcommit: 81f1bba2c97a67b5ca76bcc57b37333ffca60c7b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2020
ms.locfileid: "97008820"
---
# <a name="how-to-use-immutable-types-and-non-public-accessors-with-no-locsystemtextjson"></a><span data-ttu-id="64b67-103">如何通过 System.Text.Json 使用不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="64b67-103">How to use immutable types and non-public accessors with System.Text.Json</span></span>

<span data-ttu-id="64b67-104">本文将介绍如何通过 `System.Text.Json` 命名空间使用不可变类型（如“记录”）。</span><span class="sxs-lookup"><span data-stu-id="64b67-104">In this article, you will learn how to use immutable types, such as Records, with the `System.Text.Json` namespace.</span></span>

## <a name="immutable-types-and-records"></a><span data-ttu-id="64b67-105">不可变类型和记录</span><span class="sxs-lookup"><span data-stu-id="64b67-105">Immutable types and Records</span></span>

::: zone pivot="dotnet-5-0"
<span data-ttu-id="64b67-106">`System.Text.Json` 可以使用参数化构造函数，这可以反序列化不可变的类或结构。</span><span class="sxs-lookup"><span data-stu-id="64b67-106">`System.Text.Json` can use a parameterized constructor, which makes it possible to deserialize an immutable class or struct.</span></span> <span data-ttu-id="64b67-107">对于类，如果唯一构造函数是参数化的构造函数，则将使用该构造函数。</span><span class="sxs-lookup"><span data-stu-id="64b67-107">For a class, if the only constructor is a parameterized one, that constructor will be used.</span></span> <span data-ttu-id="64b67-108">对于结构或包含多个构造函数的类，通过应用 [[JsonConstructor]](xref:System.Text.Json.Serialization.JsonConstructorAttribute.%23ctor%2A) 特性来指定要使用的构造函数。</span><span class="sxs-lookup"><span data-stu-id="64b67-108">For a struct, or a class with multiple constructors, specify the one to use by applying the [[JsonConstructor]](xref:System.Text.Json.Serialization.JsonConstructorAttribute.%23ctor%2A) attribute.</span></span> <span data-ttu-id="64b67-109">如果未使用该特性，则始终使用公共无参数构造函数（如果存在）。</span><span class="sxs-lookup"><span data-stu-id="64b67-109">When the attribute is not used, a public parameterless constructor is always used if present.</span></span> <span data-ttu-id="64b67-110">该特性只能与公共构造函数一起使用。</span><span class="sxs-lookup"><span data-stu-id="64b67-110">The attribute can only be used with public constructors.</span></span> <span data-ttu-id="64b67-111">以下示例使用 `[JsonConstructor]` 特性：</span><span class="sxs-lookup"><span data-stu-id="64b67-111">The following example uses the `[JsonConstructor]` attribute:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/ImmutableTypes.cs" highlight="13":::

<span data-ttu-id="64b67-112">还支持 C# 9 记录，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="64b67-112">Records in C# 9 are also supported, as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/Records.cs":::

<span data-ttu-id="64b67-113">对于因其所有属性资源库都是非公共的而不可变的类型，请参阅以下部分，了解[非公共属性访问器](#non-public-property-accessors)。</span><span class="sxs-lookup"><span data-stu-id="64b67-113">For types that are immutable because all their property setters are non-public, see the following section about [non-public property accessors](#non-public-property-accessors).</span></span>
::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="64b67-114">.NET Core 3.1 不支持 `JsonConstructorAttribute` 和 C# 9 记录。</span><span class="sxs-lookup"><span data-stu-id="64b67-114">`JsonConstructorAttribute` and C# 9 Record support aren't available in .NET Core 3.1.</span></span>
::: zone-end

## <a name="non-public-property-accessors"></a><span data-ttu-id="64b67-115">非公共属性访问器</span><span class="sxs-lookup"><span data-stu-id="64b67-115">Non-public property accessors</span></span>

::: zone pivot="dotnet-5-0"
<span data-ttu-id="64b67-116">若要允许使用非公共属性访问器，请使用 [[JsonInclude]](xref:System.Text.Json.Serialization.JsonIncludeAttribute) 特性，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="64b67-116">To enable use of a non-public property accessor, use the [[JsonInclude]](xref:System.Text.Json.Serialization.JsonIncludeAttribute) attribute, as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/NonPublicAccessors.cs" highlight="12,15":::
::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="64b67-117">.NET Core 3.1 不支持非公共属性访问器。</span><span class="sxs-lookup"><span data-stu-id="64b67-117">Non-public property accessors are not supported in .NET Core 3.1.</span></span> <span data-ttu-id="64b67-118">有关详细信息，请参阅[从 Newtonsoft.Json 迁移一文](system-text-json-migrate-from-newtonsoft-how-to.md#non-public-property-setters-and-getters)。</span><span class="sxs-lookup"><span data-stu-id="64b67-118">For more information, see [the Migrate from Newtonsoft.Json article](system-text-json-migrate-from-newtonsoft-how-to.md#non-public-property-setters-and-getters).</span></span>
::: zone-end

## <a name="see-also"></a><span data-ttu-id="64b67-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="64b67-119">See also</span></span>

* [<span data-ttu-id="64b67-120">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="64b67-120">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="64b67-121">如何对 JSON 进行序列化和反序列化</span><span class="sxs-lookup"><span data-stu-id="64b67-121">How to serialize and deserialize JSON</span></span>](system-text-json-how-to.md)
* [<span data-ttu-id="64b67-122">对 JsonSerializerOptions 实例进行实例化</span><span class="sxs-lookup"><span data-stu-id="64b67-122">Instantiate JsonSerializerOptions instances</span></span>](system-text-json-configure-options.md)
* [<span data-ttu-id="64b67-123">启用不区分大小写的匹配</span><span class="sxs-lookup"><span data-stu-id="64b67-123">Enable case-insensitive matching</span></span>](system-text-json-character-casing.md)
* [<span data-ttu-id="64b67-124">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="64b67-124">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="64b67-125">忽略属性</span><span class="sxs-lookup"><span data-stu-id="64b67-125">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="64b67-126">允许无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="64b67-126">Allow invalid JSON</span></span>](system-text-json-invalid-json.md)
* [<span data-ttu-id="64b67-127">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="64b67-127">Handle overflow JSON</span></span>](system-text-json-handle-overflow.md)
* [<span data-ttu-id="64b67-128">保留引用</span><span class="sxs-lookup"><span data-stu-id="64b67-128">Preserve references</span></span>](system-text-json-preserve-references.md)
* [<span data-ttu-id="64b67-129">多态序列化</span><span class="sxs-lookup"><span data-stu-id="64b67-129">Polymorphic serialization</span></span>](system-text-json-polymorphism.md)
* [<span data-ttu-id="64b67-130">从 Newtonsoft.Json 迁移到 System.Text.Json</span><span class="sxs-lookup"><span data-stu-id="64b67-130">Migrate from Newtonsoft.Json to System.Text.Json</span></span>](system-text-json-migrate-from-newtonsoft-how-to.md)
* [<span data-ttu-id="64b67-131">自定义字符编码</span><span class="sxs-lookup"><span data-stu-id="64b67-131">Customize character encoding</span></span>](system-text-json-character-encoding.md)
* [<span data-ttu-id="64b67-132">编写自定义序列化程序和反序列化程序</span><span class="sxs-lookup"><span data-stu-id="64b67-132">Write custom serializers and deserializers</span></span>](write-custom-serializer-deserializer.md)
* [<span data-ttu-id="64b67-133">编写用于 JSON 序列化的自定义转换器</span><span class="sxs-lookup"><span data-stu-id="64b67-133">Write custom converters for JSON serialization</span></span>](system-text-json-converters-how-to.md)
* [<span data-ttu-id="64b67-134">DateTime 和 DateTimeOffset 支持</span><span class="sxs-lookup"><span data-stu-id="64b67-134">DateTime and DateTimeOffset support</span></span>](../datetime/system-text-json-support.md)
* <span data-ttu-id="64b67-135">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="64b67-135">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
* <span data-ttu-id="64b67-136">[System.Text.Json.Serialization API 参考](xref:System.Text.Json.Serialization)</span><span class="sxs-lookup"><span data-stu-id="64b67-136">[System.Text.Json.Serialization API reference](xref:System.Text.Json.Serialization)</span></span>
