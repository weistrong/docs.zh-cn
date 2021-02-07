---
description: 了解详细信息： ICorDebugNativeFrame2：： IsMatchingParentFrame 方法
title: ICorDebugNativeFrame2::IsMatchingParentFrame 方法
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame2.IsMatchingParentFrame Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame2::IsMatchingParentFrame
helpviewer_keywords:
- IsMatchingParentFrame method [.NET Framework debugging]
- ICorDebugNativeFrame2::IsMatchingParentFrame method [.NET Framework debugging]
ms.assetid: d2ca20db-df22-4528-a0dd-a09ea62c8998
topic_type:
- apiref
ms.openlocfilehash: 6dff1cb7f5205ad742ac4b886f72938dd28bd88f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722199"
---
# <a name="icordebugnativeframe2ismatchingparentframe-method"></a><span data-ttu-id="ca090-103">ICorDebugNativeFrame2::IsMatchingParentFrame 方法</span><span class="sxs-lookup"><span data-stu-id="ca090-103">ICorDebugNativeFrame2::IsMatchingParentFrame Method</span></span>

<span data-ttu-id="ca090-104">确定指定的帧是否为当前帧的父级。</span><span class="sxs-lookup"><span data-stu-id="ca090-104">Determines whether the specified frame is the parent of the current frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca090-105">语法</span><span class="sxs-lookup"><span data-stu-id="ca090-105">Syntax</span></span>  
  
```cpp  
HRESULT IsMatchingParentFrame([in] ICorDebugNativeFrame2  
                                      *pPotentialParentFrame,  
                              [out] BOOL *pIsParent);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ca090-106">参数</span><span class="sxs-lookup"><span data-stu-id="ca090-106">Parameters</span></span>  

 `pPotentialParentFrame`  
 <span data-ttu-id="ca090-107">中一个指针，指向要为父状态计算的帧对象。</span><span class="sxs-lookup"><span data-stu-id="ca090-107">[in] A pointer to the frame object that you want to evaluate for parent status.</span></span>  
  
 `pIsParent`  
 <span data-ttu-id="ca090-108">[out] `true` 如果 `pPotentialParentFrame` 为当前帧的父级，则为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="ca090-108">[out] `true` if `pPotentialParentFrame` is the current frame’s parent; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ca090-109">返回值</span><span class="sxs-lookup"><span data-stu-id="ca090-109">Return Value</span></span>  

 <span data-ttu-id="ca090-110">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="ca090-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="ca090-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ca090-111">HRESULT</span></span>|<span data-ttu-id="ca090-112">说明</span><span class="sxs-lookup"><span data-stu-id="ca090-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ca090-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca090-113">S_OK</span></span>|<span data-ttu-id="ca090-114">父状态已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ca090-114">The parent status was successfully returned.</span></span>|  
|<span data-ttu-id="ca090-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ca090-115">E_FAIL</span></span>|<span data-ttu-id="ca090-116">无法返回父状态。</span><span class="sxs-lookup"><span data-stu-id="ca090-116">The parent status could not be returned.</span></span>|  
|<span data-ttu-id="ca090-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ca090-117">E_INVALIDARG</span></span>|<span data-ttu-id="ca090-118">`pPotentialParentFrame` 或 `pIsParent` 为 null。</span><span class="sxs-lookup"><span data-stu-id="ca090-118">`pPotentialParentFrame` or `pIsParent` is null.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="ca090-119">例外</span><span class="sxs-lookup"><span data-stu-id="ca090-119">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ca090-120">备注</span><span class="sxs-lookup"><span data-stu-id="ca090-120">Remarks</span></span>  

 <span data-ttu-id="ca090-121">`IsMatchingParentFrame``true`如果传递给方法的帧对象是在其上调用方法的 frame 对象的父对象，则返回。</span><span class="sxs-lookup"><span data-stu-id="ca090-121">`IsMatchingParentFrame` returns `true` if the frame object you pass to the method is the parent of the frame object on which the method was called.</span></span> <span data-ttu-id="ca090-122">如果在不是指定帧的子级的帧上调用方法，则会返回错误。</span><span class="sxs-lookup"><span data-stu-id="ca090-122">If you call the method on a frame that is not a child of the specified frame, it returns an error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca090-123">要求</span><span class="sxs-lookup"><span data-stu-id="ca090-123">Requirements</span></span>  

 <span data-ttu-id="ca090-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ca090-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca090-125">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ca090-125">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ca090-126">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ca090-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ca090-127">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca090-127">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca090-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="ca090-128">See also</span></span>

- [<span data-ttu-id="ca090-129">ICorDebugNativeFrame2 接口</span><span class="sxs-lookup"><span data-stu-id="ca090-129">ICorDebugNativeFrame2 Interface</span></span>](icordebugnativeframe2-interface.md)
- [<span data-ttu-id="ca090-130">调试接口</span><span class="sxs-lookup"><span data-stu-id="ca090-130">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="ca090-131">调试</span><span class="sxs-lookup"><span data-stu-id="ca090-131">Debugging</span></span>](index.md)
