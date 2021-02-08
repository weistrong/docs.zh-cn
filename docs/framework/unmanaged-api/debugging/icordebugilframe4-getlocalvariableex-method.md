---
description: 了解详细信息： ICorDebugILFrame4：： GetLocalVariableEx 方法
title: ICorDebugILFrame4::GetLocalVariableEx 方法
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugILFrame4.GetCodeEx
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 0c8676f8-ca0d-4998-b64d-fefac7e38912
topic_type:
- apiref
ms.openlocfilehash: 4eb6b3abbaf05c0373a487d9bd9d575b58a9af49
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791213"
---
# <a name="icordebugilframe4getlocalvariableex-method"></a><span data-ttu-id="97391-103">ICorDebugILFrame4::GetLocalVariableEx 方法</span><span class="sxs-lookup"><span data-stu-id="97391-103">ICorDebugILFrame4::GetLocalVariableEx Method</span></span>

<span data-ttu-id="97391-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="97391-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="97391-105">获取此中间语言 (IL) 堆栈帧中指定的局部变量的值，并且（可选）访问在探查器 ReJIT 检测中添加的变量。</span><span class="sxs-lookup"><span data-stu-id="97391-105">Gets the value of the specified local variable in this intermediate language (IL) stack frame, and optionally accesses a variable added in profiler ReJIT instrumentation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97391-106">语法</span><span class="sxs-lookup"><span data-stu-id="97391-106">Syntax</span></span>  
  
```cpp
HRESULT GetLocalVariableEx(  
   [in] ILCodeKind flags,
   [in] DWORD dwIndex,
   [out] ICorDebugValue **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="97391-107">参数</span><span class="sxs-lookup"><span data-stu-id="97391-107">Parameters</span></span>  

 `flags`  
 <span data-ttu-id="97391-108">中一个 [ILCodeKind](ilcodekind-enumeration.md) 枚举成员，用于指定在探查器 ReJIT 检测中添加的变量是否包含在帧中。</span><span class="sxs-lookup"><span data-stu-id="97391-108">[in] An [ILCodeKind](ilcodekind-enumeration.md) enumeration member that specifies whether a variable added in profiler ReJIT instrumentation is included in the frame.</span></span>  
  
 `dwIndex`  
 <span data-ttu-id="97391-109">[in] IL 堆栈帧中局部变量的索引。</span><span class="sxs-lookup"><span data-stu-id="97391-109">[in] The index of the local variable in the IL stack frame.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="97391-110">弄指向表示检索到的值的 "ICorDebugValue" 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="97391-110">[out] A pointer to the address of an "ICorDebugValue" object that represents the retrieved value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="97391-111">备注</span><span class="sxs-lookup"><span data-stu-id="97391-111">Remarks</span></span>  

 <span data-ttu-id="97391-112">此方法类似于 [GetLocalVariable](icordebugilframe-getlocalvariable-method.md) 方法，不同之处在于它还可以访问在探查器 ReJIT 检测中添加的变量。</span><span class="sxs-lookup"><span data-stu-id="97391-112">This method is similar to the [GetLocalVariable](icordebugilframe-getlocalvariable-method.md) method, except that it optionally accesses a variable added in profiler ReJIT instrumentation.</span></span> <span data-ttu-id="97391-113">使用的值调用此方法 `flags` `ILCODE_ORIGINAL_IL` 等效于调用 [GetLocalVariable](icordebugilframe-getlocalvariable-method.md); 如果使用附加的局部变量检测方法，则不能访问这些变量。</span><span class="sxs-lookup"><span data-stu-id="97391-113">Calling this method with a `flags` value of `ILCODE_ORIGINAL_IL` is equivalent to calling [GetLocalVariable](icordebugilframe-getlocalvariable-method.md); if the method is instrumented with additional local variables, those variables cannot be accessed.</span></span> <span data-ttu-id="97391-114">`ILCODE_REJIT_IL` 使调试器能够访问在探查器 ReJIT 检测中添加的局部变量。</span><span class="sxs-lookup"><span data-stu-id="97391-114">`ILCODE_REJIT_IL` allows the debugger to access the local variables added in profiler ReJIT instrumentation.</span></span> <span data-ttu-id="97391-115">如果未检测到 IL，则此方法将返回 `E_INVALIDARG`。</span><span class="sxs-lookup"><span data-stu-id="97391-115">If the IL is not instrumented, the method returns `E_INVALIDARG`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="97391-116">要求</span><span class="sxs-lookup"><span data-stu-id="97391-116">Requirements</span></span>  

 <span data-ttu-id="97391-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="97391-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="97391-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="97391-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="97391-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="97391-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="97391-120">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="97391-120">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97391-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="97391-121">See also</span></span>

- [<span data-ttu-id="97391-122">ICorDebugILFrame4 接口</span><span class="sxs-lookup"><span data-stu-id="97391-122">ICorDebugILFrame4 Interface</span></span>](icordebugilframe4-interface.md)
- [<span data-ttu-id="97391-123">调试接口</span><span class="sxs-lookup"><span data-stu-id="97391-123">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="97391-124">ReJIT： How-To 指南</span><span class="sxs-lookup"><span data-stu-id="97391-124">ReJIT: A How-To Guide</span></span>](/archive/blogs/davbr/rejit-a-how-to-guide)
