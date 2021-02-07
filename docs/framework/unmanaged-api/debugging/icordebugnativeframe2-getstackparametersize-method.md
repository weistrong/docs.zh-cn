---
description: 了解详细信息： ICorDebugNativeFrame2：： GetStackParameterSize 方法
title: ICorDebugNativeFrame2::GetStackParameterSize 方法
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame2.GetStackParameterSize Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame2::GetStackParameterSize
helpviewer_keywords:
- ICorDebugNativeFrame2::GetStackParameterSize method [.NET Framework debugging]
- GetStackParameterSize method [.NET Framework debugging]
ms.assetid: f6a449c8-a941-43ba-9a90-c98b29ae3c36
topic_type:
- apiref
ms.openlocfilehash: 08a17ced0be75737c1c49aa3f9bb42b13bbe8aa0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722303"
---
# <a name="icordebugnativeframe2getstackparametersize-method"></a><span data-ttu-id="f1d29-103">ICorDebugNativeFrame2::GetStackParameterSize 方法</span><span class="sxs-lookup"><span data-stu-id="f1d29-103">ICorDebugNativeFrame2::GetStackParameterSize Method</span></span>

<span data-ttu-id="f1d29-104">返回 x86 操作系统上堆栈上的参数的累积大小。</span><span class="sxs-lookup"><span data-stu-id="f1d29-104">Returns the cumulative size of the parameters on the stack on x86 operating systems.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1d29-105">语法</span><span class="sxs-lookup"><span data-stu-id="f1d29-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStackParameterSize([out] ULONG32 * pSize)  
```  
  
## <a name="parameters"></a><span data-ttu-id="f1d29-106">参数</span><span class="sxs-lookup"><span data-stu-id="f1d29-106">Parameters</span></span>  

 `pSize`  
 <span data-ttu-id="f1d29-107">弄指向堆栈上参数的累计大小的指针。</span><span class="sxs-lookup"><span data-stu-id="f1d29-107">[out] A pointer to the cumulative size of the parameters on the stack.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f1d29-108">返回值</span><span class="sxs-lookup"><span data-stu-id="f1d29-108">Return Value</span></span>  

 <span data-ttu-id="f1d29-109">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="f1d29-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="f1d29-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f1d29-110">HRESULT</span></span>|<span data-ttu-id="f1d29-111">说明</span><span class="sxs-lookup"><span data-stu-id="f1d29-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f1d29-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1d29-112">S_OK</span></span>|<span data-ttu-id="f1d29-113">堆栈大小已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f1d29-113">The stack size was successfully returned.</span></span>|  
|<span data-ttu-id="f1d29-114">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="f1d29-114">S_FALSE</span></span>|<span data-ttu-id="f1d29-115">`GetStackParameterSize` 在非 x86 平台上调用了。</span><span class="sxs-lookup"><span data-stu-id="f1d29-115">`GetStackParameterSize` was called on a non-x86 platform.</span></span>|  
|<span data-ttu-id="f1d29-116">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f1d29-116">E_FAIL</span></span>|<span data-ttu-id="f1d29-117">`The size of the parameters could not be returned`.</span><span class="sxs-lookup"><span data-stu-id="f1d29-117">`The size of the parameters could not be returned`.</span></span>|  
|<span data-ttu-id="f1d29-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f1d29-118">E_INVALIDARG</span></span>|<span data-ttu-id="f1d29-119">`pSize` 为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="f1d29-119">`pSize` Is `null`.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="f1d29-120">例外</span><span class="sxs-lookup"><span data-stu-id="f1d29-120">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f1d29-121">备注</span><span class="sxs-lookup"><span data-stu-id="f1d29-121">Remarks</span></span>  

 <span data-ttu-id="f1d29-122">[ICorDebugStackWalk](icordebugstackwalk-interface.md)方法不调整推送到堆栈上的参数的堆栈指针。</span><span class="sxs-lookup"><span data-stu-id="f1d29-122">The [ICorDebugStackWalk](icordebugstackwalk-interface.md) methods do not adjust the stack pointer for parameters that are pushed on the stack.</span></span> <span data-ttu-id="f1d29-123">相反，你可以使用返回的值 `GetStackParameterSize` 调整堆栈指针，使其成为本机展开器的种子，这会调整参数。</span><span class="sxs-lookup"><span data-stu-id="f1d29-123">Instead, you can use the value returned by `GetStackParameterSize` to adjust the stack pointer to seed a native unwinder, which does adjust for the parameters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f1d29-124">要求</span><span class="sxs-lookup"><span data-stu-id="f1d29-124">Requirements</span></span>  

 <span data-ttu-id="f1d29-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f1d29-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f1d29-126">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f1d29-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f1d29-127">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f1d29-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f1d29-128">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f1d29-128">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1d29-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="f1d29-129">See also</span></span>

- [<span data-ttu-id="f1d29-130">ICorDebugNativeFrame2 接口</span><span class="sxs-lookup"><span data-stu-id="f1d29-130">ICorDebugNativeFrame2 Interface</span></span>](icordebugnativeframe2-interface.md)
- [<span data-ttu-id="f1d29-131">调试接口</span><span class="sxs-lookup"><span data-stu-id="f1d29-131">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="f1d29-132">调试</span><span class="sxs-lookup"><span data-stu-id="f1d29-132">Debugging</span></span>](index.md)
