---
description: 了解详细信息： ICorDebugNativeFrame2：： IsChild 方法
title: ICorDebugNativeFrame2::IsChild 方法
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame2.IsChild Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame2::IsChild
helpviewer_keywords:
- IsChild method [.NET Framework debugging]
- ICorDebugNativeFrame2::IsChild method [.NET Framework debugging]
ms.assetid: 9e2aae09-49cb-4fbd-81e5-e29cd864a88b
topic_type:
- apiref
ms.openlocfilehash: 7c698c5a49ee445b4ba9c591c96f700f86a86c32
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722290"
---
# <a name="icordebugnativeframe2ischild-method"></a><span data-ttu-id="0d038-103">ICorDebugNativeFrame2::IsChild 方法</span><span class="sxs-lookup"><span data-stu-id="0d038-103">ICorDebugNativeFrame2::IsChild Method</span></span>

<span data-ttu-id="0d038-104">确定当前帧是否为子框架。</span><span class="sxs-lookup"><span data-stu-id="0d038-104">Determines whether the current frame is a child frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0d038-105">语法</span><span class="sxs-lookup"><span data-stu-id="0d038-105">Syntax</span></span>  
  
```cpp  
HRESULT IsChild([out] BOOL * pIsChild);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0d038-106">参数</span><span class="sxs-lookup"><span data-stu-id="0d038-106">Parameters</span></span>  

 `pIsChild`  
 <span data-ttu-id="0d038-107">弄指定当前帧是否为子框架的布尔值。</span><span class="sxs-lookup"><span data-stu-id="0d038-107">[out] A Boolean value that specifies whether the current frame is a child frame.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0d038-108">返回值</span><span class="sxs-lookup"><span data-stu-id="0d038-108">Return Value</span></span>  

 <span data-ttu-id="0d038-109">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="0d038-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="0d038-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0d038-110">HRESULT</span></span>|<span data-ttu-id="0d038-111">说明</span><span class="sxs-lookup"><span data-stu-id="0d038-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0d038-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d038-112">S_OK</span></span>|<span data-ttu-id="0d038-113">已成功返回子状态。</span><span class="sxs-lookup"><span data-stu-id="0d038-113">The child status was successfully returned.</span></span>|  
|<span data-ttu-id="0d038-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0d038-114">E_FAIL</span></span>|<span data-ttu-id="0d038-115">无法返回子状态。</span><span class="sxs-lookup"><span data-stu-id="0d038-115">The child status could not be returned.</span></span>|  
|<span data-ttu-id="0d038-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0d038-116">E_INVALIDARG</span></span>|<span data-ttu-id="0d038-117">`pIsChild` 为 null。</span><span class="sxs-lookup"><span data-stu-id="0d038-117">`pIsChild` is null.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="0d038-118">例外</span><span class="sxs-lookup"><span data-stu-id="0d038-118">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0d038-119">备注</span><span class="sxs-lookup"><span data-stu-id="0d038-119">Remarks</span></span>  

 <span data-ttu-id="0d038-120">`IsChild` `true` 如果调用方法的帧对象是另一帧的子对象，则该方法返回。</span><span class="sxs-lookup"><span data-stu-id="0d038-120">The `IsChild` method returns `true` if the frame object on which you call the method is a child of another frame.</span></span> <span data-ttu-id="0d038-121">如果是这种情况，请使用 [IsMatchingParentFrame](icordebugnativeframe2-ismatchingparentframe-method.md) 方法检查帧是否为其父级。</span><span class="sxs-lookup"><span data-stu-id="0d038-121">If this is the case, use the [IsMatchingParentFrame](icordebugnativeframe2-ismatchingparentframe-method.md) method to check whether a frame is its parent.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0d038-122">要求</span><span class="sxs-lookup"><span data-stu-id="0d038-122">Requirements</span></span>  

 <span data-ttu-id="0d038-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0d038-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0d038-124">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0d038-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0d038-125">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0d038-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0d038-126">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0d038-126">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d038-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="0d038-127">See also</span></span>

- [<span data-ttu-id="0d038-128">ICorDebugNativeFrame2 接口</span><span class="sxs-lookup"><span data-stu-id="0d038-128">ICorDebugNativeFrame2 Interface</span></span>](icordebugnativeframe2-interface.md)
- [<span data-ttu-id="0d038-129">调试接口</span><span class="sxs-lookup"><span data-stu-id="0d038-129">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="0d038-130">调试</span><span class="sxs-lookup"><span data-stu-id="0d038-130">Debugging</span></span>](index.md)
