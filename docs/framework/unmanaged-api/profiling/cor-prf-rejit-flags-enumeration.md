---
description: 了解详细信息： COR_PRF_REJIT_FLAGS 枚举
title: COR_PRF_REJIT_FLAGS 枚举
ms.date: 08/06/2019
api_name:
- COR_PRF_REJIT_FLAGS Enumeration
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_REJIT_FLAGS
helpviewer_keywords:
- COR_PRF_REJIT_FLAGS enumeration [.NET Framework profiling]
topic_type:
- apiref
author: davmason
ms.author: davmason
ms.openlocfilehash: aad66285e9b31558a68b8ccdfc71f103d1772946
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102106912"
---
# <a name="cor_prf_rejit_flags-enumeration"></a><span data-ttu-id="8ee43-103">COR_PRF_REJIT_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="8ee43-103">COR_PRF_REJIT_FLAGS Enumeration</span></span>

<span data-ttu-id="8ee43-104">包含指示 [ICorProfilerInfo10：： RequestReJITWithInliners](icorprofilerinfo10-requestrejitwithinliners-method.md) API 应如何运行的值。</span><span class="sxs-lookup"><span data-stu-id="8ee43-104">Contains values that indicate how the [ICorProfilerInfo10::RequestReJITWithInliners](icorprofilerinfo10-requestrejitwithinliners-method.md) API should behave.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ee43-105">语法</span><span class="sxs-lookup"><span data-stu-id="8ee43-105">Syntax</span></span>  
  
```cpp  
typedef enum  
{
    COR_PRF_REJIT_BLOCK_INLINING = 0x1,
    COR_PRF_REJIT_INLINING_CALLBACKS    = 0x2
} COR_PRF_REJIT_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="8ee43-106">成员</span><span class="sxs-lookup"><span data-stu-id="8ee43-106">Members</span></span>  
  
|<span data-ttu-id="8ee43-107">成员</span><span class="sxs-lookup"><span data-stu-id="8ee43-107">Member</span></span>|<span data-ttu-id="8ee43-108">说明</span><span class="sxs-lookup"><span data-stu-id="8ee43-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_REJIT_BLOCK_INLINING`| <span data-ttu-id="8ee43-109">将阻止在其他方法中内联 ReJITted 方法。</span><span class="sxs-lookup"><span data-stu-id="8ee43-109">ReJITted methods will be blocked from being inlined in other methods.</span></span> |  
|`COR_PRF_REJIT_INLINING_CALLBACKS`| <span data-ttu-id="8ee43-110">`GetFunctionParameters`为内联方法请求 ReJITted 的任何方法接收回调。</span><span class="sxs-lookup"><span data-stu-id="8ee43-110">Receive `GetFunctionParameters` callbacks for any methods that inline the methods requested to be ReJITted.</span></span> |  

## <a name="requirements"></a><span data-ttu-id="8ee43-111">要求</span><span class="sxs-lookup"><span data-stu-id="8ee43-111">Requirements</span></span>  

 <span data-ttu-id="8ee43-112">**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="8ee43-112">**Platforms:** See [.NET Core supported operating systems](../../../core/install/windows.md?pivots=os-windows).</span></span>  
  
 <span data-ttu-id="8ee43-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8ee43-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8ee43-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8ee43-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8ee43-115">**.NET Framework 版本：**[!INCLUDE[net_core_30](../../../../includes/net-core-30-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ee43-115">**.NET Framework Versions:** [!INCLUDE[net_core_30](../../../../includes/net-core-30-md.md)]</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8ee43-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8ee43-116">See also</span></span>

- [<span data-ttu-id="8ee43-117">分析枚举</span><span class="sxs-lookup"><span data-stu-id="8ee43-117">Profiling Enumerations</span></span>](profiling-enumerations.md)
