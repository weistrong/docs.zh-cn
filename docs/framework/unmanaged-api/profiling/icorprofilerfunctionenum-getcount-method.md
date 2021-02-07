---
description: 了解详细信息： ICorProfilerFunctionEnum：： GetCount 方法
title: ICorProfilerFunctionEnum::GetCount 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionEnum.GetCount Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionEnum::GetCount
helpviewer_keywords:
- ICorProfilerFunctionEnum::GetCount method [.NET Framework profiling]
- GetCount method, ICorProfilerFunctionEnum interface [.NET Framework profiling]
ms.assetid: 62ec65e3-3e9d-400b-ae61-d24b8963995b
topic_type:
- apiref
ms.openlocfilehash: a3eccfa31676636aff7379b4080bcb85a268df6c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737618"
---
# <a name="icorprofilerfunctionenumgetcount-method"></a><span data-ttu-id="49bc3-103">ICorProfilerFunctionEnum::GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="49bc3-103">ICorProfilerFunctionEnum::GetCount Method</span></span>

<span data-ttu-id="49bc3-104">获取应用程序加载的函数数量或探查器强制加载的函数数量。</span><span class="sxs-lookup"><span data-stu-id="49bc3-104">Gets the number of functions that were loaded by the application or forcibly loaded by the profiler.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49bc3-105">语法</span><span class="sxs-lookup"><span data-stu-id="49bc3-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCount([out] ULONG * pcelt);  
```  
  
## <a name="parameters"></a><span data-ttu-id="49bc3-106">参数</span><span class="sxs-lookup"><span data-stu-id="49bc3-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="49bc3-107">弄已加载的函数的数目。</span><span class="sxs-lookup"><span data-stu-id="49bc3-107">[out] The number of functions that were loaded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="49bc3-108">要求</span><span class="sxs-lookup"><span data-stu-id="49bc3-108">Requirements</span></span>  

 <span data-ttu-id="49bc3-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="49bc3-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="49bc3-110">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="49bc3-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="49bc3-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="49bc3-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="49bc3-112">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="49bc3-112">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49bc3-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="49bc3-113">See also</span></span>

- [<span data-ttu-id="49bc3-114">ICorProfilerFunctionEnum 接口</span><span class="sxs-lookup"><span data-stu-id="49bc3-114">ICorProfilerFunctionEnum Interface</span></span>](icorprofilerfunctionenum-interface.md)
- [<span data-ttu-id="49bc3-115">分析接口</span><span class="sxs-lookup"><span data-stu-id="49bc3-115">Profiling Interfaces</span></span>](profiling-interfaces.md)
