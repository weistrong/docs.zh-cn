---
description: 了解详细信息： COR_PRF_MISC 枚举
title: COR_PRF_MISC 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_MISC
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_MISC
helpviewer_keywords:
- COR_PRF_MISC enumeration [.NET Framework profiling]
ms.assetid: 619bb5de-e309-48b6-a3af-32d935a0ff46
topic_type:
- apiref
ms.openlocfilehash: 037ea040dfdf9f5be48369ab4d8e94b12aea51ff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687592"
---
# <a name="cor_prf_misc-enumeration"></a><span data-ttu-id="dcc91-103">COR_PRF_MISC 枚举</span><span class="sxs-lookup"><span data-stu-id="dcc91-103">COR_PRF_MISC Enumeration</span></span>

<span data-ttu-id="dcc91-104">包含指定特殊标识符的常数值。</span><span class="sxs-lookup"><span data-stu-id="dcc91-104">Contains constant values that specify special identifiers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dcc91-105">语法</span><span class="sxs-lookup"><span data-stu-id="dcc91-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    PROFILER_PARENT_UNKNOWN = 0xFFFFFFFD,  
    PROFILER_GLOBAL_CLASS   = 0xFFFFFFFE,  
    PROFILER_GLOBAL_MODULE  = 0xFFFFFFFF  
} COR_PRF_MISC;  
```  
  
## <a name="members"></a><span data-ttu-id="dcc91-106">成员</span><span class="sxs-lookup"><span data-stu-id="dcc91-106">Members</span></span>  
  
|<span data-ttu-id="dcc91-107">成员</span><span class="sxs-lookup"><span data-stu-id="dcc91-107">Member</span></span>|<span data-ttu-id="dcc91-108">说明</span><span class="sxs-lookup"><span data-stu-id="dcc91-108">Description</span></span>|  
|------------|-----------------|  
|`PROFILER_PARENT_UNKNOWN`|<span data-ttu-id="dcc91-109">[ICorProfilerInfo：： GetModuleInfo](icorprofilerinfo-getmoduleinfo-method.md)用于尚未附加到程序集的模块的默认标识符。</span><span class="sxs-lookup"><span data-stu-id="dcc91-109">The default identifier used by [ICorProfilerInfo::GetModuleInfo](icorprofilerinfo-getmoduleinfo-method.md) for a module that has not yet been attached to an assembly.</span></span>|  
|`PROFILER_GLOBAL_CLASS`|<span data-ttu-id="dcc91-110">不属于类的全局常数的默认类标识符。</span><span class="sxs-lookup"><span data-stu-id="dcc91-110">The default class identifier for global constants that do not belong to a class.</span></span>|  
|`PROFILER_GLOBAL_MODULE`|<span data-ttu-id="dcc91-111">不属于模块的全局对象的默认模块标识符。</span><span class="sxs-lookup"><span data-stu-id="dcc91-111">The default module identifier for global objects that do not belong to a module.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="dcc91-112">要求</span><span class="sxs-lookup"><span data-stu-id="dcc91-112">Requirements</span></span>  

 <span data-ttu-id="dcc91-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dcc91-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dcc91-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="dcc91-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="dcc91-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dcc91-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dcc91-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dcc91-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dcc91-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="dcc91-117">See also</span></span>

- [<span data-ttu-id="dcc91-118">分析枚举</span><span class="sxs-lookup"><span data-stu-id="dcc91-118">Profiling Enumerations</span></span>](profiling-enumerations.md)
