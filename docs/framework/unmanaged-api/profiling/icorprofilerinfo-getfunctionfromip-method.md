---
description: 了解详细信息： ICorProfilerInfo：： GetFunctionFromIP 方法
title: ICorProfilerInfo::GetFunctionFromIP 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetFunctionFromIP
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetFunctionFromIP
helpviewer_keywords:
- GetFunctionFromIP method [.NET Framework profiling]
- ICorProfilerInfo::GetFunctionFromIP method [.NET Framework profiling]
ms.assetid: f069802a-198f-46dd-9f09-4f77adffc9ba
topic_type:
- apiref
ms.openlocfilehash: 1acea6943e74e65e4359c7da590d3888736dbd6c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647591"
---
# <a name="icorprofilerinfogetfunctionfromip-method"></a><span data-ttu-id="c0780-103">ICorProfilerInfo::GetFunctionFromIP 方法</span><span class="sxs-lookup"><span data-stu-id="c0780-103">ICorProfilerInfo::GetFunctionFromIP Method</span></span>

<span data-ttu-id="c0780-104">将托管代码指令指针映射到 `FunctionID` 。</span><span class="sxs-lookup"><span data-stu-id="c0780-104">Maps a managed code instruction pointer to a `FunctionID`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0780-105">语法</span><span class="sxs-lookup"><span data-stu-id="c0780-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFunctionFromIP(  
    [in]  LPCBYTE    ip,  
    [out] FunctionID *pFunctionId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c0780-106">参数</span><span class="sxs-lookup"><span data-stu-id="c0780-106">Parameters</span></span>

- `ip`

  <span data-ttu-id="c0780-107">\[in] 托管代码中的指令指针。</span><span class="sxs-lookup"><span data-stu-id="c0780-107">\[in] The instruction pointer in managed code.</span></span>

- `pFunctionId`

  <span data-ttu-id="c0780-108">\[out] 返回的函数 ID。</span><span class="sxs-lookup"><span data-stu-id="c0780-108">\[out] The returned function ID.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0780-109">要求</span><span class="sxs-lookup"><span data-stu-id="c0780-109">Requirements</span></span>  

 <span data-ttu-id="c0780-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c0780-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0780-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c0780-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c0780-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c0780-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c0780-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0780-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0780-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="c0780-114">See also</span></span>

- [<span data-ttu-id="c0780-115">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="c0780-115">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
