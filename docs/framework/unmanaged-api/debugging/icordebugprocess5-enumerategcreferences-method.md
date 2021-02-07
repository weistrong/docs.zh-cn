---
description: 了解详细信息： ICorDebugProcess5：： EnumerateGCReferences 方法
title: ICorDebugProcess5::EnumerateGCReferences 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.EnumerateGCReferences
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::EnumerateGCReferences
helpviewer_keywords:
- EnumerateGCReferences method, ICorDebugProcess5 interface [.NET Framework debugging]
- ICorDebugProcess5::EnumerateGCReferences method [.NET Framework debugging]
ms.assetid: 86c397c3-81d8-463e-a248-3cbe06c44d9d
topic_type:
- apiref
ms.openlocfilehash: 5145fd072b083ed107b874fe99403984915233ec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746407"
---
# <a name="icordebugprocess5enumerategcreferences-method"></a><span data-ttu-id="1baaa-103">ICorDebugProcess5::EnumerateGCReferences 方法</span><span class="sxs-lookup"><span data-stu-id="1baaa-103">ICorDebugProcess5::EnumerateGCReferences Method</span></span>

<span data-ttu-id="1baaa-104">获取一个枚举器，该枚举器用于进程中要进行垃圾回收的所有对象。</span><span class="sxs-lookup"><span data-stu-id="1baaa-104">Gets an enumerator for all objects that are to be garbage-collected in a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1baaa-105">语法</span><span class="sxs-lookup"><span data-stu-id="1baaa-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateGCReferences(  
    [in] Bool enumerateWeakReferences,
    [out] ICorDebugGCReferenceEnum **ppEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1baaa-106">参数</span><span class="sxs-lookup"><span data-stu-id="1baaa-106">Parameters</span></span>  

 `enumerateWeakReferences`  
 <span data-ttu-id="1baaa-107">中指示是否也要枚举弱引用的布尔值。</span><span class="sxs-lookup"><span data-stu-id="1baaa-107">[in] A Boolean value that indicates whether weak references are also to be enumerated.</span></span> <span data-ttu-id="1baaa-108">如果 `enumerateWeakReferences` 为 `true` ，则 `ppEnum` 枚举器将同时包含强引用和弱引用。</span><span class="sxs-lookup"><span data-stu-id="1baaa-108">If `enumerateWeakReferences` is `true`, the `ppEnum` enumerator includes both strong references and weak references.</span></span> <span data-ttu-id="1baaa-109">如果 `enumerateWeakReferences` 为 `false` ，则枚举器仅包括强引用。</span><span class="sxs-lookup"><span data-stu-id="1baaa-109">If `enumerateWeakReferences` is `false`, the enumerator includes only strong references.</span></span>  
  
 `ppEnum`  
 <span data-ttu-id="1baaa-110">弄一个指针，指向 [ICorDebugGCReferenceEnum](icordebuggcreferenceenum-interface.md) 的地址，该地址是要进行垃圾回收的对象的枚举器。</span><span class="sxs-lookup"><span data-stu-id="1baaa-110">[out] A pointer to the address of an [ICorDebugGCReferenceEnum](icordebuggcreferenceenum-interface.md) that is an enumerator for the objects to be garbage-collected.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1baaa-111">备注</span><span class="sxs-lookup"><span data-stu-id="1baaa-111">Remarks</span></span>  

 <span data-ttu-id="1baaa-112">此方法提供了一种方法，用于确定进程中任何托管对象的完整根链，并可用于确定对象仍处于活动状态的原因。</span><span class="sxs-lookup"><span data-stu-id="1baaa-112">This method provides a way to determine the full rooting chain for any managed object in a process and can be used to determine why an object is still alive.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1baaa-113">要求</span><span class="sxs-lookup"><span data-stu-id="1baaa-113">Requirements</span></span>  

 <span data-ttu-id="1baaa-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1baaa-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1baaa-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1baaa-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1baaa-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1baaa-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1baaa-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1baaa-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1baaa-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="1baaa-118">See also</span></span>

- [<span data-ttu-id="1baaa-119">ICorDebugProcess5 接口</span><span class="sxs-lookup"><span data-stu-id="1baaa-119">ICorDebugProcess5 Interface</span></span>](icordebugprocess5-interface.md)
- [<span data-ttu-id="1baaa-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="1baaa-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
