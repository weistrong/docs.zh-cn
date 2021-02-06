---
description: 了解详细信息： ICorDebugProcess5：： GetGCHeapInformation 方法
title: ICorDebugProcess5::GetGCHeapInformation 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.GetGCHeapInformation
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::GetGCHeapInformation
helpviewer_keywords:
- ICorDebugProcess5::GetGCHeapInformation method [.NET Framework debugging]
- GetGCHeapInformation method, ICorDebugProcess5 interface [.NET Framework debugging]
ms.assetid: b9538ceb-230a-4079-9cb2-903dbf5c1848
topic_type:
- apiref
ms.openlocfilehash: e63f8871a2c18d6daf2dcf93b92e49123c56442f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649801"
---
# <a name="icordebugprocess5getgcheapinformation-method"></a><span data-ttu-id="8d810-103">ICorDebugProcess5::GetGCHeapInformation 方法</span><span class="sxs-lookup"><span data-stu-id="8d810-103">ICorDebugProcess5::GetGCHeapInformation Method</span></span>

<span data-ttu-id="8d810-104">提供有关垃圾回收堆的常规信息，包括当前是否可枚举。</span><span class="sxs-lookup"><span data-stu-id="8d810-104">Provides general information about the garbage collection heap, including whether it is currently enumerable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8d810-105">语法</span><span class="sxs-lookup"><span data-stu-id="8d810-105">Syntax</span></span>  
  
```cpp  
HRESULT GetGCHeapInformation(  
    [out] COR_HEAPINFO *pHeapInfo  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8d810-106">参数</span><span class="sxs-lookup"><span data-stu-id="8d810-106">Parameters</span></span>  

 `pHeapInfo`  
 <span data-ttu-id="8d810-107">弄一个指向 [COR_HEAPINFO](cor-heapinfo-structure.md) 值的指针，该值提供有关垃圾回收堆的常规信息。</span><span class="sxs-lookup"><span data-stu-id="8d810-107">[out] A pointer to a [COR_HEAPINFO](cor-heapinfo-structure.md) value that provides general information about the garbage collection heap.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8d810-108">备注</span><span class="sxs-lookup"><span data-stu-id="8d810-108">Remarks</span></span>  

 <span data-ttu-id="8d810-109">`ICorDebugProcess5::GetGCHeapInformation`必须先调用方法，然后才能枚举堆或单独的堆区域，以确保进程中的垃圾回收结构当前有效。</span><span class="sxs-lookup"><span data-stu-id="8d810-109">The `ICorDebugProcess5::GetGCHeapInformation` method must be called before enumerating the heap or individual heap regions to ensure that the garbage collection structures in the process are currently valid.</span></span> <span data-ttu-id="8d810-110">当集合正在进行时，无法遍历垃圾回收堆。</span><span class="sxs-lookup"><span data-stu-id="8d810-110">The garbage collection heap cannot be walked while a collection is in progress.</span></span> <span data-ttu-id="8d810-111">否则，枚举可能会捕获无效的垃圾回收结构。</span><span class="sxs-lookup"><span data-stu-id="8d810-111">Otherwise, the enumeration may capture garbage collection structures that are invalid.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8d810-112">要求</span><span class="sxs-lookup"><span data-stu-id="8d810-112">Requirements</span></span>  

 <span data-ttu-id="8d810-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8d810-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8d810-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8d810-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8d810-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8d810-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8d810-116">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8d810-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8d810-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="8d810-117">See also</span></span>

- [<span data-ttu-id="8d810-118">ICorDebugProcess5 接口</span><span class="sxs-lookup"><span data-stu-id="8d810-118">ICorDebugProcess5 Interface</span></span>](icordebugprocess5-interface.md)
- [<span data-ttu-id="8d810-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="8d810-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
