---
description: 了解详细信息： CorDebugHandleType 枚举
title: CorDebugHandleType 枚举
ms.date: 03/30/2017
api_name:
- CorDebugHandleType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugHandleType
helpviewer_keywords:
- CorDebugHandleType enumeration [.NET Framework debugging]
ms.assetid: 84296b55-c2c5-424c-ac9c-8e28e2895945
topic_type:
- apiref
ms.openlocfilehash: 294fd7b04018331489e51d12930bcbbb81ec340a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662112"
---
# <a name="cordebughandletype-enumeration"></a><span data-ttu-id="315c6-103">CorDebugHandleType 枚举</span><span class="sxs-lookup"><span data-stu-id="315c6-103">CorDebugHandleType Enumeration</span></span>

<span data-ttu-id="315c6-104">指示句柄类型。</span><span class="sxs-lookup"><span data-stu-id="315c6-104">Indicates the handle type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="315c6-105">语法</span><span class="sxs-lookup"><span data-stu-id="315c6-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugHandleType {  
    HANDLE_STRONG                  = 1,  
    HANDLE_WEAK_TRACK_RESURRECTION = 2  
} CorDebugHandleType;  
```  
  
## <a name="members"></a><span data-ttu-id="315c6-106">成员</span><span class="sxs-lookup"><span data-stu-id="315c6-106">Members</span></span>  
  
|<span data-ttu-id="315c6-107">成员</span><span class="sxs-lookup"><span data-stu-id="315c6-107">Member</span></span>|<span data-ttu-id="315c6-108">说明</span><span class="sxs-lookup"><span data-stu-id="315c6-108">Description</span></span>|  
|------------|-----------------|  
|`HANDLE_STRONG`|<span data-ttu-id="315c6-109">句柄是强的，这会阻止垃圾回收功能回收对象。</span><span class="sxs-lookup"><span data-stu-id="315c6-109">The handle is strong, which prevents an object from being reclaimed by garbage collection.</span></span>|  
|`HANDLE_WEAK_TRACK_RESURRECTION`|<span data-ttu-id="315c6-110">句柄是弱的，不会阻止垃圾回收来回收对象。</span><span class="sxs-lookup"><span data-stu-id="315c6-110">The handle is weak, which does not prevent an object from being reclaimed by garbage collection.</span></span><br /><br /> <span data-ttu-id="315c6-111">收集对象时句柄变为无效。</span><span class="sxs-lookup"><span data-stu-id="315c6-111">The handle becomes invalid when the object is collected.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="315c6-112">要求</span><span class="sxs-lookup"><span data-stu-id="315c6-112">Requirements</span></span>  

 <span data-ttu-id="315c6-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="315c6-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="315c6-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="315c6-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="315c6-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="315c6-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="315c6-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="315c6-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="315c6-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="315c6-117">See also</span></span>

- [<span data-ttu-id="315c6-118">调试枚举</span><span class="sxs-lookup"><span data-stu-id="315c6-118">Debugging Enumerations</span></span>](debugging-enumerations.md)
