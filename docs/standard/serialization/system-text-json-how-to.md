---
title: 如何使用 C# 对 JSON 进行序列化和反序列化 - .NET
description: 了解如何使用 System.Text.Json 命名空间在 .NET 中向/从 JSON 进行序列化和反序列化。 包含示例代码。
ms.date: 12/02/2020
ms.custom: contperfq2
no-loc:
- System.Text.Json
- Newtonsoft.Json
zone_pivot_groups: dotnet-version
helpviewer_keywords:
- JSON serialization
- serializing objects
- serialization
- objects, serializing
ms.openlocfilehash: 1ea4ff71b9e21bd7c5b12598581b33e1e96ebb19
ms.sourcegitcommit: 81f1bba2c97a67b5ca76bcc57b37333ffca60c7b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2020
ms.locfileid: "97008833"
---
# <a name="how-to-serialize-and-deserialize-marshal-and-unmarshal-json-in-net"></a><span data-ttu-id="dd9e3-104">如何在 .NET 中对 JSON 进行序列化和反序列化（封送和拆收）</span><span class="sxs-lookup"><span data-stu-id="dd9e3-104">How to serialize and deserialize (marshal and unmarshal) JSON in .NET</span></span>

<span data-ttu-id="dd9e3-105">本文演示如何使用 <xref:System.Text.Json?displayProperty=fullName> 命名空间向/从 JavaScript 对象表示法 (JSON) 进行序列化和反序列化。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-105">This article shows how to use the <xref:System.Text.Json?displayProperty=fullName> namespace to serialize to and deserialize from JavaScript Object Notation (JSON).</span></span> <span data-ttu-id="dd9e3-106">如果要从 `Newtonsoft.Json` 移植现有代码，请参阅[如何迁移到 `System.Text.Json`](system-text-json-migrate-from-newtonsoft-how-to.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-106">If you're porting existing code from `Newtonsoft.Json`, see [How to migrate to `System.Text.Json`](system-text-json-migrate-from-newtonsoft-how-to.md).</span></span>

<span data-ttu-id="dd9e3-107">方向和示例代码直接使用库，而不是通过框架（如 [ASP.NET Core](/aspnet/core/)）。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-107">The directions and sample code use the library directly, not through a framework such as [ASP.NET Core](/aspnet/core/).</span></span>

<span data-ttu-id="dd9e3-108">大多数序列化示例代码将 <xref:System.Text.Json.JsonSerializerOptions.WriteIndented?displayProperty=nameWithType> 设置为 `true`，以 JSON 进行优质打印（包含缩进和空格，以提高可读性）。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-108">Most of the serialization sample code sets <xref:System.Text.Json.JsonSerializerOptions.WriteIndented?displayProperty=nameWithType> to `true` to "pretty-print" the JSON (with indentation and whitespace for human readability).</span></span> <span data-ttu-id="dd9e3-109">对于生产用途，通常对于此设置会接受默认值 `false`。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-109">For production use, you would typically accept the default value of `false` for this setting.</span></span>

<span data-ttu-id="dd9e3-110">代码示例引用下面的类及其变体：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-110">The code examples refer to the following class and variants of it:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/WeatherForecast.cs" id="WF":::

## <a name="namespaces"></a><span data-ttu-id="dd9e3-111">命名空间</span><span class="sxs-lookup"><span data-stu-id="dd9e3-111">Namespaces</span></span>

<span data-ttu-id="dd9e3-112"><xref:System.Text.Json> 命名空间包含所有入口点和主要类型。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-112">The <xref:System.Text.Json> namespace contains all the entry points and the main types.</span></span> <span data-ttu-id="dd9e3-113"><xref:System.Text.Json.Serialization> 命名空间包含用于高级方案的特性和 API，以及特定于序列化和反序列化的自定义。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-113">The <xref:System.Text.Json.Serialization> namespace contains attributes and APIs for advanced scenarios and customization specific to serialization and deserialization.</span></span> <span data-ttu-id="dd9e3-114">本文中演示的代码示例要求将 `using` 指令用于其中一个或两个命名空间：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-114">The code examples shown in this article require `using` directives for one or both of these namespaces:</span></span>

```csharp
using System.Text.Json;
using System.Text.Json.Serialization;
```

> [!IMPORTANT]
> <span data-ttu-id="dd9e3-115">`System.Text.Json` 中不支持 <xref:System.Runtime.Serialization> 命名空间中的特性。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-115">Attributes from the <xref:System.Runtime.Serialization> namespace aren't supported in `System.Text.Json`.</span></span>

## <a name="how-to-write-net-objects-as-json-serialize"></a><span data-ttu-id="dd9e3-116">如何将 .NET 对象编写为 JSON（序列化）</span><span class="sxs-lookup"><span data-stu-id="dd9e3-116">How to write .NET objects as JSON (serialize)</span></span>

