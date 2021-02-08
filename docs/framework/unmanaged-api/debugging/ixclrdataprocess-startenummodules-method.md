---
description: 了解详细信息： IXCLRDataProcess：： StartEnumModules 方法
title: IXCLRDataProcess：： StartEnumModules 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::StartEnumModules Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::StartEnumModules Method
helpviewer.keywords:
- IXCLRDataProcess::StartEnumModules Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 2e90c646ee8815ec10ce0bbd7538f13d7b5dcf8a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800573"
---
# <a name="ixclrdataprocessstartenummodules-method"></a><span data-ttu-id="6bc74-103">IXCLRDataProcess：： StartEnumModules 方法</span><span class="sxs-lookup"><span data-stu-id="6bc74-103">IXCLRDataProcess::StartEnumModules Method</span></span>

<span data-ttu-id="6bc74-104">提供枚举进程的模块的句柄。</span><span class="sxs-lookup"><span data-stu-id="6bc74-104">Provides a handle to enumerate the modules of a process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="6bc74-105">语法</span><span class="sxs-lookup"><span data-stu-id="6bc74-105">Syntax</span></span>

```cpp
HRESULT StartEnumModules(
    [out] CLRDATA_ENUM *handle
);
```

## <a name="parameters"></a><span data-ttu-id="6bc74-106">参数</span><span class="sxs-lookup"><span data-stu-id="6bc74-106">Parameters</span></span>

`handle`\
<span data-ttu-id="6bc74-107">弄用于枚举模块的句柄。</span><span class="sxs-lookup"><span data-stu-id="6bc74-107">[out] A handle for enumerating the modules.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bc74-108">备注</span><span class="sxs-lookup"><span data-stu-id="6bc74-108">Remarks</span></span>

<span data-ttu-id="6bc74-109">提供的方法是接口的一部分 `IXCLRDataProcess` ，并且对应于虚拟方法表的24日槽。</span><span class="sxs-lookup"><span data-stu-id="6bc74-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 24th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bc74-110">要求</span><span class="sxs-lookup"><span data-stu-id="6bc74-110">Requirements</span></span>

<span data-ttu-id="6bc74-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6bc74-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="6bc74-112">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="6bc74-112">**Header:** None</span></span>  
<span data-ttu-id="6bc74-113">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="6bc74-113">**Library:** None</span></span>  
<span data-ttu-id="6bc74-114">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="6bc74-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="6bc74-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="6bc74-115">See also</span></span>

- [<span data-ttu-id="6bc74-116">CLRDataSourceType 枚举</span><span class="sxs-lookup"><span data-stu-id="6bc74-116">CLRDataSourceType Enumeration</span></span>](clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="6bc74-117">调试</span><span class="sxs-lookup"><span data-stu-id="6bc74-117">Debugging</span></span>](index.md)
- [<span data-ttu-id="6bc74-118">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="6bc74-118">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
