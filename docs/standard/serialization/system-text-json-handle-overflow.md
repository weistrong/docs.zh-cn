---
title: 如何使用 System.Text.Json 处理溢出 JSON
description: 了解在 .NET 中序列化为 JSON 和从 JSON 进行反序列化时如何处理溢出 JSON。
ms.date: 11/30/2020
no-loc:
- System.Text.Json
- Newtonsoft.Json
helpviewer_keywords:
- JSON serialization
- serializing objects
- serialization
- objects, serializing
ms.openlocfilehash: 265ce4f77d353720419122d17c36e508a377b68f
ms.sourcegitcommit: 81f1bba2c97a67b5ca76bcc57b37333ffca60c7b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2020
ms.locfileid: "97008911"
---
# <a name="how-to-handle-overflow-json-with-no-locsystemtextjson"></a><span data-ttu-id="f056d-103">如何使用 System.Text.Json 处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="f056d-103">How to handle overflow JSON with System.Text.Json</span></span>

<span data-ttu-id="f056d-104">本文将介绍如何使用 `System.Text.Json` 命名空间处理溢出 JSON。</span><span class="sxs-lookup"><span data-stu-id="f056d-104">In this article, you will learn how to handle overflow JSON with the `System.Text.Json` namespace.</span></span>

## <a name="handle-overflow-json"></a><span data-ttu-id="f056d-105">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="f056d-105">Handle overflow JSON</span></span>

<span data-ttu-id="f056d-106">反序列化时，可能会在 JSON 中收到不是由目标类型的属性表示的数据。</span><span class="sxs-lookup"><span data-stu-id="f056d-106">While deserializing, you might receive data in the JSON that is not represented by properties of the target type.</span></span> <span data-ttu-id="f056d-107">例如，假设目标类型如下：</span><span class="sxs-lookup"><span data-stu-id="f056d-107">For example, suppose your target type is this:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/WeatherForecast.cs" id="WF":::

<span data-ttu-id="f056d-108">要反序列化的 JSON 如下：</span><span class="sxs-lookup"><span data-stu-id="f056d-108">And the JSON to be deserialized is this:</span></span>

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "temperatureCelsius": 25,
  "Summary": "Hot",
  "DatesAvailable": [
    "2019-08-01T00:00:00-07:00",
    "2019-08-02T00:00:00-07:00"
  ],
  "SummaryWords": [
    "Cool",
    "Windy",
    "Humid"
  ]
}
```

<span data-ttu-id="f056d-109">如果将显示的 JSON 反序列化为显示的类型，则 `DatesAvailable` 和 `SummaryWords` 属性无处可去，会丢失。</span><span class="sxs-lookup"><span data-stu-id="f056d-109">If you deserialize the JSON shown into the type shown, the `DatesAvailable` and `SummaryWords` properties have nowhere to go and are lost.</span></span> <span data-ttu-id="f056d-110">若要捕获额外数据（如这些属性），请将 [[JsonExtensionData]](xref:System.Text.Json.Serialization.JsonExtensionDataAttribute) 特性应用于类型 `Dictionary<string,object>` 或 `Dictionary<string,JsonElement>` 的属性：</span><span class="sxs-lookup"><span data-stu-id="f056d-110">To capture extra data such as these properties, apply the [[JsonExtensionData]](xref:System.Text.Json.Serialization.JsonExtensionDataAttribute) attribute to a property of type `Dictionary<string,object>` or `Dictionary<string,JsonElement>`:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/WeatherForecast.cs" id="WFWithExtensionData":::

<span data-ttu-id="f056d-111">将前面显示的 JSON 反序列化为此示例类型时，额外数据会成为 `ExtensionData` 属性的键值对：</span><span class="sxs-lookup"><span data-stu-id="f056d-111">When you deserialize the JSON shown earlier into this sample type, the extra data becomes key-value pairs of the `ExtensionData` property:</span></span>

| <span data-ttu-id="f056d-112">Property</span><span class="sxs-lookup"><span data-stu-id="f056d-112">Property</span></span> | <span data-ttu-id="f056d-113">值</span><span class="sxs-lookup"><span data-stu-id="f056d-113">Value</span></span> | <span data-ttu-id="f056d-114">说明</span><span class="sxs-lookup"><span data-stu-id="f056d-114">Notes</span></span> |
|--|--|--|
| `Date` | `"8/1/2019 12:00:00 AM -07:00"` |  |
| `TemperatureCelsius` | `0` | <span data-ttu-id="f056d-115">区分大小写的不匹配（JSON 中的 `temperatureCelsius`），因此未设置属性。</span><span class="sxs-lookup"><span data-stu-id="f056d-115">Case-sensitive mismatch (`temperatureCelsius` in the JSON), so the property isn't set.</span></span> |
| `Summary` | `"Hot"` |  |
| `ExtensionData` | `temperatureCelsius: 25` | <span data-ttu-id="f056d-116">因为大小写不匹配，所以此 JSON 属性是额外属性，会成为字典中的键值对。</span><span class="sxs-lookup"><span data-stu-id="f056d-116">Since the case didn't match, this JSON property is an extra and becomes a key-value pair in the dictionary.</span></span> |
| `DatesAvailable` | `[ "8/1/2019 12:00:00 AM -07:00", "8/2/2019 12:00:00 AM -07:00" ]` | <span data-ttu-id="f056d-117">JSON 中的额外属性会成为键值对，将数组作为值对象。</span><span class="sxs-lookup"><span data-stu-id="f056d-117">Extra property from the JSON becomes a key-value pair, with an array as the value object.</span></span> |
| `SummaryWords` | `[ "Cool", "Windy", "Humid" ]` | <span data-ttu-id="f056d-118">JSON 中的额外属性会成为键值对，将数组作为值对象。</span><span class="sxs-lookup"><span data-stu-id="f056d-118">Extra property from the JSON becomes a key-value pair, with an array as the value object.</span></span> |

<span data-ttu-id="f056d-119">序列化目标对象时，扩展数据键值对会成为 JSON 属性，就如同它们处于传入 JSON 中一样：</span><span class="sxs-lookup"><span data-stu-id="f056d-119">When the target object is serialized, the extension data key value pairs become JSON properties just as they were in the incoming JSON:</span></span>

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 0,
  "Summary": "Hot",
  "temperatureCelsius": 25,
  "DatesAvailable": [
    "2019-08-01T00:00:00-07:00",
    "2019-08-02T00:00:00-07:00"
  ],
  "SummaryWords": [
    "Cool",
    "Windy",
    "Humid"
  ]
}
```

