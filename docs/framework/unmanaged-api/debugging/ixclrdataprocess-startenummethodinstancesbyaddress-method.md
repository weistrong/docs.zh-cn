---
description: 了解详细信息： IXCLRDataProcess：： StartEnumMethodInstancesByAddress 方法
title: IXCLRDataProcess：： StartEnumMethodInstancesByAddress 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::StartEnumMethodInstancesByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::StartEnumMethodInstancesByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::StartEnumMethodInstancesByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 155d09192b60b8671435abb439f07dfbb290bc87
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800580"
---
# <a name="ixclrdataprocessstartenummethodinstancesbyaddress-method"></a><span data-ttu-id="a23af-103">IXCLRDataProcess：： StartEnumMethodInstancesByAddress 方法</span><span class="sxs-lookup"><span data-stu-id="a23af-103">IXCLRDataProcess::StartEnumMethodInstancesByAddress Method</span></span>

<span data-ttu-id="a23af-104">提供用于枚举 `AppDomain` 从给定地址开始的方法实例的句柄。</span><span class="sxs-lookup"><span data-stu-id="a23af-104">Provides a handle to enumerate the method instances of `AppDomain` starting at a given address.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="a23af-105">语法</span><span class="sxs-lookup"><span data-stu-id="a23af-105">Syntax</span></span>

```cpp
HRESULT StartEnumMethodInstancesByAddress(
    [in] CLRDATA_ADDRESS     address,
    [in] IXCLRDataAppDomain *appDomain,
    [out] CLRDATA_ENUM      *handle
);
```

## <a name="parameters"></a><span data-ttu-id="a23af-106">参数</span><span class="sxs-lookup"><span data-stu-id="a23af-106">Parameters</span></span>

`address`\
<span data-ttu-id="a23af-107">中第一个方法实例的地址。</span><span class="sxs-lookup"><span data-stu-id="a23af-107">[in] The address of the first method instance.</span></span>

`appDomain`\
<span data-ttu-id="a23af-108">中方法实例的 AppDomain。</span><span class="sxs-lookup"><span data-stu-id="a23af-108">[in] The AppDomain of the method instances.</span></span>

`handle`\
<span data-ttu-id="a23af-109">弄枚举方法实例的句柄。</span><span class="sxs-lookup"><span data-stu-id="a23af-109">[out] A handle for enumerating the method instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="a23af-110">备注</span><span class="sxs-lookup"><span data-stu-id="a23af-110">Remarks</span></span>

<span data-ttu-id="a23af-111">提供的方法是接口的一部分 `IXCLRDataProcess` ，并且对应于虚拟方法表的第28个槽。</span><span class="sxs-lookup"><span data-stu-id="a23af-111">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 28th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="a23af-112">要求</span><span class="sxs-lookup"><span data-stu-id="a23af-112">Requirements</span></span>

<span data-ttu-id="a23af-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a23af-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="a23af-114">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="a23af-114">**Header:** None</span></span>  
<span data-ttu-id="a23af-115">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="a23af-115">**Library:** None</span></span>  
<span data-ttu-id="a23af-116">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="a23af-116">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="a23af-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="a23af-117">See also</span></span>

- [<span data-ttu-id="a23af-118">CLRDataSourceType 枚举</span><span class="sxs-lookup"><span data-stu-id="a23af-118">CLRDataSourceType Enumeration</span></span>](clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="a23af-119">调试</span><span class="sxs-lookup"><span data-stu-id="a23af-119">Debugging</span></span>](index.md)
- [<span data-ttu-id="a23af-120">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="a23af-120">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
