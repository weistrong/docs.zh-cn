---
title: 如何使用 System.Text.Json 启用不区分大小写的属性名称
description: 了解在 .NET 中序列化为 JSON 和从 JSON 进行反序列化时如何启用不区分大小写的属性名称匹配。
ms.date: 11/30/2020
no-loc:
- System.Text.Json
- Newtonsoft.Json
helpviewer_keywords:
- JSON serialization
- serializing objects
- serialization
- objects, serializing
ms.openlocfilehash: 3e2fb8cbdd35e772b5e97c731199f69aa834bd0a
ms.sourcegitcommit: 81f1bba2c97a67b5ca76bcc57b37333ffca60c7b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2020
ms.locfileid: "97009737"
---
# <a name="how-to-enable-case-insensitive-property-name-matching-with-no-locsystemtextjson"></a><span data-ttu-id="e0bfa-103">如何使用 System.Text.Json 启用不区分大小写的属性名称</span><span class="sxs-lookup"><span data-stu-id="e0bfa-103">How to enable case-insensitive property name matching with System.Text.Json</span></span>

<span data-ttu-id="e0bfa-104">本文将介绍如何使用 `System.Text.Json` 命名空间启用不区分大小写的属性名称匹配。</span><span class="sxs-lookup"><span data-stu-id="e0bfa-104">In this article, you will learn how to enable case-insensitive property name matching with the `System.Text.Json` namespace.</span></span>

## <a name="case-insensitive-property-matching"></a><span data-ttu-id="e0bfa-105">不区分大小写的属性匹配</span><span class="sxs-lookup"><span data-stu-id="e0bfa-105">Case-insensitive property matching</span></span>

<span data-ttu-id="e0bfa-106">默认情况下，反序列化会查找 JSON 与目标对象属性之间区分大小写的属性名称匹配。</span><span class="sxs-lookup"><span data-stu-id="e0bfa-106">By default, deserialization looks for case-sensitive property name matches between JSON and the target object properties.</span></span> <span data-ttu-id="e0bfa-107">若要更改该行为，请将 <xref:System.Text.Json.JsonSerializerOptions.PropertyNameCaseInsensitive?displayProperty=nameWithType> 设置为 `true`：</span><span class="sxs-lookup"><span data-stu-id="e0bfa-107">To change that behavior, set <xref:System.Text.Json.JsonSerializerOptions.PropertyNameCaseInsensitive?displayProperty=nameWithType> to `true`:</span></span>

> [!NOTE]
> <span data-ttu-id="e0bfa-108">[Web 默认值](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions)为不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="e0bfa-108">The [web default](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions) is case-insensitive.</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/DeserializeCaseInsensitive.cs" id="Deserialize":::

<span data-ttu-id="e0bfa-109">下面是具有 camel 大小写属性名称的示例 JSON。</span><span class="sxs-lookup"><span data-stu-id="e0bfa-109">Here's example JSON with camel case property names.</span></span> <span data-ttu-id="e0bfa-110">它可以反序列化为具有帕斯卡拼写法属性名称的以下类型。</span><span class="sxs-lookup"><span data-stu-id="e0bfa-110">It can be deserialized into the following type that has Pascal case property names.</span></span>

```json
{
  "date": "2019-08-01T00:00:00-07:00",
  "temperatureCelsius": 25,
  "summary": "Hot",
}
```

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/WeatherForecast.cs" id="WF":::

## <a name="see-also"></a><span data-ttu-id="e0bfa-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="e0bfa-111">See also</span></span>

* [<span data-ttu-id="e0bfa-112">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="e0bfa-112">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="e0bfa-113">如何对 JSON 进行序列化和反序列化</span><span class="sxs-lookup"><span data-stu-id="e0bfa-113">How to serialize and deserialize JSON</span></span>](system-text-json-how-to.md)
* [<span data-ttu-id="e0bfa-114">对 JsonSerializerOptions 实例进行实例化</span><span class="sxs-lookup"><span data-stu-id="e0bfa-114">Instantiate JsonSerializerOptions instances</span></span>](system-text-json-configure-options.md)
* [<span data-ttu-id="e0bfa-115">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="e0bfa-115">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="e0bfa-116">忽略属性</span><span class="sxs-lookup"><span data-stu-id="e0bfa-116">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="e0bfa-117">允许无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="e0bfa-117">Allow invalid JSON</span></span>](system-text-json-invalid-json.md)
* [<span data-ttu-id="e0bfa-118">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="e0bfa-118">Handle overflow JSON</span></span>](system-text-json-handle-overflow.md)
* [<span data-ttu-id="e0bfa-119">保留引用</span><span class="sxs-lookup"><span data-stu-id="e0bfa-119">Preserve references</span></span>](system-text-json-preserve-references.md)
* [<span data-ttu-id="e0bfa-120">不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="e0bfa-120">Immutable types and non-public accessors</span></span>](system-text-json-immutability.md)
* [<span data-ttu-id="e0bfa-121">多态序列化</span><span class="sxs-lookup"><span data-stu-id="e0bfa-121">Polymorphic serialization</span></span>](system-text-json-polymorphism.md)
* [<span data-ttu-id="e0bfa-122">从 Newtonsoft.Json 迁移到 System.Text.Json</span><span class="sxs-lookup"><span data-stu-id="e0bfa-122">Migrate from Newtonsoft.Json to System.Text.Json</span></span>](system-text-json-migrate-from-newtonsoft-how-to.md)
* [<span data-ttu-id="e0bfa-123">自定义字符编码</span><span class="sxs-lookup"><span data-stu-id="e0bfa-123">Customize character encoding</span></span>](system-text-json-character-encoding.md)
* [<span data-ttu-id="e0bfa-124">编写自定义序列化程序和反序列化程序</span><span class="sxs-lookup"><span data-stu-id="e0bfa-124">Write custom serializers and deserializers</span></span>](write-custom-serializer-deserializer.md)
* [<span data-ttu-id="e0bfa-125">编写用于 JSON 序列化的自定义转换器</span><span class="sxs-lookup"><span data-stu-id="e0bfa-125">Write custom converters for JSON serialization</span></span>](system-text-json-converters-how-to.md)
* [<span data-ttu-id="e0bfa-126">DateTime 和 DateTimeOffset 支持</span><span class="sxs-lookup"><span data-stu-id="e0bfa-126">DateTime and DateTimeOffset support</span></span>](../datetime/system-text-json-support.md)
* <span data-ttu-id="e0bfa-127">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="e0bfa-127">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
* <span data-ttu-id="e0bfa-128">[System.Text.Json.Serialization API 参考](xref:System.Text.Json.Serialization)</span><span class="sxs-lookup"><span data-stu-id="e0bfa-128">[System.Text.Json.Serialization API reference](xref:System.Text.Json.Serialization)</span></span>
