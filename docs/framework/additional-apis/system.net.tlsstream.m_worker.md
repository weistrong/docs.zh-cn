---
description: 了解详细信息： TlsStream.m_Worker 字段
title: 'TlsStream.m_Worker 字段 (System.Net) '
ms.date: 10/21/2019
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.TlsStream.m_Worker
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: d929b0b1949bc1902425c016bfd770d4c66a3257
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699514"
---
# <a name="tlsstreamm_worker-field"></a><span data-ttu-id="ed935-103">TlsStream.m_Worker 字段</span><span class="sxs-lookup"><span data-stu-id="ed935-103">TlsStream.m_Worker Field</span></span>

<span data-ttu-id="ed935-104">表示 SSL 流的状态。</span><span class="sxs-lookup"><span data-stu-id="ed935-104">Represents the state of the SSL stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed935-105">语法</span><span class="sxs-lookup"><span data-stu-id="ed935-105">Syntax</span></span>

```csharp
private SslState m_Worker;
```

## <a name="field-value"></a><span data-ttu-id="ed935-106">字段值</span><span class="sxs-lookup"><span data-stu-id="ed935-106">Field value</span></span>

`System.Net.Security.SslState`  
<span data-ttu-id="ed935-107">SSL 流的状态。</span><span class="sxs-lookup"><span data-stu-id="ed935-107">The state of the SSL stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed935-108">备注</span><span class="sxs-lookup"><span data-stu-id="ed935-108">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="ed935-109">此 `TlsStream.m_Worker` 字段是专用的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="ed935-109">The `TlsStream.m_Worker` field is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="ed935-110">在任何情况下，Microsoft 不支持在生产应用程序中使用此字段。</span><span class="sxs-lookup"><span data-stu-id="ed935-110">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed935-111">要求</span><span class="sxs-lookup"><span data-stu-id="ed935-111">Requirements</span></span>

<span data-ttu-id="ed935-112">**命名空间：** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="ed935-112">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="ed935-113">**程序集：** System.dll 中的系统 () </span><span class="sxs-lookup"><span data-stu-id="ed935-113">**Assembly:** System (in System.dll)</span></span>

<span data-ttu-id="ed935-114">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="ed935-114">**.NET Framework versions:** Available since 2.0.</span></span>
