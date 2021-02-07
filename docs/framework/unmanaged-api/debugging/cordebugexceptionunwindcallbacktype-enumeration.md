---
description: 了解详细信息： CorDebugExceptionUnwindCallbackType 枚举
title: CorDebugExceptionUnwindCallbackType 枚举
ms.date: 03/30/2017
api_name:
- CorDebugExceptionUnwindCallbackType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugExceptionUnwindCallbackType
helpviewer_keywords:
- CorDebugExceptionUnwindCallbackType enumeration [.NET Framework debugging]
ms.assetid: 783dce92-8a98-43db-8f78-888d943dd5b2
topic_type:
- apiref
ms.openlocfilehash: 3e12cffcdf1eb921330f658215c52501dce83eff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747018"
---
# <a name="cordebugexceptionunwindcallbacktype-enumeration"></a><span data-ttu-id="8fb84-103">CorDebugExceptionUnwindCallbackType 枚举</span><span class="sxs-lookup"><span data-stu-id="8fb84-103">CorDebugExceptionUnwindCallbackType Enumeration</span></span>

<span data-ttu-id="8fb84-104">指示在展开阶段正由回调发送信号的事件。</span><span class="sxs-lookup"><span data-stu-id="8fb84-104">Indicates the event that is being signaled by the callback during the unwind phase.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8fb84-105">语法</span><span class="sxs-lookup"><span data-stu-id="8fb84-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugExceptionUnwindCallbackType {  
    DEBUG_EXCEPTION_UNWIND_BEGIN = 1,  
    DEBUG_EXCEPTION_INTERCEPTED  = 2  
} CorDebugExceptionUnwindCallbackType;  
```  
  
## <a name="members"></a><span data-ttu-id="8fb84-106">成员</span><span class="sxs-lookup"><span data-stu-id="8fb84-106">Members</span></span>  
  
|<span data-ttu-id="8fb84-107">成员</span><span class="sxs-lookup"><span data-stu-id="8fb84-107">Member</span></span>|<span data-ttu-id="8fb84-108">说明</span><span class="sxs-lookup"><span data-stu-id="8fb84-108">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_EXCEPTION_UNWIND_BEGIN`|<span data-ttu-id="8fb84-109">展开进程的开头。</span><span class="sxs-lookup"><span data-stu-id="8fb84-109">The beginning of the unwind process.</span></span>|  
|`DEBUG_EXCEPTION_INTERCEPTED`|<span data-ttu-id="8fb84-110">异常已被截取。</span><span class="sxs-lookup"><span data-stu-id="8fb84-110">The exception was intercepted.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8fb84-111">要求</span><span class="sxs-lookup"><span data-stu-id="8fb84-111">Requirements</span></span>  

 <span data-ttu-id="8fb84-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8fb84-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8fb84-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8fb84-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8fb84-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8fb84-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8fb84-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8fb84-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8fb84-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="8fb84-116">See also</span></span>

- [<span data-ttu-id="8fb84-117">调试枚举</span><span class="sxs-lookup"><span data-stu-id="8fb84-117">Debugging Enumerations</span></span>](debugging-enumerations.md)
