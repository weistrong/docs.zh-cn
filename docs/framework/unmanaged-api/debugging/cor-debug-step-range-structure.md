---
description: 了解详细信息： COR_DEBUG_STEP_RANGE 结构
title: COR_DEBUG_STEP_RANGE 结构
ms.date: 03/30/2017
api_name:
- COR_DEBUG_STEP_RANGE
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_DEBUG_STEP_RANGE
helpviewer_keywords:
- COR_DEBUG_STEP_RANGE structure [.NET Framework debugging]
ms.assetid: 8809d00e-beaa-4dcf-b4e8-e89d0a5406b7
topic_type:
- apiref
ms.openlocfilehash: 40462be4b165351b3265fa0833d19f18e0fa3a37
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801834"
---
# <a name="cor_debug_step_range-structure"></a><span data-ttu-id="043d3-103">COR_DEBUG_STEP_RANGE 结构</span><span class="sxs-lookup"><span data-stu-id="043d3-103">COR_DEBUG_STEP_RANGE Structure</span></span>

<span data-ttu-id="043d3-104">包含代码区域的偏离量信息。</span><span class="sxs-lookup"><span data-stu-id="043d3-104">Contains the offset information for a range of code.</span></span>  
  
 <span data-ttu-id="043d3-105">此结构由 [ICorDebugStepper：： StepRange](icordebugstepper-steprange-method.md) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="043d3-105">This structure is used by the [ICorDebugStepper::StepRange](icordebugstepper-steprange-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="043d3-106">语法</span><span class="sxs-lookup"><span data-stu-id="043d3-106">Syntax</span></span>  
  
```cpp  
typedef struct {  
    ULONG32 startOffset;  
    ULONG32 endOffset;  
} COR_DEBUG_STEP_RANGE;  
```  
  
## <a name="members"></a><span data-ttu-id="043d3-107">成员</span><span class="sxs-lookup"><span data-stu-id="043d3-107">Members</span></span>  
  
|<span data-ttu-id="043d3-108">成员</span><span class="sxs-lookup"><span data-stu-id="043d3-108">Member</span></span>|<span data-ttu-id="043d3-109">说明</span><span class="sxs-lookup"><span data-stu-id="043d3-109">Description</span></span>|  
|------------|-----------------|  
|`startOffset`|<span data-ttu-id="043d3-110">范围开始处的偏移量。</span><span class="sxs-lookup"><span data-stu-id="043d3-110">The offset of the beginning of the range.</span></span>|  
|`endOffset`|<span data-ttu-id="043d3-111">范围末尾的偏移量。</span><span class="sxs-lookup"><span data-stu-id="043d3-111">The offset of the end of the range.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="043d3-112">要求</span><span class="sxs-lookup"><span data-stu-id="043d3-112">Requirements</span></span>  

 <span data-ttu-id="043d3-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="043d3-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="043d3-114">**标头：** Cordebug.idl .idl</span><span class="sxs-lookup"><span data-stu-id="043d3-114">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="043d3-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="043d3-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="043d3-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="043d3-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="043d3-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="043d3-117">See also</span></span>

- [<span data-ttu-id="043d3-118">StepRange 方法</span><span class="sxs-lookup"><span data-stu-id="043d3-118">StepRange Method</span></span>](icordebugstepper-steprange-method.md)
- [<span data-ttu-id="043d3-119">调试结构</span><span class="sxs-lookup"><span data-stu-id="043d3-119">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="043d3-120">调试</span><span class="sxs-lookup"><span data-stu-id="043d3-120">Debugging</span></span>](index.md)
