---
description: 了解详细信息： ICorDebugILFrame4：： EnumerateLocalVariablesEx 方法
title: ICorDebugILFrame4::EnumerateLocalVariablesEx 方法
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugILFrame4.EnumerateLocalVariablesEx
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 6f60aae6-70ec-4c4c-963a-138df98c4668
topic_type:
- apiref
ms.openlocfilehash: 8808b1ac337304ab37a35f7733b317dad274d48e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791239"
---
# <a name="icordebugilframe4enumeratelocalvariablesex-method"></a><span data-ttu-id="b526b-103">ICorDebugILFrame4::EnumerateLocalVariablesEx 方法</span><span class="sxs-lookup"><span data-stu-id="b526b-103">ICorDebugILFrame4::EnumerateLocalVariablesEx Method</span></span>

<span data-ttu-id="b526b-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="b526b-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="b526b-105">获取帧中局部变量的枚举，并且（可选）包括在探查器 ReJIT 检测中添加的变量。</span><span class="sxs-lookup"><span data-stu-id="b526b-105">Gets an enumerator for the local variable in the frame, and optionally includes variables added in profiler ReJIT instrumentation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b526b-106">语法</span><span class="sxs-lookup"><span data-stu-id="b526b-106">Syntax</span></span>  
  
```cpp
HRESULT EnumerateLocalVariablesEx(  
   [in] ILCodeKind flags,
   [out] ICorDebugValueEnum **ppValueEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b526b-107">参数</span><span class="sxs-lookup"><span data-stu-id="b526b-107">Parameters</span></span>  

 `flags`  
 <span data-ttu-id="b526b-108">中一个 [ILCodeKind](ilcodekind-enumeration.md) 枚举成员，用于指定在探查器 ReJIT 检测中添加的变量是否包含在帧中。</span><span class="sxs-lookup"><span data-stu-id="b526b-108">[in] An [ILCodeKind](ilcodekind-enumeration.md) enumeration member that specifies whether variables added in profiler ReJIT instrumentation are included in the frame.</span></span>  
  
 `ppValueEnum`  
 <span data-ttu-id="b526b-109">弄一个指向 "ICorDebugValueEnum" 对象地址的指针，该对象是此帧中局部变量的枚举器。</span><span class="sxs-lookup"><span data-stu-id="b526b-109">[out] A pointer to the address of an "ICorDebugValueEnum" object that is the enumerator for the local variables in this frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b526b-110">备注</span><span class="sxs-lookup"><span data-stu-id="b526b-110">Remarks</span></span>  

 <span data-ttu-id="b526b-111">此方法类似于 [EnumerateLocalVariables](icordebugilframe-enumeratelocalvariables-method.md) 方法，不同之处在于它可以访问在探查器 ReJIT 检测中添加的变量。</span><span class="sxs-lookup"><span data-stu-id="b526b-111">This method is similar to the [EnumerateLocalVariables](icordebugilframe-enumeratelocalvariables-method.md) method, except that it optionally accesses variables added in profiler ReJIT instrumentation.</span></span> <span data-ttu-id="b526b-112">将设置 `flags` 为 `ILCODE_ORIGINAL_IL` 等效于调用 [ICorDebugILFrame：： EnumerateLocalVariables](icordebugilframe-enumeratelocalvariables-method.md)。</span><span class="sxs-lookup"><span data-stu-id="b526b-112">Setting `flags` to `ILCODE_ORIGINAL_IL` is equivalent to calling [ICorDebugILFrame::EnumerateLocalVariables](icordebugilframe-enumeratelocalvariables-method.md).</span></span> <span data-ttu-id="b526b-113">将 `flags` 设置为 `ILCODE_REJIT_IL` 使调试器能够访问在探查器 ReJIT 检测中添加的局部变量。</span><span class="sxs-lookup"><span data-stu-id="b526b-113">Setting `flags` to `ILCODE_REJIT_IL` allows the debugger to access the local variables added in profiler ReJIT instrumentation.</span></span> <span data-ttu-id="b526b-114">如果未检测到中间语言 (IL)，则枚举为空且该方法将返回 `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="b526b-114">If the intermediate language (IL) is not instrumented, the enumeration is empty and the method returns `S_OK`.</span></span>  
  
 <span data-ttu-id="b526b-115">由于某些局部变量可能未处于活动状态，因此枚举器可能不包括正在运行的方法中的所有局部变量。</span><span class="sxs-lookup"><span data-stu-id="b526b-115">The enumerator may not include all of the local variables in the running method, since some of them may not be active.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b526b-116">要求</span><span class="sxs-lookup"><span data-stu-id="b526b-116">Requirements</span></span>  

 <span data-ttu-id="b526b-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b526b-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b526b-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b526b-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b526b-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b526b-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b526b-120">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b526b-120">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b526b-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="b526b-121">See also</span></span>

- [<span data-ttu-id="b526b-122">ICorDebugILFrame4 接口</span><span class="sxs-lookup"><span data-stu-id="b526b-122">ICorDebugILFrame4 Interface</span></span>](icordebugilframe4-interface.md)
- [<span data-ttu-id="b526b-123">调试接口</span><span class="sxs-lookup"><span data-stu-id="b526b-123">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="b526b-124">ReJIT： How-To 指南</span><span class="sxs-lookup"><span data-stu-id="b526b-124">ReJIT: A How-To Guide</span></span>](/archive/blogs/davbr/rejit-a-how-to-guide)
