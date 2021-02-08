---
description: 了解详细信息： ICorDebugInternalFrame2：： GetFrameAddress 方法
title: ICorDebugInternalFrame2::GetFrameAddress 方法
ms.date: 03/30/2017
api_name:
- ICorDebugInternalFrame2.GetFrameAddress Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugInternalFrame2::GetFrameAddress
helpviewer_keywords:
- GetFrameAddress method [.NET Framework debugging]
- ICorDebugInternalFrame2::GetFrameAddress method [.NET Framework debugging]
ms.assetid: 4ee8d058-ffc8-4967-9133-a5adfef4e518
topic_type:
- apiref
ms.openlocfilehash: bb745424680c5b9a5277badfbe2d96db46e2e3d8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791109"
---
# <a name="icordebuginternalframe2getframeaddress-method"></a><span data-ttu-id="d8bd6-103">ICorDebugInternalFrame2::GetFrameAddress 方法</span><span class="sxs-lookup"><span data-stu-id="d8bd6-103">ICorDebugInternalFrame2::GetFrameAddress Method</span></span>

<span data-ttu-id="d8bd6-104">返回内部帧的堆栈地址。</span><span class="sxs-lookup"><span data-stu-id="d8bd6-104">Returns the stack address of the internal frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8bd6-105">语法</span><span class="sxs-lookup"><span data-stu-id="d8bd6-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFrameAddress([out] CORDB_ADDRESS *pAddress);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d8bd6-106">参数</span><span class="sxs-lookup"><span data-stu-id="d8bd6-106">Parameters</span></span>  

 `pAddress`  
 <span data-ttu-id="d8bd6-107">弄指向内部帧的的指针 `CORDB_ADDRESS` 。</span><span class="sxs-lookup"><span data-stu-id="d8bd6-107">[out] Pointer to the `CORDB_ADDRESS` for the internal frame.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d8bd6-108">返回值</span><span class="sxs-lookup"><span data-stu-id="d8bd6-108">Return Value</span></span>  

 <span data-ttu-id="d8bd6-109">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="d8bd6-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="d8bd6-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d8bd6-110">HRESULT</span></span>|<span data-ttu-id="d8bd6-111">说明</span><span class="sxs-lookup"><span data-stu-id="d8bd6-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d8bd6-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="d8bd6-112">S_OK</span></span>|<span data-ttu-id="d8bd6-113">已成功返回内部帧的地址。</span><span class="sxs-lookup"><span data-stu-id="d8bd6-113">The address of the internal frame was successfully returned.</span></span>|  
|<span data-ttu-id="d8bd6-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d8bd6-114">E_FAIL</span></span>|<span data-ttu-id="d8bd6-115">无法返回内部帧的地址。</span><span class="sxs-lookup"><span data-stu-id="d8bd6-115">The address of the internal frame could not be returned.</span></span>|  
|<span data-ttu-id="d8bd6-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d8bd6-116">E_INVALIDARG</span></span>|<span data-ttu-id="d8bd6-117">`pAddress` 为 `null`。</span><span class="sxs-lookup"><span data-stu-id="d8bd6-117">`pAddress` is `null`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d8bd6-118">备注</span><span class="sxs-lookup"><span data-stu-id="d8bd6-118">Remarks</span></span>  

 <span data-ttu-id="d8bd6-119">返回的值 `pAddress` 可用于确定内部帧相对于堆栈上其他帧的位置。</span><span class="sxs-lookup"><span data-stu-id="d8bd6-119">The value returned in `pAddress` can be used to determine the location of the internal frame relative to other frames on the stack.</span></span> <span data-ttu-id="d8bd6-120">即使在基于 IA-64 的计算机上，内部帧也仅驻留在堆栈上，并且没有指向后备存储的相应指针。</span><span class="sxs-lookup"><span data-stu-id="d8bd6-120">Even on IA-64-based computers, the internal frame lives on the stack only, and there is no corresponding pointer to a backing store.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8bd6-121">要求</span><span class="sxs-lookup"><span data-stu-id="d8bd6-121">Requirements</span></span>  

 <span data-ttu-id="d8bd6-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d8bd6-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8bd6-123">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d8bd6-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d8bd6-124">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d8bd6-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d8bd6-125">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8bd6-125">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8bd6-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="d8bd6-126">See also</span></span>

- [<span data-ttu-id="d8bd6-127">ICorDebugInternalFrame2 接口</span><span class="sxs-lookup"><span data-stu-id="d8bd6-127">ICorDebugInternalFrame2 Interface</span></span>](icordebuginternalframe2-interface.md)
- [<span data-ttu-id="d8bd6-128">调试接口</span><span class="sxs-lookup"><span data-stu-id="d8bd6-128">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="d8bd6-129">调试</span><span class="sxs-lookup"><span data-stu-id="d8bd6-129">Debugging</span></span>](index.md)