<span data-ttu-id="dd9e3-117">若要将 JSON 编写为字符串或文件，请调用 <xref:System.Text.Json.JsonSerializer.Serialize%2A?displayProperty=nameWithType> 方法。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-117">To write JSON to a string or to a file, call the <xref:System.Text.Json.JsonSerializer.Serialize%2A?displayProperty=nameWithType> method.</span></span>

<span data-ttu-id="dd9e3-118">下面的示例将 JSON 创建为字符串：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-118">The following example creates JSON as a string:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/RoundtripToString.cs" id="Serialize":::

<span data-ttu-id="dd9e3-119">下面的示例使用同步代码创建 JSON 文件：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-119">The following example uses synchronous code to create a JSON file:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/RoundtripToFile.cs" id="Serialize":::

<span data-ttu-id="dd9e3-120">下面的示例使用异步代码创建 JSON 文件：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-120">The following example uses asynchronous code to create a JSON file:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/RoundtripToFileAsync.cs" id="Serialize":::

<span data-ttu-id="dd9e3-121">前面的示例对要序列化的类型使用类型推理。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-121">The preceding examples use type inference for the type being serialized.</span></span> <span data-ttu-id="dd9e3-122">`Serialize()` 的重载采用泛型类型参数：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-122">An overload of `Serialize()` takes a generic type parameter:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/RoundtripToString.cs" id="SerializeWithGenericParameter":::

### <a name="serialization-example"></a><span data-ttu-id="dd9e3-123">序列化示例</span><span class="sxs-lookup"><span data-stu-id="dd9e3-123">Serialization example</span></span>

<span data-ttu-id="dd9e3-124">下面是一个包含集合类型属性和用户定义类型的示例类：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-124">Here's an example class that contains collection-type properties and a user-defined type:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/WeatherForecast.cs" id="WFWithPOCOs":::

