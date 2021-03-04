---
description: 了解详细信息： ICorProfilerInfo10：： ResumeRuntime 方法
title: ICorProfilerInfo10::ResumeRuntime
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo10.ResumeRuntime
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: 6e40270377fab07e110bbd1ea0f94e4e10c3d033
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102103577"
---
# <a name="icorprofilerinfo10resumeruntime-method"></a><span data-ttu-id="fdefc-103">ICorProfilerInfo10：： ResumeRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="fdefc-103">ICorProfilerInfo10::ResumeRuntime Method</span></span>

<span data-ttu-id="fdefc-104">恢复运行时，而不执行 GC。</span><span class="sxs-lookup"><span data-stu-id="fdefc-104">Resumes the runtime without performing a GC.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdefc-105">语法</span><span class="sxs-lookup"><span data-stu-id="fdefc-105">Syntax</span></span>

```cpp
HRESULT ResumeRuntime();
```

## <a name="requirements"></a><span data-ttu-id="fdefc-106">要求</span><span class="sxs-lookup"><span data-stu-id="fdefc-106">Requirements</span></span>

<span data-ttu-id="fdefc-107">**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="fdefc-107">**Platforms:** See [.NET Core supported operating systems](../../../core/install/windows.md?pivots=os-windows).</span></span>

<span data-ttu-id="fdefc-108">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fdefc-108">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="fdefc-109">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fdefc-109">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="fdefc-110">**.Net 版本：**[!INCLUDE[net_core_30](../../../../includes/net-core-30-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fdefc-110">**.NET Versions:** [!INCLUDE[net_core_30](../../../../includes/net-core-30-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="fdefc-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fdefc-111">See also</span></span>

- [<span data-ttu-id="fdefc-112">ICorProfilerInfo10 接口</span><span class="sxs-lookup"><span data-stu-id="fdefc-112">ICorProfilerInfo10 Interface</span></span>](icorprofilerinfo10-interface.md)
