---
description: 了解详细信息： CorDebugExceptionObjectStackFrame 结构
title: CorDebugExceptionObjectStackFrame 结构
ms.date: 03/30/2017
api_name:
- CorDebugExceptionObjectStackFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugExceptionObjectStackFrame
helpviewer_keywords:
- CorDebugExceptionObjectStackFrame structure [.NET Framework debugging]
ms.assetid: 542cdd81-5ae7-4361-b0ef-1ae4775df258
topic_type:
- apiref
ms.openlocfilehash: abeb5a9f6385c494745a34c6f37d6fbc1376ad7b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662151"
---
# <a name="cordebugexceptionobjectstackframe-structure"></a><span data-ttu-id="0f857-103">CorDebugExceptionObjectStackFrame 结构</span><span class="sxs-lookup"><span data-stu-id="0f857-103">CorDebugExceptionObjectStackFrame Structure</span></span>

<span data-ttu-id="0f857-104">表示异常对象中的堆栈帧信息。</span><span class="sxs-lookup"><span data-stu-id="0f857-104">Represents stack frame information from an exception object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f857-105">语法</span><span class="sxs-lookup"><span data-stu-id="0f857-105">Syntax</span></span>  
  
```cpp  
typedef struct CorDebugExceptionObjectStackFrame {  
    ICorDebugModule* pModule;  
    CORDB_ADDRESS ip;  
    mdMethodDef methodDef;  
    BOOL isLastForeignExceptionFrame;  
} CorDebugExceptionObjectStackFrame;  
```  
  
## <a name="members"></a><span data-ttu-id="0f857-106">成员</span><span class="sxs-lookup"><span data-stu-id="0f857-106">Members</span></span>  
  
|<span data-ttu-id="0f857-107">成员</span><span class="sxs-lookup"><span data-stu-id="0f857-107">Member</span></span>|<span data-ttu-id="0f857-108">说明</span><span class="sxs-lookup"><span data-stu-id="0f857-108">Description</span></span>|  
|------------|-----------------|  
|`pModule`|<span data-ttu-id="0f857-109">指向当前帧的 ICorDebugModule 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="0f857-109">A pointer to the ICorDebugModule object for the current frame.</span></span>|  
|`ip`|<span data-ttu-id="0f857-110">指令指针的值 (当前帧的 EIP/裂缝) 。</span><span class="sxs-lookup"><span data-stu-id="0f857-110">The value of the instruction pointer (EIP/RIP) for the current frame.</span></span>|  
|`methodDef`|<span data-ttu-id="0f857-111">当前帧的方法标记。</span><span class="sxs-lookup"><span data-stu-id="0f857-111">The method token for the current frame.</span></span>|  
|`isLastForeignExceptionFrame`|<span data-ttu-id="0f857-112">一个值，该值指示帧是否为外部异常中的最后一个帧。</span><span class="sxs-lookup"><span data-stu-id="0f857-112">A value that indicates whether the frame is the last frame in a foreign exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0f857-113">备注</span><span class="sxs-lookup"><span data-stu-id="0f857-113">Remarks</span></span>  

 <span data-ttu-id="0f857-114">当不再使用 ICorDebugModule 对象时，调用方必须释放指向该对象的指针。</span><span class="sxs-lookup"><span data-stu-id="0f857-114">The caller must release the pointer to the ICorDebugModule object once it is no longer in use.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f857-115">要求</span><span class="sxs-lookup"><span data-stu-id="0f857-115">Requirements</span></span>  

 <span data-ttu-id="0f857-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0f857-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f857-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0f857-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0f857-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0f857-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0f857-119">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0f857-119">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f857-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="0f857-120">See also</span></span>

- [<span data-ttu-id="0f857-121">调试结构</span><span class="sxs-lookup"><span data-stu-id="0f857-121">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="0f857-122">调试</span><span class="sxs-lookup"><span data-stu-id="0f857-122">Debugging</span></span>](index.md)