> [!TIP]
> <span data-ttu-id="dd9e3-125">“POCO”代表[普通旧 CLR 对象](https://en.wikipedia.org/wiki/Plain_old_CLR_object)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-125">"POCO" stands for [plain old CLR object](https://en.wikipedia.org/wiki/Plain_old_CLR_object).</span></span> <span data-ttu-id="dd9e3-126">POCO 是一种 .NET 类型，它不通过继承或特性等依赖于任何框架特定类型。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-126">A POCO is a .NET type that doesn't depend on any framework-specific types, for example, through inheritance or attributes.</span></span>

<span data-ttu-id="dd9e3-127">序列化以上类型的实例的 JSON 输出类似于下面的示例。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-127">The JSON output from serializing an instance of the preceding type looks like the following example.</span></span> <span data-ttu-id="dd9e3-128">默认情况下，JSON 输出会缩小（将删除空格、缩进和换行符）：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-128">The JSON output is minified (whitespace, indentation, and new-line characters are removed) by default:</span></span>

```json
{"Date":"2019-08-01T00:00:00-07:00","TemperatureCelsius":25,"Summary":"Hot","DatesAvailable":["2019-08-01T00:00:00-07:00","2019-08-02T00:00:00-07:00"],"TemperatureRanges":{"Cold":{"High":20,"Low":-10},"Hot":{"High":60,"Low":20}},"SummaryWords":["Cool","Windy","Humid"]}
```

<span data-ttu-id="dd9e3-129">下面的示例演示相同的 JSON，但进行了格式设置（即，具有空格和缩进的优质打印版本）：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-129">The following example shows the same JSON, but formatted (that is, pretty-printed with whitespace and indentation):</span></span>

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 25,
  "Summary": "Hot",
  "DatesAvailable": [
    "2019-08-01T00:00:00-07:00",
    "2019-08-02T00:00:00-07:00"
  ],
  "TemperatureRanges": {
    "Cold": {
      "High": 20,
      "Low": -10
    },
    "Hot": {
      "High": 60,
      "Low": 20
    }
  },
  "SummaryWords": [
    "Cool",
    "Windy",
    "Humid"
  ]
}
```

## <a name="serialize-to-utf-8"></a><span data-ttu-id="dd9e3-130">序列化为 UTF-8</span><span class="sxs-lookup"><span data-stu-id="dd9e3-130">Serialize to UTF-8</span></span>

<span data-ttu-id="dd9e3-131">若要序列化为 UTF-8，请调用 <xref:System.Text.Json.JsonSerializer.SerializeToUtf8Bytes%2A?displayProperty=nameWithType> 方法：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-131">To serialize to UTF-8, call the <xref:System.Text.Json.JsonSerializer.SerializeToUtf8Bytes%2A?displayProperty=nameWithType> method:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/RoundtripToUtf8.cs" id="Serialize":::

<span data-ttu-id="dd9e3-132">还有一个采用 <xref:System.Text.Json.Utf8JsonWriter> 的 <xref:System.Text.Json.JsonSerializer.Serialize%2A> 重载可用。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-132">A <xref:System.Text.Json.JsonSerializer.Serialize%2A> overload that takes a <xref:System.Text.Json.Utf8JsonWriter> is also available.</span></span>

<span data-ttu-id="dd9e3-133">序列化为 UTF-8 比使用基于字符串的方法大约快 5-10%。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-133">Serializing to UTF-8 is about 5-10% faster than using the string-based methods.</span></span> <span data-ttu-id="dd9e3-134">出现这种差别的原因是字节（作为 UTF-8）不需要转换为字符串 (UTF-16)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-134">The difference is because the bytes (as UTF-8) don't need to be converted to strings (UTF-16).</span></span>

## <a name="serialization-behavior"></a><span data-ttu-id="dd9e3-135">序列化行为</span><span class="sxs-lookup"><span data-stu-id="dd9e3-135">Serialization behavior</span></span>

::: zone pivot="dotnet-5-0"

* <span data-ttu-id="dd9e3-136">默认情况下，所有公共属性都会序列化。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-136">By default, all public properties are serialized.</span></span> <span data-ttu-id="dd9e3-137">可以[指定要忽略的属性](system-text-json-ignore-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-137">You can [specify properties to ignore](system-text-json-ignore-properties.md).</span></span>
* <span data-ttu-id="dd9e3-138">[默认编码器](xref:System.Text.Encodings.Web.JavaScriptEncoder.Default)会转义非 ASCII 字符、ASCII 范围内的 HTML 敏感字符以及根据 [RFC 8259 JSON 规范](https://tools.ietf.org/html/rfc8259#section-7)必须进行转义的字符。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-138">The [default encoder](xref:System.Text.Encodings.Web.JavaScriptEncoder.Default) escapes non-ASCII characters, HTML-sensitive characters within the ASCII-range, and characters that must be escaped according to [the RFC 8259 JSON spec](https://tools.ietf.org/html/rfc8259#section-7).</span></span>
* <span data-ttu-id="dd9e3-139">默认情况下，JSON 会缩小。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-139">By default, JSON is minified.</span></span> <span data-ttu-id="dd9e3-140">可以[对 JSON 进行优质打印](#serialize-to-formatted-json)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-140">You can [pretty-print the JSON](#serialize-to-formatted-json).</span></span>
* <span data-ttu-id="dd9e3-141">默认情况下，JSON 名称的大小写与 .NET 名称匹配。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-141">By default, casing of JSON names matches the .NET names.</span></span> <span data-ttu-id="dd9e3-142">可以[自定义 JSON 名称大小写](system-text-json-customize-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-142">You can [customize JSON name casing](system-text-json-customize-properties.md).</span></span>
* <span data-ttu-id="dd9e3-143">默认情况下，检测到循环引用并引发异常。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-143">By default, circular references are detected and exceptions thrown.</span></span> <span data-ttu-id="dd9e3-144">可以[保留引用并处理循环引用](system-text-json-preserve-references.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-144">You can [preserve references and handle circular references](system-text-json-preserve-references.md).</span></span>
* <span data-ttu-id="dd9e3-145">默认情况下忽略[字段](../../csharp/programming-guide/classes-and-structs/fields.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-145">By default, [fields](../../csharp/programming-guide/classes-and-structs/fields.md) are ignored.</span></span> <span data-ttu-id="dd9e3-146">可以[包含字段](#include-fields)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-146">You can [include fields](#include-fields).</span></span>

<span data-ttu-id="dd9e3-147">当你在 ASP.NET Core 应用中间接使用 System.Text.Json 时，某些默认行为会有所不同。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-147">When you use System.Text.Json indirectly in an ASP.NET Core app, some default behaviors are different.</span></span> <span data-ttu-id="dd9e3-148">有关详细信息，请参阅 [JsonSerializerOptions 的 Web 默认值](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-148">For more information, see [Web defaults for JsonSerializerOptions](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions).</span></span>
::: zone-end

::: zone pivot="dotnet-core-3-1"

* <span data-ttu-id="dd9e3-149">默认情况下，所有公共属性都会序列化。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-149">By default, all public properties are serialized.</span></span> <span data-ttu-id="dd9e3-150">可以[指定要忽略的属性](system-text-json-ignore-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-150">You can [specify properties to ignore](system-text-json-ignore-properties.md).</span></span>
* <span data-ttu-id="dd9e3-151">[默认编码器](xref:System.Text.Encodings.Web.JavaScriptEncoder.Default)会转义非 ASCII 字符、ASCII 范围内的 HTML 敏感字符以及根据 [RFC 8259 JSON 规范](https://tools.ietf.org/html/rfc8259#section-7)必须进行转义的字符。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-151">The [default encoder](xref:System.Text.Encodings.Web.JavaScriptEncoder.Default) escapes non-ASCII characters, HTML-sensitive characters within the ASCII-range, and characters that must be escaped according to [the RFC 8259 JSON spec](https://tools.ietf.org/html/rfc8259#section-7).</span></span>
* <span data-ttu-id="dd9e3-152">默认情况下，JSON 会缩小。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-152">By default, JSON is minified.</span></span> <span data-ttu-id="dd9e3-153">可以[对 JSON 进行优质打印](#serialize-to-formatted-json)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-153">You can [pretty-print the JSON](#serialize-to-formatted-json).</span></span>
* <span data-ttu-id="dd9e3-154">默认情况下，JSON 名称的大小写与 .NET 名称匹配。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-154">By default, casing of JSON names matches the .NET names.</span></span> <span data-ttu-id="dd9e3-155">可以[自定义 JSON 名称大小写](system-text-json-customize-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-155">You can [customize JSON name casing](system-text-json-customize-properties.md).</span></span>
* <span data-ttu-id="dd9e3-156">检测到循环引用并引发异常。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-156">Circular references are detected and exceptions thrown.</span></span>
* <span data-ttu-id="dd9e3-157">将忽略[字段](../../csharp/programming-guide/classes-and-structs/fields.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-157">[Fields](../../csharp/programming-guide/classes-and-structs/fields.md) are ignored.</span></span>
::: zone-end

<span data-ttu-id="dd9e3-158">支持的类型包括：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-158">Supported types include:</span></span>
::: zone pivot="dotnet-5-0"

* <span data-ttu-id="dd9e3-159">映射到 JavaScript 基元的 .NET 基元，如数值类型、字符串和布尔。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-159">.NET primitives that map to JavaScript primitives, such as numeric types, strings, and Boolean.</span></span>
* <span data-ttu-id="dd9e3-160">用户定义的[普通旧 CLR 对象 (POCO)](https://en.wikipedia.org/wiki/Plain_old_CLR_object)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-160">User-defined [plain old CLR objects (POCOs)](https://en.wikipedia.org/wiki/Plain_old_CLR_object).</span></span>
* <span data-ttu-id="dd9e3-161">一维和交错数组 (`T[][]`)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-161">One-dimensional and jagged arrays (`T[][]`).</span></span>
* <span data-ttu-id="dd9e3-162">以下命名空间中的集合和字典。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-162">Collections and dictionaries from the following namespaces.</span></span>
  * <xref:System.Collections>
  * <xref:System.Collections.Generic>
  * <xref:System.Collections.Immutable>
  * <xref:System.Collections.Concurrent>
  * <xref:System.Collections.Specialized>
  * <xref:System.Collections.ObjectModel>
::: zone-end

::: zone pivot="dotnet-core-3-1"

* <span data-ttu-id="dd9e3-163">映射到 JavaScript 基元的 .NET 基元，如数值类型、字符串和布尔。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-163">.NET primitives that map to JavaScript primitives, such as numeric types, strings, and Boolean.</span></span>
* <span data-ttu-id="dd9e3-164">用户定义的[普通旧 CLR 对象 (POCO)](https://en.wikipedia.org/wiki/Plain_old_CLR_object)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-164">User-defined [plain old CLR objects (POCOs)](https://en.wikipedia.org/wiki/Plain_old_CLR_object).</span></span>
* <span data-ttu-id="dd9e3-165">一维和交错数组 (`ArrayName[][]`)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-165">One-dimensional and jagged arrays (`ArrayName[][]`).</span></span>
* <span data-ttu-id="dd9e3-166">`Dictionary<string,TValue>`其中 `TValue` 是 `object`、`JsonElement` 或 POCO。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-166">`Dictionary<string,TValue>` where `TValue` is `object`, `JsonElement`, or a POCO.</span></span>
* <span data-ttu-id="dd9e3-167">以下命名空间中的集合。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-167">Collections from the following namespaces.</span></span>
  * <xref:System.Collections>
  * <xref:System.Collections.Generic>
  * <xref:System.Collections.Immutable>
  * <xref:System.Collections.Concurrent>
  * <xref:System.Collections.Specialized>
  * <xref:System.Collections.ObjectModel>
::: zone-end

<span data-ttu-id="dd9e3-168">可以[实现自定义转换器](system-text-json-converters-how-to.md)以处理其他类型或提供内置转换器不支持的功能。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-168">You can [implement custom converters](system-text-json-converters-how-to.md) to handle additional types or to provide functionality that isn't supported by the built-in converters.</span></span>

## <a name="how-to-read-json-as-net-objects-deserialize"></a><span data-ttu-id="dd9e3-169">如何将 JSON 读取为 .NET 对象（反序列化）</span><span class="sxs-lookup"><span data-stu-id="dd9e3-169">How to read JSON as .NET objects (deserialize)</span></span>

<span data-ttu-id="dd9e3-170">若要从字符串或文件进行反序列化，请调用 <xref:System.Text.Json.JsonSerializer.Deserialize%2A?displayProperty=nameWithType> 方法。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-170">To deserialize from a string or a file, call the <xref:System.Text.Json.JsonSerializer.Deserialize%2A?displayProperty=nameWithType> method.</span></span>

<span data-ttu-id="dd9e3-171">下面的示例从字符串读取 JSON，并创建前面为[序列化示例](#serialization-example)显示的 `WeatherForecastWithPOCOs` 类的实例：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-171">The following example reads JSON from a string and creates an instance of the `WeatherForecastWithPOCOs` class shown earlier for the [serialization example](#serialization-example):</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/RoundtripToString.cs" id="Deserialize":::

<span data-ttu-id="dd9e3-172">若要使用同步代码从文件进行反序列化，请将文件读入字符串中，如下面的示例中所示：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-172">To deserialize from a file by using synchronous code, read the file into a string, as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/RoundtripToFile.cs" id="Deserialize":::

<span data-ttu-id="dd9e3-173">若要使用异步代码从文件进行反序列化，请调用 <xref:System.Text.Json.JsonSerializer.DeserializeAsync%2A> 方法：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-173">To deserialize from a file by using asynchronous code, call the <xref:System.Text.Json.JsonSerializer.DeserializeAsync%2A> method:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/RoundtripToFileAsync.cs" id="Deserialize":::

## <a name="deserialize-from-utf-8"></a><span data-ttu-id="dd9e3-174">从 UTF-8 进行反序列化</span><span class="sxs-lookup"><span data-stu-id="dd9e3-174">Deserialize from UTF-8</span></span>

<span data-ttu-id="dd9e3-175">若要从 UTF-8 进行反序列化，请调用采用 `ReadOnlySpan<byte>` 或 `Utf8JsonReader` 的 <xref:System.Text.Json.JsonSerializer.Deserialize%2A?displayProperty=nameWithType> 重载，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-175">To deserialize from UTF-8, call a <xref:System.Text.Json.JsonSerializer.Deserialize%2A?displayProperty=nameWithType> overload that takes a `ReadOnlySpan<byte>` or a `Utf8JsonReader`, as shown in the following examples.</span></span> <span data-ttu-id="dd9e3-176">这些示例假设 JSON 处于名为 jsonUtf8Bytes 的字节数组中。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-176">The examples assume the JSON is in a byte array named jsonUtf8Bytes.</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/RoundtripToUtf8.cs" id="Deserialize1":::

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/RoundtripToUtf8.cs" id="Deserialize2":::

## <a name="deserialization-behavior"></a><span data-ttu-id="dd9e3-177">反序列化行为</span><span class="sxs-lookup"><span data-stu-id="dd9e3-177">Deserialization behavior</span></span>

<span data-ttu-id="dd9e3-178">对 JSON 进行反序列化时，以下行为适用：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-178">The following behaviors apply when deserializing JSON:</span></span>

::: zone pivot="dotnet-5-0"

* <span data-ttu-id="dd9e3-179">默认情况下，属性名称匹配区分大小写。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-179">By default, property name matching is case-sensitive.</span></span> <span data-ttu-id="dd9e3-180">可以[指定不区分大小写](system-text-json-character-casing.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-180">You can [specify case-insensitivity](system-text-json-character-casing.md).</span></span>
* <span data-ttu-id="dd9e3-181">如果 JSON 包含只读属性的值，则会忽略该值，并且不引发异常。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-181">If the JSON contains a value for a read-only property, the value is ignored and no exception is thrown.</span></span>
* <span data-ttu-id="dd9e3-182">序列化程序会忽略非公共构造函数。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-182">Non-public constructors are ignored by the serializer.</span></span>
* <span data-ttu-id="dd9e3-183">支持反序列化为不可变对象或只读属性。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-183">Deserialization to immutable objects or read-only properties is supported.</span></span> <span data-ttu-id="dd9e3-184">请参阅[不可变类型和记录](system-text-json-immutability.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-184">See [Immutable types and Records](system-text-json-immutability.md).</span></span>
* <span data-ttu-id="dd9e3-185">默认情况下，支持将枚举作为数字。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-185">By default, enums are supported as numbers.</span></span> <span data-ttu-id="dd9e3-186">可以[将枚举名称序列化为字符串](system-text-json-customize-properties.md#enums-as-strings)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-186">You can [serialize enum names as strings](system-text-json-customize-properties.md#enums-as-strings).</span></span>
* <span data-ttu-id="dd9e3-187">默认情况下忽略字段。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-187">By default, fields are ignored.</span></span> <span data-ttu-id="dd9e3-188">可以[包含字段](#include-fields)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-188">You can [include fields](#include-fields).</span></span>
* <span data-ttu-id="dd9e3-189">默认情况下，JSON 中的注释或尾随逗号会引发异常。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-189">By default, comments or trailing commas in the JSON throw exceptions.</span></span> <span data-ttu-id="dd9e3-190">可以[允许注释和尾随逗号](system-text-json-invalid-json.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-190">You can [allow comments and trailing commas](system-text-json-invalid-json.md).</span></span>
* <span data-ttu-id="dd9e3-191">[默认最大深度](xref:System.Text.Json.JsonReaderOptions.MaxDepth)为 64。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-191">The [default maximum depth](xref:System.Text.Json.JsonReaderOptions.MaxDepth) is 64.</span></span>

<span data-ttu-id="dd9e3-192">当你在 ASP.NET Core 应用中间接使用 System.Text.Json 时，某些默认行为会有所不同。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-192">When you use System.Text.Json indirectly in an ASP.NET Core app, some default behaviors are different.</span></span> <span data-ttu-id="dd9e3-193">有关详细信息，请参阅 [JsonSerializerOptions 的 Web 默认值](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-193">For more information, see [Web defaults for JsonSerializerOptions](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions).</span></span>
::: zone-end

::: zone pivot="dotnet-core-3-1"

* <span data-ttu-id="dd9e3-194">默认情况下，属性名称匹配区分大小写。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-194">By default, property name matching is case-sensitive.</span></span> <span data-ttu-id="dd9e3-195">可以[指定不区分大小写](system-text-json-character-casing.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-195">You can [specify case-insensitivity](system-text-json-character-casing.md).</span></span> <span data-ttu-id="dd9e3-196">ASP.NET Core 应用[默认指定不区分大小写](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-196">ASP.NET Core apps [specify case-insensitivity by default](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions).</span></span>
* <span data-ttu-id="dd9e3-197">如果 JSON 包含只读属性的值，则会忽略该值，并且不引发异常。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-197">If the JSON contains a value for a read-only property, the value is ignored and no exception is thrown.</span></span>
* <span data-ttu-id="dd9e3-198">无参数构造函数（可以是公共的、内部的或专用的）用于反序列化。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-198">A parameterless constructor, which can be public, internal, or private, is used for deserialization.</span></span>
* <span data-ttu-id="dd9e3-199">不支持反序列化为不可变对象或只读属性。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-199">Deserialization to immutable objects or read-only properties isn't supported.</span></span>
* <span data-ttu-id="dd9e3-200">默认情况下，支持将枚举作为数字。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-200">By default, enums are supported as numbers.</span></span> <span data-ttu-id="dd9e3-201">可以[将枚举名称序列化为字符串](system-text-json-customize-properties.md#enums-as-strings)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-201">You can [serialize enum names as strings](system-text-json-customize-properties.md#enums-as-strings).</span></span>
* <span data-ttu-id="dd9e3-202">不支持字段。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-202">Fields aren't supported.</span></span>
* <span data-ttu-id="dd9e3-203">默认情况下，JSON 中的注释或尾随逗号会引发异常。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-203">By default, comments or trailing commas in the JSON throw exceptions.</span></span> <span data-ttu-id="dd9e3-204">可以[允许注释和尾随逗号](system-text-json-invalid-json.md)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-204">You can [allow comments and trailing commas](system-text-json-invalid-json.md).</span></span>
* <span data-ttu-id="dd9e3-205">[默认最大深度](xref:System.Text.Json.JsonReaderOptions.MaxDepth)为 64。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-205">The [default maximum depth](xref:System.Text.Json.JsonReaderOptions.MaxDepth) is 64.</span></span>

<span data-ttu-id="dd9e3-206">当你在 ASP.NET Core 应用中间接使用 System.Text.Json 时，某些默认行为会有所不同。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-206">When you use System.Text.Json indirectly in an ASP.NET Core app, some default behaviors are different.</span></span> <span data-ttu-id="dd9e3-207">有关详细信息，请参阅 [JsonSerializerOptions 的 Web 默认值](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-207">For more information, see [Web defaults for JsonSerializerOptions](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions).</span></span>
::: zone-end

<span data-ttu-id="dd9e3-208">可以[实现自定义转换器](system-text-json-converters-how-to.md)以提供内置转换器不支持的功能。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-208">You can [implement custom converters](system-text-json-converters-how-to.md) to provide functionality that isn't supported by the built-in converters.</span></span>

## <a name="serialize-to-formatted-json"></a><span data-ttu-id="dd9e3-209">序列化为格式化 JSON</span><span class="sxs-lookup"><span data-stu-id="dd9e3-209">Serialize to formatted JSON</span></span>

<span data-ttu-id="dd9e3-210">若要对 JSON 输出进行优质打印，请将 <xref:System.Text.Json.JsonSerializerOptions.WriteIndented?displayProperty=nameWithType> 设置为 `true`：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-210">To pretty-print the JSON output, set <xref:System.Text.Json.JsonSerializerOptions.WriteIndented?displayProperty=nameWithType> to `true`:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/RoundtripToString.cs" id="SerializePrettyPrint":::

<span data-ttu-id="dd9e3-211">下面是一个要进行序列化的示例类型，以及进行了优质打印的 JSON 输出：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-211">Here's an example type to be serialized and pretty-printed JSON output:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/WeatherForecast.cs" id="WF":::

```json
{
  "Date": "2019-08-01T00:00:00-07:00",
  "TemperatureCelsius": 25,
  "Summary": "Hot"
}
```

<span data-ttu-id="dd9e3-212">如果你通过相同的选项重复使用 `JsonSerializerOptions`，则请勿在每次使用时都创建新的 `JsonSerializerOptions` 实例。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-212">If you use `JsonSerializerOptions` repeatedly with the same options, don't create a new `JsonSerializerOptions` instance each time you use it.</span></span> <span data-ttu-id="dd9e3-213">对每个调用重复使用同一实例。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-213">Reuse the same instance for every call.</span></span> <span data-ttu-id="dd9e3-214">有关详细信息，请参阅[重用 JsonSerializerOptions 实例](system-text-json-configure-options.md#reuse-jsonserializeroptions-instances)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-214">For more information, see [Reuse JsonSerializerOptions instances](system-text-json-configure-options.md#reuse-jsonserializeroptions-instances).</span></span>

## <a name="include-fields"></a><span data-ttu-id="dd9e3-215">包含字段</span><span class="sxs-lookup"><span data-stu-id="dd9e3-215">Include fields</span></span>

::: zone pivot="dotnet-5-0"
<span data-ttu-id="dd9e3-216">在序列化或反序列化时，使用 <xref:System.Text.Json.JsonSerializerOptions.IncludeFields?displayProperty=nameWithType> 全局设置或 [[JsonInclude]](xref:System.Text.Json.Serialization.JsonIncludeAttribute) 特性来包含字段，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-216">Use the <xref:System.Text.Json.JsonSerializerOptions.IncludeFields?displayProperty=nameWithType> global setting or the [[JsonInclude]](xref:System.Text.Json.Serialization.JsonIncludeAttribute) attribute to include fields when serializing or deserializing, as shown in the following example:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/Fields.cs" highlight="16,18,20,32-35":::

<span data-ttu-id="dd9e3-217">若要忽略只读字段，请使用 <xref:System.Text.Json.JsonSerializerOptions.IgnoreReadOnlyFields%2A?displayProperty=nameWithType> 全局设置。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-217">To ignore read-only fields, use the <xref:System.Text.Json.JsonSerializerOptions.IgnoreReadOnlyFields%2A?displayProperty=nameWithType> global setting.</span></span>
::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="dd9e3-218">.NET Core 3.1 的 System.Text.Json 中不支持字段。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-218">Fields are not supported in System.Text.Json in .NET Core 3.1.</span></span> <span data-ttu-id="dd9e3-219">[自定义转换器](system-text-json-converters-how-to.md)可提供此功能。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-219">[Custom converters](system-text-json-converters-how-to.md) can provide this functionality.</span></span>
::: zone-end

## <a name="httpclient-and-httpcontent-extension-methods"></a><span data-ttu-id="dd9e3-220">HttpClient 和 HttpContent 扩展方法</span><span class="sxs-lookup"><span data-stu-id="dd9e3-220">HttpClient and HttpContent extension methods</span></span>

::: zone pivot="dotnet-5-0"

<span data-ttu-id="dd9e3-221">序列化和反序列化来自网络的 JSON 有效负载是常见的操作。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-221">Serializing and deserializing JSON payloads from the network are common operations.</span></span> <span data-ttu-id="dd9e3-222">[HttpClient](xref:System.Net.Http.Json.HttpClientJsonExtensions) 和 [HttpContent](xref:System.Net.Http.Json.HttpContentJsonExtensions) 上的扩展方法允许在单个代码行中执行这些操作。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-222">Extension methods on [HttpClient](xref:System.Net.Http.Json.HttpClientJsonExtensions) and [HttpContent](xref:System.Net.Http.Json.HttpContentJsonExtensions) let you do these operations in a single line of code.</span></span> <span data-ttu-id="dd9e3-223">这些扩展方法使用 [JsonSerializerOptions 的 Web 默认值](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions)。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-223">These extension methods use [web defaults for JsonSerializerOptions](system-text-json-configure-options.md#web-defaults-for-jsonserializeroptions).</span></span>

<span data-ttu-id="dd9e3-224">以下示例说明了 <xref:System.Net.Http.Json.HttpClientJsonExtensions.GetFromJsonAsync%2A?displayProperty=nameWithType> 和 <xref:System.Net.Http.Json.HttpClientJsonExtensions.PostAsJsonAsync%2A?displayProperty=nameWithType> 的用法：</span><span class="sxs-lookup"><span data-stu-id="dd9e3-224">The following example illustrates use of <xref:System.Net.Http.Json.HttpClientJsonExtensions.GetFromJsonAsync%2A?displayProperty=nameWithType> and <xref:System.Net.Http.Json.HttpClientJsonExtensions.PostAsJsonAsync%2A?displayProperty=nameWithType>:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to-5-0/csharp/HttpClientExtensionMethods.cs" highlight="26,33":::

<span data-ttu-id="dd9e3-225">此外还有 [HttpContent](xref:System.Net.Http.Json.HttpContentJsonExtensions) 上的 System.Text.Json 的扩展方法。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-225">There are also extension methods for System.Text.Json on [HttpContent](xref:System.Net.Http.Json.HttpContentJsonExtensions).</span></span>
::: zone-end

::: zone pivot="dotnet-core-3-1"
<span data-ttu-id="dd9e3-226">`HttpClient` 和 `HttpContent` 上的扩展方法在 .NET Core 3.1 的 System.Text.Json 中不可用。</span><span class="sxs-lookup"><span data-stu-id="dd9e3-226">Extension methods on `HttpClient` and `HttpContent` are not available in System.Text.Json in .NET Core 3.1.</span></span>
::: zone-end

## <a name="see-also"></a><span data-ttu-id="dd9e3-227">请参阅</span><span class="sxs-lookup"><span data-stu-id="dd9e3-227">See also</span></span>

* [<span data-ttu-id="dd9e3-228">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="dd9e3-228">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="dd9e3-229">对 JsonSerializerOptions 实例进行实例化</span><span class="sxs-lookup"><span data-stu-id="dd9e3-229">Instantiate JsonSerializerOptions instances</span></span>](system-text-json-configure-options.md)
* [<span data-ttu-id="dd9e3-230">启用不区分大小写的匹配</span><span class="sxs-lookup"><span data-stu-id="dd9e3-230">Enable case-insensitive matching</span></span>](system-text-json-character-casing.md)
* [<span data-ttu-id="dd9e3-231">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="dd9e3-231">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="dd9e3-232">忽略属性</span><span class="sxs-lookup"><span data-stu-id="dd9e3-232">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="dd9e3-233">允许无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="dd9e3-233">Allow invalid JSON</span></span>](system-text-json-invalid-json.md)
* [<span data-ttu-id="dd9e3-234">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="dd9e3-234">Handle overflow JSON</span></span>](system-text-json-handle-overflow.md)
* [<span data-ttu-id="dd9e3-235">保留引用</span><span class="sxs-lookup"><span data-stu-id="dd9e3-235">Preserve references</span></span>](system-text-json-preserve-references.md)
* [<span data-ttu-id="dd9e3-236">不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="dd9e3-236">Immutable types and non-public accessors</span></span>](system-text-json-immutability.md)
* [<span data-ttu-id="dd9e3-237">多态序列化</span><span class="sxs-lookup"><span data-stu-id="dd9e3-237">Polymorphic serialization</span></span>](system-text-json-polymorphism.md)
* [<span data-ttu-id="dd9e3-238">从 Newtonsoft.Json 迁移到 System.Text.Json</span><span class="sxs-lookup"><span data-stu-id="dd9e3-238">Migrate from Newtonsoft.Json to System.Text.Json</span></span>](system-text-json-migrate-from-newtonsoft-how-to.md)
* [<span data-ttu-id="dd9e3-239">自定义字符编码</span><span class="sxs-lookup"><span data-stu-id="dd9e3-239">Customize character encoding</span></span>](system-text-json-character-encoding.md)
* [<span data-ttu-id="dd9e3-240">编写自定义序列化程序和反序列化程序</span><span class="sxs-lookup"><span data-stu-id="dd9e3-240">Write custom serializers and deserializers</span></span>](write-custom-serializer-deserializer.md)
* [<span data-ttu-id="dd9e3-241">编写用于 JSON 序列化的自定义转换器</span><span class="sxs-lookup"><span data-stu-id="dd9e3-241">Write custom converters for JSON serialization</span></span>](system-text-json-converters-how-to.md)
* [<span data-ttu-id="dd9e3-242">DateTime 和 DateTimeOffset 支持</span><span class="sxs-lookup"><span data-stu-id="dd9e3-242">DateTime and DateTimeOffset support</span></span>](../datetime/system-text-json-support.md)
* <span data-ttu-id="dd9e3-243">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="dd9e3-243">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
* <span data-ttu-id="dd9e3-244">[System.Text.Json.Serialization API 参考](xref:System.Text.Json.Serialization)</span><span class="sxs-lookup"><span data-stu-id="dd9e3-244">[System.Text.Json.Serialization API reference](xref:System.Text.Json.Serialization)</span></span>
