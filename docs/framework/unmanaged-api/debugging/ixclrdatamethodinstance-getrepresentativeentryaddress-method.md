---
description: 了解详细信息： IXCLRDataMethodInstance：： GetRepresentativeEntryAddress 方法
title: IXCLRDataMethodInstance：： GetRepresentativeEntryAddress 方法
ms.date: 02/01/2019
api.name:
- IXCLRDataMethodInstance::GetRepresentativeEntryAddress
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodInstance::GetRepresentativeEntryAddress
helpviewer.keywords:
- IXCLRDataMethodInstance::GetRepresentativeEntryAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 21cc6c50ab460c0e3a3a92c11fcfe51d4a2a4606
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800794"
---
# <a name="ixclrdatamethodinstancegetrepresentativeentryaddress-method"></a><span data-ttu-id="557d1-103">IXCLRDataMethodInstance：： GetRepresentativeEntryAddress 方法</span><span class="sxs-lookup"><span data-stu-id="557d1-103">IXCLRDataMethodInstance::GetRepresentativeEntryAddress Method</span></span>

<span data-ttu-id="557d1-104">获取方法的所有可能入口点的本机编译的最具代表性的入口点地址。</span><span class="sxs-lookup"><span data-stu-id="557d1-104">Gets the most representative entry point address for the native compilation of all the possible entry points for a method.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="557d1-105">语法</span><span class="sxs-lookup"><span data-stu-id="557d1-105">Syntax</span></span>

```cpp
HRESULT GetRepresentativeEntryAddress(
    [out] CLRDATA_ADDRESS* addr
);
```

## <a name="parameters"></a><span data-ttu-id="557d1-106">参数</span><span class="sxs-lookup"><span data-stu-id="557d1-106">Parameters</span></span>

`addr`\
<span data-ttu-id="557d1-107">弄方法的最具代表性的本机入口点的地址。</span><span class="sxs-lookup"><span data-stu-id="557d1-107">[out] The address of the most representative native entry point for the method.</span></span>

## <a name="remarks"></a><span data-ttu-id="557d1-108">备注</span><span class="sxs-lookup"><span data-stu-id="557d1-108">Remarks</span></span>

<span data-ttu-id="557d1-109">提供的方法是[ `IXCLRDataMethodInstance` 接口](ixclrdatamethodinstance-interface.md)的一部分，并且对应于虚拟方法表的第20个槽。</span><span class="sxs-lookup"><span data-stu-id="557d1-109">The provided method is part of the [`IXCLRDataMethodInstance` interface](ixclrdatamethodinstance-interface.md) and corresponds to the 20th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="557d1-110">要求</span><span class="sxs-lookup"><span data-stu-id="557d1-110">Requirements</span></span>

<span data-ttu-id="557d1-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="557d1-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="557d1-112">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="557d1-112">**Header:** None</span></span>  
<span data-ttu-id="557d1-113">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="557d1-113">**Library:** None</span></span>  
<span data-ttu-id="557d1-114">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="557d1-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="557d1-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="557d1-115">See also</span></span>

- [<span data-ttu-id="557d1-116">调试</span><span class="sxs-lookup"><span data-stu-id="557d1-116">Debugging</span></span>](index.md)
- [<span data-ttu-id="557d1-117">IXCLRDataMethodInstance 接口</span><span class="sxs-lookup"><span data-stu-id="557d1-117">IXCLRDataMethodInstance Interface</span></span>](ixclrdatamethodinstance-interface.md)
