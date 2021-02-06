---
description: 了解详细信息： CorDebugJITCompilerFlagsDeprecated 枚举
title: CorDebugJITCompilerFlagsDeprecated 枚举
ms.date: 03/30/2017
api_name:
- CorDebugJITCompilerFlagsDeprecated
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugJITCompilerFlagsDeprecated
helpviewer_keywords:
- CorDebugJITCompilerFlagsDeprecated enumeration [.NET Framework debugging]
ms.assetid: af15e2ca-6be1-472b-bd36-03644a1e3ddd
topic_type:
- apiref
ms.openlocfilehash: ac607766c484a63a757d726826c81d16edd48aae
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661904"
---
# <a name="cordebugjitcompilerflagsdeprecated-enumeration"></a><span data-ttu-id="e1189-103">CorDebugJITCompilerFlagsDeprecated 枚举</span><span class="sxs-lookup"><span data-stu-id="e1189-103">CorDebugJITCompilerFlagsDeprecated Enumeration</span></span>

<span data-ttu-id="e1189-104">此枚举已过时。</span><span class="sxs-lookup"><span data-stu-id="e1189-104">This enumeration is obsolete.</span></span> <span data-ttu-id="e1189-105">改为使用 `CORDEBUG_JIT_DEFAULT` [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) 枚举的成员。</span><span class="sxs-lookup"><span data-stu-id="e1189-105">Use the `CORDEBUG_JIT_DEFAULT` member of the [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) enumeration instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e1189-106">语法</span><span class="sxs-lookup"><span data-stu-id="e1189-106">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugJITCompilerFlagsDeprecated {  
    CORDEBUG_JIT_TRACK_DEBUG_INFO  = 0x1  
} CorDebugJITCompilerFlagsDeprecated;  
```  
  
## <a name="members"></a><span data-ttu-id="e1189-107">成员</span><span class="sxs-lookup"><span data-stu-id="e1189-107">Members</span></span>  
  
|<span data-ttu-id="e1189-108">成员</span><span class="sxs-lookup"><span data-stu-id="e1189-108">Member</span></span>|<span data-ttu-id="e1189-109">说明</span><span class="sxs-lookup"><span data-stu-id="e1189-109">Description</span></span>|  
|------------|-----------------|  
|`CORDEBUG_JIT_TRACK_DEBUG_INFO`|<span data-ttu-id="e1189-110">请改用 `CORDEBUG_JIT_DEFAULT`。</span><span class="sxs-lookup"><span data-stu-id="e1189-110">Use `CORDEBUG_JIT_DEFAULT` instead.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e1189-111">要求</span><span class="sxs-lookup"><span data-stu-id="e1189-111">Requirements</span></span>  

 <span data-ttu-id="e1189-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e1189-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e1189-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e1189-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e1189-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e1189-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e1189-115">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="e1189-115">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1189-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="e1189-116">See also</span></span>

- [<span data-ttu-id="e1189-117">调试枚举</span><span class="sxs-lookup"><span data-stu-id="e1189-117">Debugging Enumerations</span></span>](debugging-enumerations.md)
