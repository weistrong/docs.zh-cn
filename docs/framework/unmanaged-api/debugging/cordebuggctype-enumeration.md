---
description: 了解详细信息： CorDebugGCType 枚举
title: CorDebugGCType 枚举
ms.date: 03/30/2017
api_name:
- CorDebugGCType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugGCType
helpviewer_keywords:
- CorDebugGCType enumeration [.NET Framework debugging]
ms.assetid: 880ca92a-42d4-42a5-9b9c-c2848eb39c6a
topic_type:
- apiref
ms.openlocfilehash: 4be835a9a028a882fa050991beb31d2a8dec5354
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801652"
---
# <a name="cordebuggctype-enumeration"></a><span data-ttu-id="742a2-103">CorDebugGCType 枚举</span><span class="sxs-lookup"><span data-stu-id="742a2-103">CorDebugGCType Enumeration</span></span>

<span data-ttu-id="742a2-104">指示垃圾回收器是在工作站还是服务器上运行。</span><span class="sxs-lookup"><span data-stu-id="742a2-104">Indicates whether the garbage collector is running on a workstation or a server.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="742a2-105">语法</span><span class="sxs-lookup"><span data-stu-id="742a2-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugGCType {  
    CorDebugWorkstationGC  = 0,  
    CorDebugServerGC       = ( CorDebugWorkstationGC + 1 )  
} CorDebugGCType;  
```  
  
## <a name="parameters"></a><span data-ttu-id="742a2-106">参数</span><span class="sxs-lookup"><span data-stu-id="742a2-106">Parameters</span></span>  
  
## <a name="members"></a><span data-ttu-id="742a2-107">成员</span><span class="sxs-lookup"><span data-stu-id="742a2-107">Members</span></span>  
  
|<span data-ttu-id="742a2-108">成员名称</span><span class="sxs-lookup"><span data-stu-id="742a2-108">Member name</span></span>|<span data-ttu-id="742a2-109">描述</span><span class="sxs-lookup"><span data-stu-id="742a2-109">Description</span></span>|  
|-----------------|-----------------|  
|`CorDebugWorkstationGC`|<span data-ttu-id="742a2-110">垃圾回收器正在工作站上运行。</span><span class="sxs-lookup"><span data-stu-id="742a2-110">The garbage collector is running on a workstation.</span></span>|  
|`CorDebugServerGC`|<span data-ttu-id="742a2-111">垃圾回收器正在服务器上运行。</span><span class="sxs-lookup"><span data-stu-id="742a2-111">The garbage collector is running on a server.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="742a2-112">备注</span><span class="sxs-lookup"><span data-stu-id="742a2-112">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="742a2-113">要求</span><span class="sxs-lookup"><span data-stu-id="742a2-113">Requirements</span></span>  

 <span data-ttu-id="742a2-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="742a2-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="742a2-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="742a2-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="742a2-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="742a2-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="742a2-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="742a2-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="742a2-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="742a2-118">See also</span></span>

- [<span data-ttu-id="742a2-119">调试枚举</span><span class="sxs-lookup"><span data-stu-id="742a2-119">Debugging Enumerations</span></span>](debugging-enumerations.md)
