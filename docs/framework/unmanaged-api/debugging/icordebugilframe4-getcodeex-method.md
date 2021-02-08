---
description: 了解详细信息： ICorDebugILFrame4：： GetCodeEx 方法
title: ICorDebugILFrame4::GetCodeEx 方法
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugILFrame4.GetLocalVariableEx
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: aeda0e42-29ee-4ca8-9f21-ac4641677a62
topic_type:
- apiref
ms.openlocfilehash: 1d17dfa531354b8a4b0dd3c0d3d2eb47206900cc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791226"
---
# <a name="icordebugilframe4getcodeex-method"></a><span data-ttu-id="85d49-103">ICorDebugILFrame4::GetCodeEx 方法</span><span class="sxs-lookup"><span data-stu-id="85d49-103">ICorDebugILFrame4::GetCodeEx Method</span></span>

<span data-ttu-id="85d49-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="85d49-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="85d49-105">获取指向此堆栈帧正在执行的代码的指针。</span><span class="sxs-lookup"><span data-stu-id="85d49-105">Gets a pointer to the code that this stack frame is executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="85d49-106">语法</span><span class="sxs-lookup"><span data-stu-id="85d49-106">Syntax</span></span>  
  
```cpp
HRESULT GetCodeEx(  
   [in] ILCodeKind flags,
   [out] ICorDebugCode **ppCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="85d49-107">参数</span><span class="sxs-lookup"><span data-stu-id="85d49-107">Parameters</span></span>  

 `flags`  
 <span data-ttu-id="85d49-108">中一个 [ILCodeKind](ilcodekind-enumeration.md) 枚举成员，该成员指定由探查器的 ReJIT 请求定义的中间语言 (IL) 是否包含在帧中。</span><span class="sxs-lookup"><span data-stu-id="85d49-108">[in] An [ILCodeKind](ilcodekind-enumeration.md) enumeration member that specifies whether the intermediate language (IL) defined by the profiler's ReJIT request is included in the frame.</span></span>  
  
 `ppCode`  
 <span data-ttu-id="85d49-109">弄一个指向 "ICorDebugCode" 对象地址的指针，该对象表示此堆栈帧正在执行的代码。</span><span class="sxs-lookup"><span data-stu-id="85d49-109">[out] A pointer to the address of an "ICorDebugCode" object that represents the code that this stack frame is executing.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="85d49-110">备注</span><span class="sxs-lookup"><span data-stu-id="85d49-110">Remarks</span></span>  

 <span data-ttu-id="85d49-111">此方法类似于 [ICorDebugFrame：： GetCode](icordebugframe-getcode-method.md) 方法，不同之处在于它可以访问由探查器的 ReJIT 请求定义的代码。</span><span class="sxs-lookup"><span data-stu-id="85d49-111">This method is similar to the [ICorDebugFrame::GetCode](icordebugframe-getcode-method.md) method, except that it optionally accesses code defined by the profiler's ReJIT request.</span></span> <span data-ttu-id="85d49-112">使用的值调用此方法 `flags` `ILCODE_ORIGINAL_IL` 等效于调用 [GetCode](icordebugframe-getcode-method.md); 如果检测到此方法，则将无法访问其 IL。</span><span class="sxs-lookup"><span data-stu-id="85d49-112">Calling this method with a `flags` value of `ILCODE_ORIGINAL_IL` is equivalent to calling [GetCode](icordebugframe-getcode-method.md); if the method is instrumented, its IL will not be accessible.</span></span> <span data-ttu-id="85d49-113">`ILCODE_REJIT_IL` 允许调试器访问由探查器的 ReJIT 请求定义的 IL。</span><span class="sxs-lookup"><span data-stu-id="85d49-113">`ILCODE_REJIT_IL` allows the debugger to access the IL defined by the profiler's ReJIT request.</span></span> <span data-ttu-id="85d49-114">如果未检测到 IL， `ppCode` 则为 **null**，并且该方法将返回 `S_OK` 。</span><span class="sxs-lookup"><span data-stu-id="85d49-114">If the IL is not instrumented, `ppCode` is **null**, and the method returns `S_OK`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="85d49-115">要求</span><span class="sxs-lookup"><span data-stu-id="85d49-115">Requirements</span></span>  

 <span data-ttu-id="85d49-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="85d49-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="85d49-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="85d49-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="85d49-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="85d49-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="85d49-119">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="85d49-119">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="85d49-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="85d49-120">See also</span></span>

- [<span data-ttu-id="85d49-121">ICorDebugILFrame4 接口</span><span class="sxs-lookup"><span data-stu-id="85d49-121">ICorDebugILFrame4 Interface</span></span>](icordebugilframe4-interface.md)
- [<span data-ttu-id="85d49-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="85d49-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="85d49-123">ReJIT： How-To 指南</span><span class="sxs-lookup"><span data-stu-id="85d49-123">ReJIT: A How-To Guide</span></span>](/archive/blogs/davbr/rejit-a-how-to-guide)
