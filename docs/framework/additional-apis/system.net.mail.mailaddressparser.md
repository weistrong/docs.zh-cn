---
description: 了解详细信息： MailAddressParser 类
title: 'MailAddressParser 类 (System.Net) '
ms.date: 06/12/2020
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.Mail.MailAddressParser
- System.Net.Mail.MailAddressParser.ParseAddress
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: 5ad534e731e283f5449b3b8cc8e87628716da9b0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699761"
---
# <a name="mailaddressparser-class"></a><span data-ttu-id="f05b1-103">MailAddressParser 类</span><span class="sxs-lookup"><span data-stu-id="f05b1-103">MailAddressParser class</span></span>

<span data-ttu-id="f05b1-104">如 RFC 2822 中所述分析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="f05b1-104">Parses email addresses as described in RFC 2822.</span></span> <span data-ttu-id="f05b1-105">此类不能被继承。</span><span class="sxs-lookup"><span data-stu-id="f05b1-105">This class cannot be inherited.</span></span>

```csharp
internal static class MailAddressParser
```

> [!WARNING]
> <span data-ttu-id="f05b1-106">此类是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="f05b1-106">This class is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="f05b1-107">在任何情况下，Microsoft 不支持在生产应用程序中使用此类。</span><span class="sxs-lookup"><span data-stu-id="f05b1-107">Microsoft does not support the use of this class in a production application under any circumstance.</span></span>

## <a name="parseaddress-method"></a><span data-ttu-id="f05b1-108">ParseAddress 方法</span><span class="sxs-lookup"><span data-stu-id="f05b1-108">ParseAddress method</span></span>

<span data-ttu-id="f05b1-109">分析指定字符串中的单个电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="f05b1-109">Parses a single email address from the specified string.</span></span>

```csharp
internal static MailAddress ParseAddress(string data)
```

### <a name="parameters"></a><span data-ttu-id="f05b1-110">参数</span><span class="sxs-lookup"><span data-stu-id="f05b1-110">Parameters</span></span>

<span data-ttu-id="f05b1-111">`data` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="f05b1-111">`data` <xref:System.String></span></span>

<span data-ttu-id="f05b1-112">包含要分析的电子邮件地址的字符串。</span><span class="sxs-lookup"><span data-stu-id="f05b1-112">The string that contains an email address to be parsed.</span></span>

### <a name="return-value"></a><span data-ttu-id="f05b1-113">返回值</span><span class="sxs-lookup"><span data-stu-id="f05b1-113">Return value</span></span>

<xref:System.Net.Mail.MailAddress>

<span data-ttu-id="f05b1-114">有效的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="f05b1-114">A valid email address.</span></span>

### <a name="exceptions"></a><span data-ttu-id="f05b1-115">异常</span><span class="sxs-lookup"><span data-stu-id="f05b1-115">Exceptions</span></span>

<xref:System.FormatException?displayProperty=nameWithType>

<span data-ttu-id="f05b1-116">电子邮件地址无效。</span><span class="sxs-lookup"><span data-stu-id="f05b1-116">The email address is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="f05b1-117">要求</span><span class="sxs-lookup"><span data-stu-id="f05b1-117">Requirements</span></span>

<span data-ttu-id="f05b1-118">**命名空间：** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="f05b1-118">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="f05b1-119">**程序集：** System.dll 中的系统 () </span><span class="sxs-lookup"><span data-stu-id="f05b1-119">**Assembly:** System (in System.dll)</span></span>
