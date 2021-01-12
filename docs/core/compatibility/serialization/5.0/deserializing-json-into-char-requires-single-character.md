---
title: 中断性变更：反序列化 char 需要单字符的字符串
description: 了解 .NET 5.0 中的以下中断性变更：反序列化为 char 目标时，System.Text.Json 在 JSON 中需要单字符字符串。
ms.date: 12/15/2020
ms.openlocfilehash: 39a2d25b00bf8855cfbf46a4d78b8545052703e5
ms.sourcegitcommit: 635a0ff775d2447a81ef7233a599b8f88b162e5d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "97633866"
---
# <a name="systemtextjson-requires-single-char-string-to-deserialize-a-char"></a><span data-ttu-id="ecf58-103">System.Text.Json 需要使用单字符字符串才能反序列化 char</span><span class="sxs-lookup"><span data-stu-id="ecf58-103">System.Text.Json requires single-char string to deserialize a char</span></span>

<span data-ttu-id="ecf58-104">若要成功使用 <xref:System.Text.Json> 反序列化 <xref:System.Char>，JSON 字符串必须包含单字符。</span><span class="sxs-lookup"><span data-stu-id="ecf58-104">To successfully deserialize a <xref:System.Char> using <xref:System.Text.Json>, the JSON string must contain a single character.</span></span>

## <a name="change-description"></a><span data-ttu-id="ecf58-105">更改描述</span><span class="sxs-lookup"><span data-stu-id="ecf58-105">Change description</span></span>

<span data-ttu-id="ecf58-106">在 .NET 早期版本中，JSON 中的多 `char` 字符串会被成功地反序列化为 `char` 属性或字段。</span><span class="sxs-lookup"><span data-stu-id="ecf58-106">In previous .NET versions, a multi-`char` string in the JSON is successfully deserialized to a `char` property or field.</span></span> <span data-ttu-id="ecf58-107">只使用字符串的第一个 `char`，如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="ecf58-107">Only the first `char` of the string is used, as in the following example:</span></span>

```csharp
// .NET Core 3.0 and 3.1: Returns the first char 'a'.
// .NET 5.0 and later: Throws JsonException because payload has more than one char.
char deserializedChar = JsonSerializer.Deserialize<char>("\"abc\"");
```

<span data-ttu-id="ecf58-108">在 .NET 5.0 和更高版本中，当反序列化目标为 `char` 时，除单 `char` 字符串以外的任何内容都会导致引发 <xref:System.Text.Json.JsonException>。</span><span class="sxs-lookup"><span data-stu-id="ecf58-108">In .NET 5.0 and later, anything other than a single-`char` string causes a <xref:System.Text.Json.JsonException> to be thrown when the deserialization target is a `char`.</span></span> <span data-ttu-id="ecf58-109">以下示例字符串在所有 .NET 版本中都已成功反序列化：</span><span class="sxs-lookup"><span data-stu-id="ecf58-109">The following example string is successfully deserialized in all .NET versions:</span></span>

```csharp
// Correct usage.
char deserializedChar = JsonSerializer.Deserialize<char>("\"a\"");
```

## <a name="version-introduced"></a><span data-ttu-id="ecf58-110">引入的版本</span><span class="sxs-lookup"><span data-stu-id="ecf58-110">Version introduced</span></span>

<span data-ttu-id="ecf58-111">5.0</span><span class="sxs-lookup"><span data-stu-id="ecf58-111">5.0</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="ecf58-112">更改原因</span><span class="sxs-lookup"><span data-stu-id="ecf58-112">Reason for change</span></span>

<span data-ttu-id="ecf58-113">仅在提供的有效负载对目标类型有效时，反序列化分析才会成功。</span><span class="sxs-lookup"><span data-stu-id="ecf58-113">Parsing for deserialization should only succeed when the provided payload is valid for the target type.</span></span> <span data-ttu-id="ecf58-114">对于 `char` 类型，唯一有效的有效负载是单 `char` 字符串。</span><span class="sxs-lookup"><span data-stu-id="ecf58-114">For a `char` type, the only valid payload is a single-`char` string.</span></span>

## <a name="recommended-action"></a><span data-ttu-id="ecf58-115">建议的操作</span><span class="sxs-lookup"><span data-stu-id="ecf58-115">Recommended action</span></span>

<span data-ttu-id="ecf58-116">将 JSON 反序列化为 `char` 目标时，请确保字符串包含单 `char`。</span><span class="sxs-lookup"><span data-stu-id="ecf58-116">When you deserialize JSON into a `char` target, make sure the string consists of a single `char`.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="ecf58-117">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="ecf58-117">Affected APIs</span></span>

- <xref:System.Text.Json.JsonSerializer.Deserialize%2A?displayProperty=fullName>

<!--

### Affected APIs

- `Overload:System.Text.Json.JsonSerializer.Deserialize`

### Category

Serialization

-->
