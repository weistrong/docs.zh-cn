---
description: 了解详细信息： MailBnfHelper 类
title: 'MailBnfHelper 类 (System.Net) '
ms.date: 06/12/2020
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.Mime.MailBnfHelper
- System.Net.Mime.MailBnfHelper.Ascii7bitMaxValue
- System.Net.Mime.MailBnfHelper.Atext
- System.Net.Mime.MailBnfHelper.CR
- System.Net.Mime.MailBnfHelper.Ctext
- System.Net.Mime.MailBnfHelper.Dot
- System.Net.Mime.MailBnfHelper.EndComment
- System.Net.Mime.MailBnfHelper.LF
- System.Net.Mime.MailBnfHelper.Space
- System.Net.Mime.MailBnfHelper.StartComment
- System.Net.Mime.MailBnfHelper.Tab
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: 942b5c423d2f63985a8f7840f69d956bbade7582
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699644"
---
# <a name="mailbnfhelper-class"></a><span data-ttu-id="d8da9-103">MailBnfHelper 类</span><span class="sxs-lookup"><span data-stu-id="d8da9-103">MailBnfHelper class</span></span>

<span data-ttu-id="d8da9-104">包含用于分析 internet 邮件格式字符串的实用工具方法。</span><span class="sxs-lookup"><span data-stu-id="d8da9-104">Contains utility methods for parsing internet message-formatted strings.</span></span> <span data-ttu-id="d8da9-105">此类不能被继承。</span><span class="sxs-lookup"><span data-stu-id="d8da9-105">This class cannot be inherited.</span></span>

```csharp
internal static class MailBnfHelper
```

> [!WARNING]
> <span data-ttu-id="d8da9-106">此类是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="d8da9-106">This class is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="d8da9-107">在任何情况下，Microsoft 不支持在生产应用程序中使用此类。</span><span class="sxs-lookup"><span data-stu-id="d8da9-107">Microsoft does not support the use of this class in a production application under any circumstance.</span></span>

## <a name="ascii7bitmaxvalue-field"></a><span data-ttu-id="d8da9-108">Ascii7bitMaxValue 字段</span><span class="sxs-lookup"><span data-stu-id="d8da9-108">Ascii7bitMaxValue field</span></span>

<span data-ttu-id="d8da9-109">表示最大7位 Ascii 值。</span><span class="sxs-lookup"><span data-stu-id="d8da9-109">Represents the maximum 7-bit Ascii value.</span></span>

```csharp
internal static readonly int Ascii7bitMaxValue
```

## <a name="atext-field"></a><span data-ttu-id="d8da9-110">由于文本字段</span><span class="sxs-lookup"><span data-stu-id="d8da9-110">Atext field</span></span>

<span data-ttu-id="d8da9-111">表示原子中允许使用的字符。</span><span class="sxs-lookup"><span data-stu-id="d8da9-111">Represents the characters allowed in atoms.</span></span>

```csharp
internal static bool[] Atext
```

## <a name="cr-field"></a><span data-ttu-id="d8da9-112">CR 字段</span><span class="sxs-lookup"><span data-stu-id="d8da9-112">CR field</span></span>

<span data-ttu-id="d8da9-113">表示回车符。</span><span class="sxs-lookup"><span data-stu-id="d8da9-113">Represents the carriage-return character.</span></span>

```csharp
internal static readonly char CR
```

## <a name="ctext-field"></a><span data-ttu-id="d8da9-114">Ctext 字段</span><span class="sxs-lookup"><span data-stu-id="d8da9-114">Ctext field</span></span>

<span data-ttu-id="d8da9-115">表示注释内允许使用的字符。</span><span class="sxs-lookup"><span data-stu-id="d8da9-115">Represents the characters allowed inside of comments.</span></span>

```csharp
internal static bool[] Ctext
```

## <a name="dot-field"></a><span data-ttu-id="d8da9-116">点字段</span><span class="sxs-lookup"><span data-stu-id="d8da9-116">Dot field</span></span>

<span data-ttu-id="d8da9-117">表示 () 的全停止字符 `.` 。</span><span class="sxs-lookup"><span data-stu-id="d8da9-117">Represents the full-stop character (`.`).</span></span>

```csharp
internal static readonly char Dot
```

## <a name="endcomment-field"></a><span data-ttu-id="d8da9-118">EndComment 字段</span><span class="sxs-lookup"><span data-stu-id="d8da9-118">EndComment field</span></span>

<span data-ttu-id="d8da9-119">表示指定注释末尾的字符。</span><span class="sxs-lookup"><span data-stu-id="d8da9-119">Represents the character that specifies the end of a comment.</span></span>

```csharp
internal static readonly char EndComment
```

## <a name="lf-field"></a><span data-ttu-id="d8da9-120">LF 字段</span><span class="sxs-lookup"><span data-stu-id="d8da9-120">LF field</span></span>

<span data-ttu-id="d8da9-121">表示换行符。</span><span class="sxs-lookup"><span data-stu-id="d8da9-121">Represents the line-feed character.</span></span>

```csharp
internal static readonly char LF
```

## <a name="space-field"></a><span data-ttu-id="d8da9-122">空间字段</span><span class="sxs-lookup"><span data-stu-id="d8da9-122">Space field</span></span>

<span data-ttu-id="d8da9-123">表示空格字符。</span><span class="sxs-lookup"><span data-stu-id="d8da9-123">Represents the space character.</span></span>

```csharp
internal static readonly char Space
```

## <a name="startcomment-field"></a><span data-ttu-id="d8da9-124">StartComment 字段</span><span class="sxs-lookup"><span data-stu-id="d8da9-124">StartComment field</span></span>

<span data-ttu-id="d8da9-125">表示指定注释开头的字符。</span><span class="sxs-lookup"><span data-stu-id="d8da9-125">Represents the character that specifies the start of a comment.</span></span>

```csharp
internal static readonly char StartComment
```

## <a name="tab-field"></a><span data-ttu-id="d8da9-126">选项卡字段</span><span class="sxs-lookup"><span data-stu-id="d8da9-126">Tab field</span></span>

<span data-ttu-id="d8da9-127">表示制表符。</span><span class="sxs-lookup"><span data-stu-id="d8da9-127">Represents the tab character.</span></span>

```csharp
internal static readonly char Tab
```

## <a name="requirements"></a><span data-ttu-id="d8da9-128">要求</span><span class="sxs-lookup"><span data-stu-id="d8da9-128">Requirements</span></span>

<span data-ttu-id="d8da9-129">**命名空间：** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="d8da9-129">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="d8da9-130">**程序集：** System.dll 中的系统 () </span><span class="sxs-lookup"><span data-stu-id="d8da9-130">**Assembly:** System (in System.dll)</span></span>
