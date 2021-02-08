---
description: 了解详细信息： IXCLRDataProcess：： EndEnumModules 方法
title: IXCLRDataProcess：： EndEnumModules 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EndEnumModules Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EndEnumModules Method
helpviewer.keywords:
- IXCLRDataProcess::EndEnumModules Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 454d4fa3616f9ba8312dc3d1ac02c228625aa488
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800703"
---
# <a name="ixclrdataprocessendenummodules-method"></a><span data-ttu-id="f6961-103">IXCLRDataProcess：： EndEnumModules 方法</span><span class="sxs-lookup"><span data-stu-id="f6961-103">IXCLRDataProcess::EndEnumModules Method</span></span>

<span data-ttu-id="f6961-104">释放模块枚举期间使用的内部迭代器所使用的资源。</span><span class="sxs-lookup"><span data-stu-id="f6961-104">Releases the resources used by internal iterators used during module enumeration.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="f6961-105">语法</span><span class="sxs-lookup"><span data-stu-id="f6961-105">Syntax</span></span>

```cpp
HRESULT EndEnumModules(
    [in] CLRDATA_ENUM handle
);
```

## <a name="parameters"></a><span data-ttu-id="f6961-106">参数</span><span class="sxs-lookup"><span data-stu-id="f6961-106">Parameters</span></span>

`handle`\
<span data-ttu-id="f6961-107">弄用于枚举模块的句柄。</span><span class="sxs-lookup"><span data-stu-id="f6961-107">[out] A handle for enumerating the modules.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6961-108">备注</span><span class="sxs-lookup"><span data-stu-id="f6961-108">Remarks</span></span>

<span data-ttu-id="f6961-109">提供的方法是接口的一部分 `IXCLRDataProcess` ，并且对应于虚拟方法表的26个槽。</span><span class="sxs-lookup"><span data-stu-id="f6961-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 26th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6961-110">要求</span><span class="sxs-lookup"><span data-stu-id="f6961-110">Requirements</span></span>

<span data-ttu-id="f6961-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f6961-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>
<span data-ttu-id="f6961-112">**标头：** 无 **库：** 无 **.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="f6961-112">**Header:** None **Library:** None **.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="f6961-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="f6961-113">See also</span></span>

- [<span data-ttu-id="f6961-114">调试</span><span class="sxs-lookup"><span data-stu-id="f6961-114">Debugging</span></span>](index.md)
- [<span data-ttu-id="f6961-115">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="f6961-115">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
