---
description: 了解详细信息： CorDebugNGenPolicy 枚举
title: CorDebugNGenPolicy 枚举
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CorDebugNGenPolicy
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugNGenPolicy
helpviewer_keywords:
- CorDebugNgenPolicy enumeration [.NET Framework debugging]
ms.assetid: edb4e4d2-3166-44d4-8b17-bf302f7ea093
topic_type:
- apiref
ms.openlocfilehash: 529a5979bacef32ce78262c122004a66b54156ed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801574"
---
# <a name="cordebugngenpolicy-enumeration"></a><span data-ttu-id="4e55c-103">CorDebugNGenPolicy 枚举</span><span class="sxs-lookup"><span data-stu-id="4e55c-103">CorDebugNGenPolicy Enumeration</span></span>

<span data-ttu-id="4e55c-104">提供用于确定调试器是否从本机映像缓存中加载本机 (NGen) 映像的值。</span><span class="sxs-lookup"><span data-stu-id="4e55c-104">Provides a value that determines whether a debugger loads native (NGen) images from the native image cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e55c-105">语法</span><span class="sxs-lookup"><span data-stu-id="4e55c-105">Syntax</span></span>  
  
```cpp
enum CorDebugNGENPolicy {  
    DISABLE_LOCAL_NIC = 1  
} CorDebugNGENPolicy;  
```  
  
## <a name="members"></a><span data-ttu-id="4e55c-106">成员</span><span class="sxs-lookup"><span data-stu-id="4e55c-106">Members</span></span>  
  
|<span data-ttu-id="4e55c-107">成员名称</span><span class="sxs-lookup"><span data-stu-id="4e55c-107">Member name</span></span>|<span data-ttu-id="4e55c-108">描述</span><span class="sxs-lookup"><span data-stu-id="4e55c-108">Description</span></span>|  
|-----------------|-----------------|  
|`DISABLE_LOCAL_NIC`|<span data-ttu-id="4e55c-109">在 Windows 8.x 应用商店应用中，禁用了本地本机映像缓存中的映像。</span><span class="sxs-lookup"><span data-stu-id="4e55c-109">In a Windows 8.x Store app, the use of images from the local native image cache is disabled.</span></span> <span data-ttu-id="4e55c-110">在桌面应用中，此设置不起作用。</span><span class="sxs-lookup"><span data-stu-id="4e55c-110">In a desktop app, this setting has no effect.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4e55c-111">备注</span><span class="sxs-lookup"><span data-stu-id="4e55c-111">Remarks</span></span>  

 <span data-ttu-id="4e55c-112">`CorDebugNGENPolicy`枚举由[ICorDebugProcess5：： EnableNGENPolicy](icordebugprocess5-enablengenpolicy-method.md)方法使用。</span><span class="sxs-lookup"><span data-stu-id="4e55c-112">The `CorDebugNGENPolicy` enumeration is used by the [ICorDebugProcess5::EnableNGENPolicy](icordebugprocess5-enablengenpolicy-method.md) method.</span></span> <span data-ttu-id="4e55c-113">禁用本地本机映像缓存中的映像可提供一致的调试体验，方法是确保调试器加载可调试 JIT 编译的映像，而不是优化的本机映像。</span><span class="sxs-lookup"><span data-stu-id="4e55c-113">Disabling the use of images from the local native image cache provides for a consistent debugging experience by ensuring that the debugger loads debuggable JIT-compiled images instead of optimized native images.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4e55c-114">要求</span><span class="sxs-lookup"><span data-stu-id="4e55c-114">Requirements</span></span>  

 <span data-ttu-id="4e55c-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4e55c-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4e55c-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4e55c-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4e55c-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4e55c-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4e55c-118">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4e55c-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4e55c-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="4e55c-119">See also</span></span>

- [<span data-ttu-id="4e55c-120">调试枚举</span><span class="sxs-lookup"><span data-stu-id="4e55c-120">Debugging Enumerations</span></span>](debugging-enumerations.md)
