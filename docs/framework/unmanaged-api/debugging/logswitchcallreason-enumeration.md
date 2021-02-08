---
description: 了解详细信息： LogSwitchCallReason 枚举
title: LogSwitchCallReason 枚举
ms.date: 03/30/2017
api_name:
- LogSwitchCallReason
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- LogSwitchCallReason
helpviewer_keywords:
- LogSwitchCallReason enumeration [.NET Framework debugging]
ms.assetid: 5bbb8d1b-bbc4-47b0-b1b1-2d54cc0be291
topic_type:
- apiref
ms.openlocfilehash: 46c457ee4c12fe9a73796aa7b7a5f599d90c9c6c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800600"
---
# <a name="logswitchcallreason-enumeration"></a><span data-ttu-id="43392-103">LogSwitchCallReason 枚举</span><span class="sxs-lookup"><span data-stu-id="43392-103">LogSwitchCallReason Enumeration</span></span>

<span data-ttu-id="43392-104">指示已对调试/跟踪开关执行的操作。</span><span class="sxs-lookup"><span data-stu-id="43392-104">Indicates the operation that was performed on a debugging/tracing switch.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="43392-105">语法</span><span class="sxs-lookup"><span data-stu-id="43392-105">Syntax</span></span>  
  
```cpp  
typedef enum LogSwitchCallReason {  
    SWITCH_CREATE,  
    SWITCH_MODIFY,  
    SWITCH_DELETE  
} LogSwitchCallReason;  
```  
  
## <a name="members"></a><span data-ttu-id="43392-106">成员</span><span class="sxs-lookup"><span data-stu-id="43392-106">Members</span></span>  
  
|<span data-ttu-id="43392-107">成员</span><span class="sxs-lookup"><span data-stu-id="43392-107">Member</span></span>|<span data-ttu-id="43392-108">说明</span><span class="sxs-lookup"><span data-stu-id="43392-108">Description</span></span>|  
|------------|-----------------|  
|`SWITCH_CREATE`|<span data-ttu-id="43392-109">已创建调试/跟踪开关。</span><span class="sxs-lookup"><span data-stu-id="43392-109">A debugging/tracing switch was created.</span></span>|  
|`SWITCH_MODIFY`|<span data-ttu-id="43392-110">已修改调试/跟踪开关。</span><span class="sxs-lookup"><span data-stu-id="43392-110">A debugging/tracing switch was modified.</span></span>|  
|`SWITCH_DELETE`|<span data-ttu-id="43392-111">已删除调试/跟踪开关。</span><span class="sxs-lookup"><span data-stu-id="43392-111">A debugging/tracing switch was deleted.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="43392-112">要求</span><span class="sxs-lookup"><span data-stu-id="43392-112">Requirements</span></span>  

 <span data-ttu-id="43392-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="43392-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="43392-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="43392-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="43392-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="43392-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="43392-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="43392-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="43392-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="43392-117">See also</span></span>

- [<span data-ttu-id="43392-118">调试枚举</span><span class="sxs-lookup"><span data-stu-id="43392-118">Debugging Enumerations</span></span>](debugging-enumerations.md)
