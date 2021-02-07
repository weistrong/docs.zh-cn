---
description: 了解详细信息： SslState. SslProtocol 属性
title: SslState)  (系统 .Net。安全
ms.date: 10/21/2019
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.Security.SslState.SslProtocol
- System.Net.Security.SslState.get_SslProtocol
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: b0b9bebf23fcd8d643d06f1cff10c260c77a7c08
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699618"
---
# <a name="sslstatesslprotocol-property"></a><span data-ttu-id="69932-103">SslState. SslProtocol 属性</span><span class="sxs-lookup"><span data-stu-id="69932-103">SslState.SslProtocol Property</span></span>

<span data-ttu-id="69932-104">获取 SSL 协议版本。</span><span class="sxs-lookup"><span data-stu-id="69932-104">Gets the SSL protocol versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="69932-105">语法</span><span class="sxs-lookup"><span data-stu-id="69932-105">Syntax</span></span>

```csharp
internal SslProtocols SslProtocol { get; }
```

## <a name="property-value"></a><span data-ttu-id="69932-106">属性值</span><span class="sxs-lookup"><span data-stu-id="69932-106">Property value</span></span>

<xref:System.Security.Authentication.SslProtocols>  
<span data-ttu-id="69932-107">枚举值的按位组合，这些枚举值指定 SSL 协议版本。</span><span class="sxs-lookup"><span data-stu-id="69932-107">A bitwise combination of the enumeration values that specify the SSL protocol versions.</span></span>

## <a name="remarks"></a><span data-ttu-id="69932-108">备注</span><span class="sxs-lookup"><span data-stu-id="69932-108">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="69932-109">`SslState.SslProtocol`属性是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="69932-109">The `SslState.SslProtocol` property is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="69932-110">在任何情况下，Microsoft 不支持在生产应用程序中使用此属性。</span><span class="sxs-lookup"><span data-stu-id="69932-110">Microsoft does not support the use of this property in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="69932-111">要求</span><span class="sxs-lookup"><span data-stu-id="69932-111">Requirements</span></span>

<span data-ttu-id="69932-112">**命名空间：** <xref:System.Net.Security></span><span class="sxs-lookup"><span data-stu-id="69932-112">**Namespace:** <xref:System.Net.Security></span></span>

<span data-ttu-id="69932-113">**程序集：** System.dll 中的系统 () </span><span class="sxs-lookup"><span data-stu-id="69932-113">**Assembly:** System (in System.dll)</span></span>

<span data-ttu-id="69932-114">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="69932-114">**.NET Framework versions:** Available since 2.0.</span></span>