<span data-ttu-id="f056d-120">请注意，`ExtensionData` 属性名称不会出现在 JSON 中。</span><span class="sxs-lookup"><span data-stu-id="f056d-120">Notice that the `ExtensionData` property name doesn't appear in the JSON.</span></span> <span data-ttu-id="f056d-121">此行为使 JSON 可以进行往返，而不会丢失任何不会以其他方式进行反序列化的额外数据。</span><span class="sxs-lookup"><span data-stu-id="f056d-121">This behavior lets the JSON make a round trip without losing any extra data that otherwise wouldn't be deserialized.</span></span>

## <a name="see-also"></a><span data-ttu-id="f056d-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="f056d-122">See also</span></span>

* [<span data-ttu-id="f056d-123">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="f056d-123">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="f056d-124">如何对 JSON 进行序列化和反序列化</span><span class="sxs-lookup"><span data-stu-id="f056d-124">How to serialize and deserialize JSON</span></span>](system-text-json-how-to.md)
* [<span data-ttu-id="f056d-125">对 JsonSerializerOptions 实例进行实例化</span><span class="sxs-lookup"><span data-stu-id="f056d-125">Instantiate JsonSerializerOptions instances</span></span>](system-text-json-configure-options.md)
* [<span data-ttu-id="f056d-126">启用不区分大小写的匹配</span><span class="sxs-lookup"><span data-stu-id="f056d-126">Enable case-insensitive matching</span></span>](system-text-json-character-casing.md)
* [<span data-ttu-id="f056d-127">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="f056d-127">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="f056d-128">忽略属性</span><span class="sxs-lookup"><span data-stu-id="f056d-128">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="f056d-129">允许无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="f056d-129">Allow invalid JSON</span></span>](system-text-json-invalid-json.md)
* [<span data-ttu-id="f056d-130">保留引用</span><span class="sxs-lookup"><span data-stu-id="f056d-130">Preserve references</span></span>](system-text-json-preserve-references.md)
* [<span data-ttu-id="f056d-131">不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="f056d-131">Immutable types and non-public accessors</span></span>](system-text-json-immutability.md)
* [<span data-ttu-id="f056d-132">多态序列化</span><span class="sxs-lookup"><span data-stu-id="f056d-132">Polymorphic serialization</span></span>](system-text-json-polymorphism.md)
* [<span data-ttu-id="f056d-133">从 Newtonsoft.Json 迁移到 System.Text.Json</span><span class="sxs-lookup"><span data-stu-id="f056d-133">Migrate from Newtonsoft.Json to System.Text.Json</span></span>](system-text-json-migrate-from-newtonsoft-how-to.md)
* [<span data-ttu-id="f056d-134">自定义字符编码</span><span class="sxs-lookup"><span data-stu-id="f056d-134">Customize character encoding</span></span>](system-text-json-character-encoding.md)
* [<span data-ttu-id="f056d-135">编写自定义序列化程序和反序列化程序</span><span class="sxs-lookup"><span data-stu-id="f056d-135">Write custom serializers and deserializers</span></span>](write-custom-serializer-deserializer.md)
* [<span data-ttu-id="f056d-136">编写用于 JSON 序列化的自定义转换器</span><span class="sxs-lookup"><span data-stu-id="f056d-136">Write custom converters for JSON serialization</span></span>](system-text-json-converters-how-to.md)
* [<span data-ttu-id="f056d-137">DateTime 和 DateTimeOffset 支持</span><span class="sxs-lookup"><span data-stu-id="f056d-137">DateTime and DateTimeOffset support</span></span>](../datetime/system-text-json-support.md)
* <span data-ttu-id="f056d-138">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="f056d-138">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
* <span data-ttu-id="f056d-139">[System.Text.Json.Serialization API 参考](xref:System.Text.Json.Serialization)</span><span class="sxs-lookup"><span data-stu-id="f056d-139">[System.Text.Json.Serialization API reference](xref:System.Text.Json.Serialization)</span></span>
