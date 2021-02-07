---
description: 了解详细信息： QuotedPairReader 类
title: 'QuotedPairReader 类 (System.Net) '
ms.date: 06/12/2020
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.Mail.QuotedPairReader
- System.Net.Mail.QuotedPairReader.CountQuotedChars
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: 810a7b02948a1b7aa542a179563af9a6d79dd763
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699657"
---
# <a name="quotedpairreader-class"></a><span data-ttu-id="f63e7-103">QuotedPairReader 类</span><span class="sxs-lookup"><span data-stu-id="f63e7-103">QuotedPairReader class</span></span>

<span data-ttu-id="f63e7-104">确定在带引号的字符串中 (转义) 的引号字符。</span><span class="sxs-lookup"><span data-stu-id="f63e7-104">Determines which characters are quoted (escaped) in a quoted string.</span></span> <span data-ttu-id="f63e7-105">此类不能被继承。</span><span class="sxs-lookup"><span data-stu-id="f63e7-105">This class cannot be inherited.</span></span>

```csharp
internal static class QuotedPairReader
```

> [!WARNING]
> <span data-ttu-id="f63e7-106">此类是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="f63e7-106">This class is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="f63e7-107">在任何情况下，Microsoft 不支持在生产应用程序中使用此类。</span><span class="sxs-lookup"><span data-stu-id="f63e7-107">Microsoft does not support the use of this class in a production application under any circumstance.</span></span>

## <a name="countquotedchars-method"></a><span data-ttu-id="f63e7-108">CountQuotedChars 方法</span><span class="sxs-lookup"><span data-stu-id="f63e7-108">CountQuotedChars method</span></span>

<span data-ttu-id="f63e7-109">计算指定字符串中连续带引号的字符数（包括多个前面带引号的反斜杠）。</span><span class="sxs-lookup"><span data-stu-id="f63e7-109">Counts the number of consecutive quoted characters, including multiple preceding quoted backslashes, in the specified string.</span></span> <span data-ttu-id="f63e7-110">例如，给定的字符串 `a\\\b` 和索引 `4` ，该方法返回 `4` ，因为带有引号， `b` 因此是前面三个反斜杠。</span><span class="sxs-lookup"><span data-stu-id="f63e7-110">For example, given the string `a\\\b` and an index of `4`, the method returns `4`, because `b` is quoted and so are the three preceding backslashes.</span></span>

```csharp
internal static int CountQuotedChars(string data, int index, bool permitUnicodeEscaping)
```

### <a name="parameters"></a><span data-ttu-id="f63e7-111">参数</span><span class="sxs-lookup"><span data-stu-id="f63e7-111">Parameters</span></span>

- <span data-ttu-id="f63e7-112">`data` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="f63e7-112">`data` <xref:System.String></span></span>

  <span data-ttu-id="f63e7-113">用于对连续带引号字符进行计数的数据字符串。</span><span class="sxs-lookup"><span data-stu-id="f63e7-113">The data string in which to count consecutive quoted characters.</span></span>

- <span data-ttu-id="f63e7-114">`index` <xref:System.Int32></span><span class="sxs-lookup"><span data-stu-id="f63e7-114">`index` <xref:System.Int32></span></span>

  <span data-ttu-id="f63e7-115">指定字符串中的位置，最多包含和包括应对哪些连续的带引号字符进行计数。</span><span class="sxs-lookup"><span data-stu-id="f63e7-115">The position in the specified string up to and including which consecutive quoted characters should be counted.</span></span>

- <span data-ttu-id="f63e7-116">`permitUnicodeEscaping` <xref:System.Boolean></span><span class="sxs-lookup"><span data-stu-id="f63e7-116">`permitUnicodeEscaping` <xref:System.Boolean></span></span>

  <span data-ttu-id="f63e7-117">`true` 允许转义 Unicode 字符;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="f63e7-117">`true` to permit Unicode characters to be escaped; otherwise, `false`.</span></span>

### <a name="return-value"></a><span data-ttu-id="f63e7-118">返回值</span><span class="sxs-lookup"><span data-stu-id="f63e7-118">Return value</span></span>

<xref:System.Int32?displayProperty=nameWithType>

<span data-ttu-id="f63e7-119">`0` 如果指定索引处的字符未转义，则为; 否则为。否则，则为，最多包含中的字符（包括字符） `index` 。</span><span class="sxs-lookup"><span data-stu-id="f63e7-119">`0` if the character at the specified index is not escaped; otherwise, the number of consecutive quoted characters up to and including the character at `index`.</span></span>

### <a name="exceptions"></a><span data-ttu-id="f63e7-120">异常</span><span class="sxs-lookup"><span data-stu-id="f63e7-120">Exceptions</span></span>

<xref:System.FormatException?displayProperty=nameWithType>

<span data-ttu-id="f63e7-121">找到了一个转义的 Unicode 字符，但不允许这样做。</span><span class="sxs-lookup"><span data-stu-id="f63e7-121">An escaped Unicode character was found but is not permitted.</span></span>

## <a name="requirements"></a><span data-ttu-id="f63e7-122">要求</span><span class="sxs-lookup"><span data-stu-id="f63e7-122">Requirements</span></span>

<span data-ttu-id="f63e7-123">**命名空间：** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="f63e7-123">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="f63e7-124">**程序集：** System.dll 中的系统 () </span><span class="sxs-lookup"><span data-stu-id="f63e7-124">**Assembly:** System (in System.dll)</span></span>
