---
description: 了解详细信息： CorDebugExceptionCallbackType 枚举
title: CorDebugExceptionCallbackType 枚举
ms.date: 03/30/2017
api_name:
- CorDebugExceptionCallbackType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugExceptionCallbackType
helpviewer_keywords:
- CorDebugExceptionCallbackType enumeration [.NET Framework debugging]
ms.assetid: 4d946ad4-3c19-42cb-bec9-8633325ba769
topic_type:
- apiref
ms.openlocfilehash: 41b9cdf707de017703ee3756b3d04a38163bb03b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801678"
---
# <a name="cordebugexceptioncallbacktype-enumeration"></a><span data-ttu-id="24680-103">CorDebugExceptionCallbackType 枚举</span><span class="sxs-lookup"><span data-stu-id="24680-103">CorDebugExceptionCallbackType Enumeration</span></span>

<span data-ttu-id="24680-104">指示从 [ICorDebugManagedCallback2：： Exception](icordebugmanagedcallback2-exception-method.md) 事件进行的回调类型。</span><span class="sxs-lookup"><span data-stu-id="24680-104">Indicates the type of callback that is made from an [ICorDebugManagedCallback2::Exception](icordebugmanagedcallback2-exception-method.md) event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24680-105">语法</span><span class="sxs-lookup"><span data-stu-id="24680-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugExceptionCallbackType {  
    DEBUG_EXCEPTION_FIRST_CHANCE         = 1,  
    DEBUG_EXCEPTION_USER_FIRST_CHANCE    = 2,  
    DEBUG_EXCEPTION_CATCH_HANDLER_FOUND  = 3,  
    DEBUG_EXCEPTION_UNHANDLED            = 4  
} CorDebugExceptionCallbackType;  
```  
  
## <a name="members"></a><span data-ttu-id="24680-106">成员</span><span class="sxs-lookup"><span data-stu-id="24680-106">Members</span></span>  
  
|<span data-ttu-id="24680-107">成员</span><span class="sxs-lookup"><span data-stu-id="24680-107">Member</span></span>|<span data-ttu-id="24680-108">说明</span><span class="sxs-lookup"><span data-stu-id="24680-108">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_EXCEPTION_FIRST_CHANCE`|<span data-ttu-id="24680-109">引发了异常。</span><span class="sxs-lookup"><span data-stu-id="24680-109">An exception was thrown.</span></span>|  
|`DEBUG_EXCEPTION_USER_FIRST_CHANCE`|<span data-ttu-id="24680-110">异常 windup 进程输入了用户代码。</span><span class="sxs-lookup"><span data-stu-id="24680-110">The exception windup process entered user code.</span></span>|  
|`DEBUG_EXCEPTION_CATCH_HANDLER_FOUND`|<span data-ttu-id="24680-111">异常 windup 进程 `catch` 在用户代码中找到了一个块。</span><span class="sxs-lookup"><span data-stu-id="24680-111">The exception windup process found a `catch` block in user code.</span></span>|  
|`DEBUG_EXCEPTION_UNHANDLED`|<span data-ttu-id="24680-112">异常未处理。</span><span class="sxs-lookup"><span data-stu-id="24680-112">The exception was not handled.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="24680-113">要求</span><span class="sxs-lookup"><span data-stu-id="24680-113">Requirements</span></span>  

 <span data-ttu-id="24680-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="24680-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24680-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="24680-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="24680-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="24680-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="24680-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="24680-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24680-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="24680-118">See also</span></span>

- [<span data-ttu-id="24680-119">调试枚举</span><span class="sxs-lookup"><span data-stu-id="24680-119">Debugging Enumerations</span></span>](debugging-enumerations.md)
