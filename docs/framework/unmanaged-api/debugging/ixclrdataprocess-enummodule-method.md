---
description: 了解详细信息： IXCLRDataProcess：： EnumModule 方法
title: IXCLRDataProcess：： EnumModule 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumModule Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumModule Method
helpviewer.keywords:
- IXCLRDataProcess::EnumModule Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 33b15da6939a0fb78a4eeafcf75e1a2b2f0d0ab1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800677"
---
# <a name="ixclrdataprocessenummodule-method"></a><span data-ttu-id="60981-103">IXCLRDataProcess：： EnumModule 方法</span><span class="sxs-lookup"><span data-stu-id="60981-103">IXCLRDataProcess::EnumModule Method</span></span>

<span data-ttu-id="60981-104">枚举此进程的模块。</span><span class="sxs-lookup"><span data-stu-id="60981-104">Enumerates the modules of this process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="60981-105">语法</span><span class="sxs-lookup"><span data-stu-id="60981-105">Syntax</span></span>

```cpp
HRESULT EnumModule(
    [in, out] CLRDATA_ENUM  *handle,
    [out] IXCLRDataModule  **mod
);
```

## <a name="parameters"></a><span data-ttu-id="60981-106">参数</span><span class="sxs-lookup"><span data-stu-id="60981-106">Parameters</span></span>

`handle`\
<span data-ttu-id="60981-107">[in，out]用于枚举模块的句柄。</span><span class="sxs-lookup"><span data-stu-id="60981-107">[in, out] A handle for enumerating the modules.</span></span>

`mod`\
<span data-ttu-id="60981-108">弄枚举的模块。</span><span class="sxs-lookup"><span data-stu-id="60981-108">[out] The enumerated module.</span></span>

## <a name="remarks"></a><span data-ttu-id="60981-109">备注</span><span class="sxs-lookup"><span data-stu-id="60981-109">Remarks</span></span>

<span data-ttu-id="60981-110">提供的方法是接口的一部分 `IXCLRDataProcess` ，并且对应于虚拟方法表的第25个槽。</span><span class="sxs-lookup"><span data-stu-id="60981-110">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 25th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="60981-111">要求</span><span class="sxs-lookup"><span data-stu-id="60981-111">Requirements</span></span>

<span data-ttu-id="60981-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="60981-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="60981-113">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="60981-113">**Header:** None</span></span>  
<span data-ttu-id="60981-114">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="60981-114">**Library:** None</span></span>  
<span data-ttu-id="60981-115">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="60981-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="60981-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="60981-116">See also</span></span>

- [<span data-ttu-id="60981-117">CLRDataSourceType 枚举</span><span class="sxs-lookup"><span data-stu-id="60981-117">CLRDataSourceType Enumeration</span></span>](clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="60981-118">调试</span><span class="sxs-lookup"><span data-stu-id="60981-118">Debugging</span></span>](index.md)
- [<span data-ttu-id="60981-119">IXCLRDataModule 接口</span><span class="sxs-lookup"><span data-stu-id="60981-119">IXCLRDataModule Interface</span></span>](ixclrdatamodule-interface.md)
- [<span data-ttu-id="60981-120">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="60981-120">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
