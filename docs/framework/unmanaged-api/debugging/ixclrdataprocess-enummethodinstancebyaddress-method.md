---
description: 了解详细信息： IXCLRDataProcess：： EnumMethodInstanceByAddress 方法
title: IXCLRDataProcess：： EnumMethodInstanceByAddress 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: a0d59956288e39be188628d10c63a52d09d17638
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800690"
---
# <a name="ixclrdataprocessenummethodinstancebyaddress-method"></a><span data-ttu-id="854f0-103">IXCLRDataProcess：： EnumMethodInstanceByAddress 方法</span><span class="sxs-lookup"><span data-stu-id="854f0-103">IXCLRDataProcess::EnumMethodInstanceByAddress Method</span></span>

<span data-ttu-id="854f0-104">枚举此进程的方法实例（从地址偏移量开始）。</span><span class="sxs-lookup"><span data-stu-id="854f0-104">Enumerates the method instances of this process starting at an address offset.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="854f0-105">语法</span><span class="sxs-lookup"><span data-stu-id="854f0-105">Syntax</span></span>

```cpp
HRESULT EnumMethodInstanceByAddress(
    [in] CLRDATA_ENUM              *handle,
    [out] IXCLRDataMethodInstance **method
);
```

## <a name="parameters"></a><span data-ttu-id="854f0-106">参数</span><span class="sxs-lookup"><span data-stu-id="854f0-106">Parameters</span></span>

`handle`\
<span data-ttu-id="854f0-107">中枚举方法实例的句柄。</span><span class="sxs-lookup"><span data-stu-id="854f0-107">[in] A handle for enumerating the method instances.</span></span>

`mod`\
<span data-ttu-id="854f0-108">弄枚举的方法实例。</span><span class="sxs-lookup"><span data-stu-id="854f0-108">[out] The enumerated method instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="854f0-109">备注</span><span class="sxs-lookup"><span data-stu-id="854f0-109">Remarks</span></span>

<span data-ttu-id="854f0-110">提供的方法是接口的一部分 `IXCLRDataProcess` ，并且对应于虚拟方法表的第29个槽。</span><span class="sxs-lookup"><span data-stu-id="854f0-110">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 29th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="854f0-111">要求</span><span class="sxs-lookup"><span data-stu-id="854f0-111">Requirements</span></span>

<span data-ttu-id="854f0-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="854f0-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>
<span data-ttu-id="854f0-113">**标头：** 无 **库：** 无 **.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="854f0-113">**Header:** None **Library:** None **.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="854f0-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="854f0-114">See also</span></span>

- [<span data-ttu-id="854f0-115">CLRDataSourceType 枚举</span><span class="sxs-lookup"><span data-stu-id="854f0-115">CLRDataSourceType Enumeration</span></span>](clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="854f0-116">调试</span><span class="sxs-lookup"><span data-stu-id="854f0-116">Debugging</span></span>](index.md)
- [<span data-ttu-id="854f0-117">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="854f0-117">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
