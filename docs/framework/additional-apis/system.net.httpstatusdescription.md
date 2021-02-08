---
description: 了解详细信息： HttpStatusDescription 类
title: 'HttpStatusDescription 类 (System.Net) '
ms.date: 06/12/2020
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.HttpStatusDescription
- System.Net.HttpStatusDescription.Get
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: fa135a6421397ce6b7be2af05d66aa8e81beafb7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802497"
---
# <a name="httpstatusdescription-class"></a><span data-ttu-id="89670-103">HttpStatusDescription 类</span><span class="sxs-lookup"><span data-stu-id="89670-103">HttpStatusDescription class</span></span>

<span data-ttu-id="89670-104">提供标准 HTTP 状态说明。</span><span class="sxs-lookup"><span data-stu-id="89670-104">Provides standard HTTP status descriptions.</span></span> <span data-ttu-id="89670-105">此类不能被继承。</span><span class="sxs-lookup"><span data-stu-id="89670-105">This class cannot be inherited.</span></span>

```csharp
internal static class HttpStatusDescription
```

> [!WARNING]
> <span data-ttu-id="89670-106">此类是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="89670-106">This class is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="89670-107">在任何情况下，Microsoft 不支持在生产应用程序中使用此类。</span><span class="sxs-lookup"><span data-stu-id="89670-107">Microsoft does not support the use of this class in a production application under any circumstance.</span></span>

## <a name="get-method"></a><span data-ttu-id="89670-108">Get 方法</span><span class="sxs-lookup"><span data-stu-id="89670-108">Get method</span></span>

<span data-ttu-id="89670-109">返回与指定的 HTTP 状态代码相关联的说明。</span><span class="sxs-lookup"><span data-stu-id="89670-109">Returns the description associated with the specified HTTP status code.</span></span>

```csharp
internal static string Get(int code)
```

### <a name="parameters"></a><span data-ttu-id="89670-110">参数</span><span class="sxs-lookup"><span data-stu-id="89670-110">Parameters</span></span>

<span data-ttu-id="89670-111">`code` <xref:System.Int32></span><span class="sxs-lookup"><span data-stu-id="89670-111">`code` <xref:System.Int32></span></span>

<span data-ttu-id="89670-112">HTTP 状态代码，例如 `404` 。</span><span class="sxs-lookup"><span data-stu-id="89670-112">The HTTP status code, for example, `404`.</span></span>

### <a name="return-value"></a><span data-ttu-id="89670-113">返回值</span><span class="sxs-lookup"><span data-stu-id="89670-113">Return value</span></span>

<xref:System.String?displayProperty=nameWithType>

<span data-ttu-id="89670-114">HTTP 状态说明。</span><span class="sxs-lookup"><span data-stu-id="89670-114">The HTTP status description.</span></span>

## <a name="requirements"></a><span data-ttu-id="89670-115">要求</span><span class="sxs-lookup"><span data-stu-id="89670-115">Requirements</span></span>

<span data-ttu-id="89670-116">**命名空间：** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="89670-116">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="89670-117">**程序集：** System.dll 中的系统 () </span><span class="sxs-lookup"><span data-stu-id="89670-117">**Assembly:** System (in System.dll)</span></span>
