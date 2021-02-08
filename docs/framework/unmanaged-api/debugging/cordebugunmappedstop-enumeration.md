---
description: 了解详细信息： CorDebugUnmappedStop 枚举
title: CorDebugUnmappedStop 枚举
ms.date: 03/30/2017
api_name:
- CorDebugUnmappedStop
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugUnmappedStop
helpviewer_keywords:
- CorDebugUnmappedStop enumeration [.NET Framework debugging]
ms.assetid: a684f7d7-d0c2-4690-b721-639e613f11f8
topic_type:
- apiref
ms.openlocfilehash: 9c4f70c5de451689f98a1c08627fd6df5128fdbd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801522"
---
# <a name="cordebugunmappedstop-enumeration"></a><span data-ttu-id="3c7dc-103">CorDebugUnmappedStop 枚举</span><span class="sxs-lookup"><span data-stu-id="3c7dc-103">CorDebugUnmappedStop Enumeration</span></span>

<span data-ttu-id="3c7dc-104">指定未映射代码的类型，这些代码可以中断分档器代码执行。</span><span class="sxs-lookup"><span data-stu-id="3c7dc-104">Specifies the type of unmapped code that can trigger a halt in code execution by the stepper.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c7dc-105">语法</span><span class="sxs-lookup"><span data-stu-id="3c7dc-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugUnmappedStop {  
    STOP_NONE               = 0x0,  
    STOP_PROLOG             = 0x01,  
    STOP_EPILOG             = 0x02,  
    STOP_NO_MAPPING_INFO    = 0x04,  
    STOP_OTHER_UNMAPPED     = 0x08,  
    STOP_UNMANAGED          = 0x10,  
    STOP_ALL                = 0xffff,  
} CorDebugUnmappedStop;  
```  
  
## <a name="members"></a><span data-ttu-id="3c7dc-106">成员</span><span class="sxs-lookup"><span data-stu-id="3c7dc-106">Members</span></span>  
  
|<span data-ttu-id="3c7dc-107">成员</span><span class="sxs-lookup"><span data-stu-id="3c7dc-107">Member</span></span>|<span data-ttu-id="3c7dc-108">说明</span><span class="sxs-lookup"><span data-stu-id="3c7dc-108">Description</span></span>|  
|------------|-----------------|  
|`STOP_NONE`|<span data-ttu-id="3c7dc-109">请勿在任何类型的未映射代码中停止。</span><span class="sxs-lookup"><span data-stu-id="3c7dc-109">Do not stop in any type of unmapped code.</span></span>|  
|`STOP_PROLOG`|<span data-ttu-id="3c7dc-110">在 prolog 代码中停止。</span><span class="sxs-lookup"><span data-stu-id="3c7dc-110">Stop in prolog code.</span></span>|  
|`STOP_EPILOG`|<span data-ttu-id="3c7dc-111">在 epilog 代码中停止。</span><span class="sxs-lookup"><span data-stu-id="3c7dc-111">Stop in epilog code.</span></span>|  
|`STOP_NO_MAPPING_INFO`|<span data-ttu-id="3c7dc-112">在没有映射信息的代码中停止。</span><span class="sxs-lookup"><span data-stu-id="3c7dc-112">Stop in code that has no mapping information.</span></span>|  
|`STOP_OTHER_UNMAPPED`|<span data-ttu-id="3c7dc-113">在未映射的代码中停止，不适合 prolog、epilog、无映射-信息或非托管类别。</span><span class="sxs-lookup"><span data-stu-id="3c7dc-113">Stop in unmapped code that does not fit into the prolog, epilog, no-mapping-information, or unmanaged category.</span></span>|  
|`STOP_UNMANAGED`|<span data-ttu-id="3c7dc-114">在非托管代码中停止。</span><span class="sxs-lookup"><span data-stu-id="3c7dc-114">Stop in unmanaged code.</span></span> <span data-ttu-id="3c7dc-115">此值仅适用于互操作调试。</span><span class="sxs-lookup"><span data-stu-id="3c7dc-115">This value is valid only with interop debugging.</span></span>|  
|`STOP_ALL`|<span data-ttu-id="3c7dc-116">在所有类型的未映射代码中停止。</span><span class="sxs-lookup"><span data-stu-id="3c7dc-116">Stop in all types of unmapped code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3c7dc-117">备注</span><span class="sxs-lookup"><span data-stu-id="3c7dc-117">Remarks</span></span>  

 <span data-ttu-id="3c7dc-118">使用 [ICorDebugStepper：： SetUnmappedStopMask](icordebugstepper-setunmappedstopmask-method.md) 方法设置标志，这些标志指定分档器将停止的未映射代码。</span><span class="sxs-lookup"><span data-stu-id="3c7dc-118">Use the [ICorDebugStepper::SetUnmappedStopMask](icordebugstepper-setunmappedstopmask-method.md) method to set the flags that specify the unmapped code in which the stepper will stop.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c7dc-119">要求</span><span class="sxs-lookup"><span data-stu-id="3c7dc-119">Requirements</span></span>  

 <span data-ttu-id="3c7dc-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3c7dc-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c7dc-121">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3c7dc-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3c7dc-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3c7dc-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3c7dc-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c7dc-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c7dc-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="3c7dc-124">See also</span></span>

- [<span data-ttu-id="3c7dc-125">调试枚举</span><span class="sxs-lookup"><span data-stu-id="3c7dc-125">Debugging Enumerations</span></span>](debugging-enumerations.md)
