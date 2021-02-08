---
description: 了解详细信息： ICorDebugInternalFrame2：： IsCloserToLeaf 方法
title: ICorDebugInternalFrame2::IsCloserToLeaf 方法
ms.date: 03/30/2017
api_name:
- ICorDebugInternalFrame2.IsCloserToLeaf Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugInternalFrame2::IsCloserToLeaf
helpviewer_keywords:
- ICorDebugInternalFrame2::IsCloserToLeaf method [.NET Framework debugging]
- IsCloserToLeaf method [.NET Framework debugging]
ms.assetid: c1d3d1eb-8370-4f25-8297-3bd262b4740a
topic_type:
- apiref
ms.openlocfilehash: d773f8670f600a5bcd2a8dad7f23fe243195957c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801275"
---
# <a name="icordebuginternalframe2isclosertoleaf-method"></a><span data-ttu-id="6c76f-103">ICorDebugInternalFrame2::IsCloserToLeaf 方法</span><span class="sxs-lookup"><span data-stu-id="6c76f-103">ICorDebugInternalFrame2::IsCloserToLeaf Method</span></span>

<span data-ttu-id="6c76f-104">检查 `this` 内部帧是否接近于指定的 ICorDebugFrame 对象。</span><span class="sxs-lookup"><span data-stu-id="6c76f-104">Checks whether the `this` internal frame is closer to the leaf than the specified ICorDebugFrame object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c76f-105">语法</span><span class="sxs-lookup"><span data-stu-id="6c76f-105">Syntax</span></span>  
  
```cpp  
HRESULT IsCloserToLeaf([in] ICorDebugFrame * pFrameToCompare,  
                       [out] BOOL * pIsCloser);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6c76f-106">参数</span><span class="sxs-lookup"><span data-stu-id="6c76f-106">Parameters</span></span>  

 `pFrameToCompare`  
 <span data-ttu-id="6c76f-107">中指向比较对象的指针 `ICorDebugFrame` 。</span><span class="sxs-lookup"><span data-stu-id="6c76f-107">[in] A pointer to the comparison `ICorDebugFrame` object.</span></span>  
  
 `pIsCloser`  
 <span data-ttu-id="6c76f-108">[out] `true` 如果 `this` 内部帧比指定的帧更接近叶 `pFrameToCompare` ，则为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="6c76f-108">[out] `true` if the `this` internal frame is closer to the leaf than the frame specified by `pFrameToCompare`; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6c76f-109">返回值</span><span class="sxs-lookup"><span data-stu-id="6c76f-109">Return Value</span></span>  

 <span data-ttu-id="6c76f-110">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="6c76f-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="6c76f-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="6c76f-111">HRESULT</span></span>|<span data-ttu-id="6c76f-112">说明</span><span class="sxs-lookup"><span data-stu-id="6c76f-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6c76f-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c76f-113">S_OK</span></span>|<span data-ttu-id="6c76f-114">已成功执行比较。</span><span class="sxs-lookup"><span data-stu-id="6c76f-114">The comparison was successfully performed.</span></span>|  
|<span data-ttu-id="6c76f-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="6c76f-115">E_FAIL</span></span>|<span data-ttu-id="6c76f-116">无法执行比较。</span><span class="sxs-lookup"><span data-stu-id="6c76f-116">The comparison could not be performed.</span></span>|  
|<span data-ttu-id="6c76f-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="6c76f-117">E_INVALIDARG</span></span>|<span data-ttu-id="6c76f-118">`pFrameToCompare` 或 `pIsCloser` 为 null。</span><span class="sxs-lookup"><span data-stu-id="6c76f-118">`pFrameToCompare` or `pIsCloser` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6c76f-119">备注</span><span class="sxs-lookup"><span data-stu-id="6c76f-119">Remarks</span></span>  

 <span data-ttu-id="6c76f-120">`IsCloserToLeaf` 可用于实现将内部帧与堆栈上的其他帧交错的策略。</span><span class="sxs-lookup"><span data-stu-id="6c76f-120">`IsCloserToLeaf` can be used to implement a policy for interleaving internal frames with other frames on the stack.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6c76f-121">要求</span><span class="sxs-lookup"><span data-stu-id="6c76f-121">Requirements</span></span>  

 <span data-ttu-id="6c76f-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6c76f-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c76f-123">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6c76f-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6c76f-124">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6c76f-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6c76f-125">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c76f-125">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c76f-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="6c76f-126">See also</span></span>

- [<span data-ttu-id="6c76f-127">ICorDebugInternalFrame2 接口</span><span class="sxs-lookup"><span data-stu-id="6c76f-127">ICorDebugInternalFrame2 Interface</span></span>](icordebuginternalframe2-interface.md)
- [<span data-ttu-id="6c76f-128">调试接口</span><span class="sxs-lookup"><span data-stu-id="6c76f-128">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="6c76f-129">调试</span><span class="sxs-lookup"><span data-stu-id="6c76f-129">Debugging</span></span>](index.md)
