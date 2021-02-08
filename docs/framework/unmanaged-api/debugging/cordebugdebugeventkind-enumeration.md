---
description: 了解详细信息： CorDebugDebugEventKind 枚举
title: “Cor调试调试事件类型”枚举
ms.date: 03/30/2017
api_name:
- CorDebugDebugEventKind
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 6075a6cd-97e6-4472-a090-0dd14860d1f3
topic_type:
- apiref
ms.openlocfilehash: 62094c934873a74fdab01fad87c42126e28cb0f4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801704"
---
# <a name="cordebugdebugeventkind-enumeration"></a><span data-ttu-id="7836f-103">“Cor调试调试事件类型”枚举</span><span class="sxs-lookup"><span data-stu-id="7836f-103">CorDebugDebugEventKind Enumeration</span></span>

<span data-ttu-id="7836f-104">指示 [DecodeEvent](icordebugprocess6-decodeevent-method.md) 方法对其信息进行解码的事件类型。</span><span class="sxs-lookup"><span data-stu-id="7836f-104">Indicates the type of event whose information is decoded by the [DecodeEvent](icordebugprocess6-decodeevent-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7836f-105">语法</span><span class="sxs-lookup"><span data-stu-id="7836f-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugDebugEventKind {  
    DEBUG_EVENT_KIND_MODULE_LOADED                          = 1,  
    DEBUG_EVENT_KIND_MODULE_UNLOADED                        = 2,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_FIRST_CHANCE         = 3,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_USER_FIRST_CHANCE    = 4,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_CATCH_HANDLER_FOUND  = 5,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_UNHANDLED            = 6  
} CorDebugRecordFormat;  
```  
  
## <a name="members"></a><span data-ttu-id="7836f-106">成员</span><span class="sxs-lookup"><span data-stu-id="7836f-106">Members</span></span>  
  
|<span data-ttu-id="7836f-107">成员</span><span class="sxs-lookup"><span data-stu-id="7836f-107">Member</span></span>|<span data-ttu-id="7836f-108">说明</span><span class="sxs-lookup"><span data-stu-id="7836f-108">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_EVENT_KIND_MODULE_LOADED`|<span data-ttu-id="7836f-109">模块加载事件。</span><span class="sxs-lookup"><span data-stu-id="7836f-109">A module load event.</span></span>|  
|`DEBUG_EVENT_KIND_MODULE_UNLOADED`|<span data-ttu-id="7836f-110">模块卸载事件。</span><span class="sxs-lookup"><span data-stu-id="7836f-110">A module unload event.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_FIRST_CHANCE`|<span data-ttu-id="7836f-111">最可能的异常。</span><span class="sxs-lookup"><span data-stu-id="7836f-111">A first-chance exception.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_USER_FIRST_CHANCE`|<span data-ttu-id="7836f-112">最可能的用户异常。</span><span class="sxs-lookup"><span data-stu-id="7836f-112">A first-chance user exception.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_CATCH_HANDLER_FOUND`|<span data-ttu-id="7836f-113">`catch` 处理程序存在的异常。</span><span class="sxs-lookup"><span data-stu-id="7836f-113">An exception for which a `catch` handler exists.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_UNHANDLED`|<span data-ttu-id="7836f-114">未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="7836f-114">An unhandled exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7836f-115">备注</span><span class="sxs-lookup"><span data-stu-id="7836f-115">Remarks</span></span>  

 <span data-ttu-id="7836f-116">枚举的成员 `CorDebugDebugEventKind` 是通过调用 [ICorDebugDebugEvent：： GetEventKind](icordebugdebugevent-geteventkind-method.md) 方法返回的。</span><span class="sxs-lookup"><span data-stu-id="7836f-116">A member of the `CorDebugDebugEventKind` enumeration is returned by calling the [ICorDebugDebugEvent::GetEventKind](icordebugdebugevent-geteventkind-method.md) method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7836f-117">此枚举仅用于 .NET Native 调试方案。</span><span class="sxs-lookup"><span data-stu-id="7836f-117">This enumeration is intended for use in .NET Native debugging scenarios only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7836f-118">要求</span><span class="sxs-lookup"><span data-stu-id="7836f-118">Requirements</span></span>  

 <span data-ttu-id="7836f-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7836f-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7836f-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7836f-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7836f-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7836f-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7836f-122">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7836f-122">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7836f-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="7836f-123">See also</span></span>

- [<span data-ttu-id="7836f-124">调试枚举</span><span class="sxs-lookup"><span data-stu-id="7836f-124">Debugging Enumerations</span></span>](debugging-enumerations.md)
