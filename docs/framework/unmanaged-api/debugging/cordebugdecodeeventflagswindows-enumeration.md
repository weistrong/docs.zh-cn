---
description: 了解详细信息： CorDebugDecodeEventFlagsWindows 枚举
title: “Cor调试解码事件标志窗口”枚举
ms.date: 03/30/2017
api_name:
- CorDebugDecodeEventFlagsWindows
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: aa6cf962-30ae-4cfd-8895-826deeb46a54
topic_type:
- apiref
ms.openlocfilehash: 765ce4b967d00bd70becca666e2ed418614d6fe3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801691"
---
# <a name="cordebugdecodeeventflagswindows-enumeration"></a><span data-ttu-id="01eee-103">“Cor调试解码事件标志窗口”枚举</span><span class="sxs-lookup"><span data-stu-id="01eee-103">CorDebugDecodeEventFlagsWindows Enumeration</span></span>

<span data-ttu-id="01eee-104">提供关于 Windows 平台上的调试事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="01eee-104">Provides additional information about debug events on the Windows platform.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="01eee-105">语法</span><span class="sxs-lookup"><span data-stu-id="01eee-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugDecodeEventFlagsWindows {  
    IS_FIRST_CHANCE = 1,  
} CorDebugDecodeEventFlagsWindows;  
```  
  
## <a name="members"></a><span data-ttu-id="01eee-106">成员</span><span class="sxs-lookup"><span data-stu-id="01eee-106">Members</span></span>  
  
|<span data-ttu-id="01eee-107">成员</span><span class="sxs-lookup"><span data-stu-id="01eee-107">Member</span></span>|<span data-ttu-id="01eee-108">说明</span><span class="sxs-lookup"><span data-stu-id="01eee-108">Description</span></span>|  
|------------|-----------------|  
|`IS_FIRST_CHANCE`|<span data-ttu-id="01eee-109">指出调试事件为最可能的异常。</span><span class="sxs-lookup"><span data-stu-id="01eee-109">Indicates that the debug event is a first-chance exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="01eee-110">备注</span><span class="sxs-lookup"><span data-stu-id="01eee-110">Remarks</span></span>  

 <span data-ttu-id="01eee-111">[ICorDebugProcess6：:D ecodeevent](icordebugprocess6-decodeevent-method.md)方法包含一个 `dwFlags` 参数，该参数提供有关调试事件的附加信息，并且其值依赖于目标体系结构。</span><span class="sxs-lookup"><span data-stu-id="01eee-111">The [ICorDebugProcess6::DecodeEvent](icordebugprocess6-decodeevent-method.md) method includes a `dwFlags` parameter that provides additional information about a debug event and whose value is dependent on the target architecture.</span></span> <span data-ttu-id="01eee-112">`CorDebugDecodeEventFlagsWindows` 枚举可与 Windows 平台上的调试事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="01eee-112">The `CorDebugDecodeEventFlagsWindows` enumeration can be used with debug events on the Windows platform.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="01eee-113">此枚举仅用于 .NET Native 调试方案。</span><span class="sxs-lookup"><span data-stu-id="01eee-113">This enumeration is intended for use in .NET Native debugging scenarios only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="01eee-114">要求</span><span class="sxs-lookup"><span data-stu-id="01eee-114">Requirements</span></span>  

 <span data-ttu-id="01eee-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="01eee-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="01eee-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="01eee-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="01eee-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="01eee-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="01eee-118">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="01eee-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01eee-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="01eee-119">See also</span></span>

- [<span data-ttu-id="01eee-120">调试枚举</span><span class="sxs-lookup"><span data-stu-id="01eee-120">Debugging Enumerations</span></span>](debugging-enumerations.md)
