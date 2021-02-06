---
description: 了解详细信息： ICorDebugHeapValue2 接口
title: ICorDebugHeapValue2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue2
helpviewer_keywords:
- ICorDebugHeapValue2 interface [.NET Framework debugging]
ms.assetid: 87360a52-90b1-4ada-80c0-589a556116d8
topic_type:
- apiref
ms.openlocfilehash: 04c757540a11a74db0a9bdf7f638786af46055c7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660747"
---
# <a name="icordebugheapvalue2-interface"></a><span data-ttu-id="45fae-103">ICorDebugHeapValue2 接口</span><span class="sxs-lookup"><span data-stu-id="45fae-103">ICorDebugHeapValue2 Interface</span></span>

<span data-ttu-id="45fae-104">ICorDebugHeapValue 的扩展，它为公共语言运行时 (CLR) 句柄提供支持。</span><span class="sxs-lookup"><span data-stu-id="45fae-104">An extension of ICorDebugHeapValue that provides support for common language runtime (CLR) handles.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="45fae-105">方法</span><span class="sxs-lookup"><span data-stu-id="45fae-105">Methods</span></span>  
  
|<span data-ttu-id="45fae-106">方法</span><span class="sxs-lookup"><span data-stu-id="45fae-106">Method</span></span>|<span data-ttu-id="45fae-107">说明</span><span class="sxs-lookup"><span data-stu-id="45fae-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="45fae-108">CreateHandle 方法</span><span class="sxs-lookup"><span data-stu-id="45fae-108">CreateHandle Method</span></span>](icordebugheapvalue2-createhandle-method.md)|<span data-ttu-id="45fae-109">为此对象创建指定类型的句柄 `ICorDebugHeapValue2` 。</span><span class="sxs-lookup"><span data-stu-id="45fae-109">Creates a handle of the specified type for this `ICorDebugHeapValue2` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="45fae-110">备注</span><span class="sxs-lookup"><span data-stu-id="45fae-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="45fae-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="45fae-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="45fae-112">要求</span><span class="sxs-lookup"><span data-stu-id="45fae-112">Requirements</span></span>  

 <span data-ttu-id="45fae-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="45fae-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="45fae-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="45fae-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="45fae-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="45fae-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="45fae-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="45fae-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="45fae-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="45fae-117">See also</span></span>

- [<span data-ttu-id="45fae-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="45fae-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
