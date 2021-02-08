---
description: 了解详细信息： CorDebugCreateProcessFlags 枚举
title: CorDebugCreateProcessFlags 枚举
ms.date: 03/30/2017
api_name:
- CorDebugCreateProcessFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugCreateProcessFlags
helpviewer_keywords:
- CorDebugCreateProcessFlags enumeration [.NET Framework debugging]
ms.assetid: e709acce-6a17-4346-b38a-467dba567358
topic_type:
- apiref
ms.openlocfilehash: 29363510c83873c7f367079857809c165bc55b1e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801730"
---
# <a name="cordebugcreateprocessflags-enumeration"></a><span data-ttu-id="d497a-103">CorDebugCreateProcessFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="d497a-103">CorDebugCreateProcessFlags Enumeration</span></span>

<span data-ttu-id="d497a-104">提供可在对 [ICorDebug：： CreateProcess](icordebug-createprocess-method.md) 方法的调用中使用的其他调试选项。</span><span class="sxs-lookup"><span data-stu-id="d497a-104">Provides additional debugging options that can be used in a call to the [ICorDebug::CreateProcess](icordebug-createprocess-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d497a-105">语法</span><span class="sxs-lookup"><span data-stu-id="d497a-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugCreateProcessFlags {  
    DEBUG_NO_SPECIAL_OPTIONS    = 0x0000  
} CorDebugCreateProcessFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="d497a-106">成员</span><span class="sxs-lookup"><span data-stu-id="d497a-106">Members</span></span>  
  
|<span data-ttu-id="d497a-107">成员</span><span class="sxs-lookup"><span data-stu-id="d497a-107">Member</span></span>|<span data-ttu-id="d497a-108">说明</span><span class="sxs-lookup"><span data-stu-id="d497a-108">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_NO_SPECIAL_OPTIONS`|<span data-ttu-id="d497a-109">未设置任何特殊选项。</span><span class="sxs-lookup"><span data-stu-id="d497a-109">No special options are set.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d497a-110">要求</span><span class="sxs-lookup"><span data-stu-id="d497a-110">Requirements</span></span>  

 <span data-ttu-id="d497a-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d497a-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d497a-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d497a-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d497a-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d497a-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d497a-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d497a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d497a-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="d497a-115">See also</span></span>

- [<span data-ttu-id="d497a-116">调试枚举</span><span class="sxs-lookup"><span data-stu-id="d497a-116">Debugging Enumerations</span></span>](debugging-enumerations.md)
