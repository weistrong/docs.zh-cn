---
description: 了解详细信息： ICorDebugExceptionObjectCallStackEnum：： Next 方法
title: ICorDebugExceptionObjectCallStackEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugExceptionObjectCallStackEnum::Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugExceptionObjectCallStackEnum::Next
helpviewer_keywords:
- ICorDebugExceptionObjectCallStackEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugExceptionObjectCallStackEnum interface [.NET Framework debugging]
ms.assetid: 3328a2c0-1e48-4a54-802a-9b474cf82c21
topic_type:
- apiref
ms.openlocfilehash: df68eb6e4794d294fc39dd943065582dc52a58a1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693312"
---
# <a name="icordebugexceptionobjectcallstackenumnext-method"></a><span data-ttu-id="4579f-103">ICorDebugExceptionObjectCallStackEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="4579f-103">ICorDebugExceptionObjectCallStackEnum::Next Method</span></span>

<span data-ttu-id="4579f-104">获取指定数量的 [CorDebugExceptionObjectStackFrame](cordebugexceptionobjectstackframe-structure.md) 实例，其中包含异常对象的调用堆栈中的信息。</span><span class="sxs-lookup"><span data-stu-id="4579f-104">Gets the specified number of [CorDebugExceptionObjectStackFrame](cordebugexceptionobjectstackframe-structure.md) instances that contain information from an exception object's call stack.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4579f-105">语法</span><span class="sxs-lookup"><span data-stu-id="4579f-105">Syntax</span></span>  
  
```cpp  
HRESULT Next(  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)] CorDebugExceptionObjectStackFrame values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4579f-106">参数</span><span class="sxs-lookup"><span data-stu-id="4579f-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="4579f-107">中要检索的 [CorDebugExceptionObjectStackFrame](cordebugexceptionobjectstackframe-structure.md) 实例的数目。</span><span class="sxs-lookup"><span data-stu-id="4579f-107">[in] The number of [CorDebugExceptionObjectStackFrame](cordebugexceptionobjectstackframe-structure.md) instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="4579f-108">弄指针的数组，其中每个指针指向一个 [CorDebugExceptionObjectStackFrame](cordebugexceptionobjectstackframe-structure.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="4579f-108">[out] An array of pointers, each of which points to a [CorDebugExceptionObjectStackFrame](cordebugexceptionobjectstackframe-structure.md) object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="4579f-109">弄一个指针，指向实际返回的 [CorDebugExceptionObjectStackFrame](cordebugexceptionobjectstackframe-structure.md) 实例的数目。</span><span class="sxs-lookup"><span data-stu-id="4579f-109">[out] A pointer to the number of [CorDebugExceptionObjectStackFrame](cordebugexceptionobjectstackframe-structure.md) instances actually returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4579f-110">备注</span><span class="sxs-lookup"><span data-stu-id="4579f-110">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4579f-111">要求</span><span class="sxs-lookup"><span data-stu-id="4579f-111">Requirements</span></span>  

 <span data-ttu-id="4579f-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4579f-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4579f-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4579f-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4579f-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4579f-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4579f-115">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4579f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4579f-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="4579f-116">See also</span></span>

- [<span data-ttu-id="4579f-117">ICorDebugExceptionObjectCallStackEnum 接口</span><span class="sxs-lookup"><span data-stu-id="4579f-117">ICorDebugExceptionObjectCallStackEnum Interface</span></span>](icordebugexceptionobjectcallstackenum-interface.md)
- [<span data-ttu-id="4579f-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="4579f-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
