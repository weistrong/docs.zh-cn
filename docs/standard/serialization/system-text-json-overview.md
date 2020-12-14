---
title: 使用 C# 对 JSON 进行序列化和反序列化 - .NET
description: 本概述介绍了在 .NET 中对 JSON 进行序列化和反序列化的 System.Text.Json 命名空间功能。
ms.date: 01/10/2020
no-loc:
- System.Text.Json
- Newtonsoft.Json
helpviewer_keywords:
- JSON serialization
- serializing objects
- serialization
- objects, serializing
ms.openlocfilehash: cb5c15c2a5c336e2d5b4a3754fa7a02a370602f3
ms.sourcegitcommit: 81f1bba2c97a67b5ca76bcc57b37333ffca60c7b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2020
ms.locfileid: "97009880"
---
# <a name="json-serialization-and-deserialization-marshalling-and-unmarshalling-in-net---overview"></a><span data-ttu-id="5143b-103">.NET 中的 JSON 序列化和反序列化（封送和拆收）- 概述</span><span class="sxs-lookup"><span data-stu-id="5143b-103">JSON serialization and deserialization (marshalling and unmarshalling) in .NET - overview</span></span>

<span data-ttu-id="5143b-104">`System.Text.Json` 命名空间提供用于序列化和反序列化 JavaScript 对象表示法 (JSON) 的功能。</span><span class="sxs-lookup"><span data-stu-id="5143b-104">The `System.Text.Json` namespace provides functionality for serializing to and deserializing from JavaScript Object Notation (JSON).</span></span>

<span data-ttu-id="5143b-105">库的设计强调对广泛的功能集实现高性能和低内存分配。</span><span class="sxs-lookup"><span data-stu-id="5143b-105">The library design emphasizes high performance and low memory allocation over an extensive feature set.</span></span> <span data-ttu-id="5143b-106">内置的 UTF-8 支持可优化读写以 UTF-8 编码的 JSON 文本的过程，UTF-8 编码是针对 Web 上的数据和磁盘上的文件的最普遍的编码方式。</span><span class="sxs-lookup"><span data-stu-id="5143b-106">Built-in UTF-8 support optimizes the process of reading and writing JSON text encoded as UTF-8, which is the most prevalent encoding for data on the web and files on disk.</span></span>

<span data-ttu-id="5143b-107">库还提供了用于处理内存中文档对象模型 (DOM) 的类。</span><span class="sxs-lookup"><span data-stu-id="5143b-107">The library also provides classes for working with an in-memory document object model (DOM).</span></span> <span data-ttu-id="5143b-108">此功能允许对 JSON 文件或字符串中的元素进行随机只读访问。</span><span class="sxs-lookup"><span data-stu-id="5143b-108">This feature enables random read-only access of the elements in a JSON file or string.</span></span>

## <a name="how-to-get-the-library"></a><span data-ttu-id="5143b-109">如何获取库</span><span class="sxs-lookup"><span data-stu-id="5143b-109">How to get the library</span></span>

* <span data-ttu-id="5143b-110">该库是作为 .NET Core 3.0 及更高版本共享框架的一部分内置的。</span><span class="sxs-lookup"><span data-stu-id="5143b-110">The library is built-in as part of the shared framework for .NET Core 3.0 and later versions.</span></span>
* <span data-ttu-id="5143b-111">对于早期版本的框架，请安装 [System.Text.Json](https://www.nuget.org/packages/System.Text.Json) NuGet 包。</span><span class="sxs-lookup"><span data-stu-id="5143b-111">For earlier framework versions, install the [System.Text.Json](https://www.nuget.org/packages/System.Text.Json) NuGet package.</span></span> <span data-ttu-id="5143b-112">包支持以下框架：</span><span class="sxs-lookup"><span data-stu-id="5143b-112">The package supports:</span></span>

  * <span data-ttu-id="5143b-113">.NET Standard 2.0 及更高版本</span><span class="sxs-lookup"><span data-stu-id="5143b-113">.NET Standard 2.0 and later versions</span></span>
  * <span data-ttu-id="5143b-114">.NET Framework 4.7.2 及更高版本</span><span class="sxs-lookup"><span data-stu-id="5143b-114">.NET Framework 4.7.2 and later versions</span></span>
  * <span data-ttu-id="5143b-115">.NET Core 2.0、2.1 和 2.2</span><span class="sxs-lookup"><span data-stu-id="5143b-115">.NET Core 2.0, 2.1, and 2.2</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5143b-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="5143b-116">Additional resources</span></span>

* [<span data-ttu-id="5143b-117">如何使用库</span><span class="sxs-lookup"><span data-stu-id="5143b-117">How to use the library</span></span>](system-text-json-how-to.md)
* [<span data-ttu-id="5143b-118">对 JsonSerializerOptions 实例进行实例化</span><span class="sxs-lookup"><span data-stu-id="5143b-118">Instantiate JsonSerializerOptions instances</span></span>](system-text-json-configure-options.md)
* [<span data-ttu-id="5143b-119">启用不区分大小写的匹配</span><span class="sxs-lookup"><span data-stu-id="5143b-119">Enable case-insensitive matching</span></span>](system-text-json-character-casing.md)
* [<span data-ttu-id="5143b-120">自定义属性名称和值</span><span class="sxs-lookup"><span data-stu-id="5143b-120">Customize property names and values</span></span>](system-text-json-customize-properties.md)
* [<span data-ttu-id="5143b-121">忽略属性</span><span class="sxs-lookup"><span data-stu-id="5143b-121">Ignore properties</span></span>](system-text-json-ignore-properties.md)
* [<span data-ttu-id="5143b-122">允许无效的 JSON</span><span class="sxs-lookup"><span data-stu-id="5143b-122">Allow invalid JSON</span></span>](system-text-json-invalid-json.md)
* [<span data-ttu-id="5143b-123">处理溢出 JSON</span><span class="sxs-lookup"><span data-stu-id="5143b-123">Handle overflow JSON</span></span>](system-text-json-handle-overflow.md)
* [<span data-ttu-id="5143b-124">保留引用</span><span class="sxs-lookup"><span data-stu-id="5143b-124">Preserve references</span></span>](system-text-json-preserve-references.md)
* [<span data-ttu-id="5143b-125">不可变类型和非公共访问器</span><span class="sxs-lookup"><span data-stu-id="5143b-125">Immutable types and non-public accessors</span></span>](system-text-json-immutability.md)
* [<span data-ttu-id="5143b-126">多态序列化</span><span class="sxs-lookup"><span data-stu-id="5143b-126">Polymorphic serialization</span></span>](system-text-json-polymorphism.md)
* [<span data-ttu-id="5143b-127">从 Newtonsoft.Json 迁移到 System.Text.Json</span><span class="sxs-lookup"><span data-stu-id="5143b-127">Migrate from Newtonsoft.Json to System.Text.Json</span></span>](system-text-json-migrate-from-newtonsoft-how-to.md)
* [<span data-ttu-id="5143b-128">自定义字符编码</span><span class="sxs-lookup"><span data-stu-id="5143b-128">Customize character encoding</span></span>](system-text-json-character-encoding.md)
* [<span data-ttu-id="5143b-129">编写自定义序列化程序和反序列化程序</span><span class="sxs-lookup"><span data-stu-id="5143b-129">Write custom serializers and deserializers</span></span>](write-custom-serializer-deserializer.md)
* [<span data-ttu-id="5143b-130">编写用于 JSON 序列化的自定义转换器</span><span class="sxs-lookup"><span data-stu-id="5143b-130">Write custom converters for JSON serialization</span></span>](system-text-json-converters-how-to.md)
* [<span data-ttu-id="5143b-131">DateTime 和 DateTimeOffset 支持</span><span class="sxs-lookup"><span data-stu-id="5143b-131">DateTime and DateTimeOffset support</span></span>](../datetime/system-text-json-support.md)
* <span data-ttu-id="5143b-132">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="5143b-132">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
* <span data-ttu-id="5143b-133">[System.Text.Json.Serialization API 参考](xref:System.Text.Json.Serialization)</span><span class="sxs-lookup"><span data-stu-id="5143b-133">[System.Text.Json.Serialization API reference](xref:System.Text.Json.Serialization)</span></span>
