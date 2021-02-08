---
description: 了解详细信息： CorDebugJITCompilerFlags 枚举
title: CorDebugJITCompilerFlags 枚举
ms.date: 03/30/2017
api_name:
- CorDebugJITCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugJITCompilerFlags
helpviewer_keywords:
- CorDebugJITCompilerFlags enumeration [.NET Framework debugging]
ms.assetid: c0774f70-5bed-45e8-9922-fdad778c4c33
topic_type:
- apiref
ms.openlocfilehash: 7e5337293aa4fe446deb12653acd22864eb7679a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801600"
---
# <a name="cordebugjitcompilerflags-enumeration"></a><span data-ttu-id="fa699-103">CorDebugJITCompilerFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="fa699-103">CorDebugJITCompilerFlags Enumeration</span></span>

<span data-ttu-id="fa699-104">包含影响托管的实时 (JIT) 编译器的行为的值。</span><span class="sxs-lookup"><span data-stu-id="fa699-104">Contains values that influence the behavior of the managed just-in-time (JIT) compiler.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa699-105">语法</span><span class="sxs-lookup"><span data-stu-id="fa699-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugJITCompilerFlags {  
  
    CORDEBUG_JIT_DEFAULT = 0x1,  
    CORDEBUG_JIT_DISABLE_OPTIMIZATION = 0x3,  
    CORDEBUG_JIT_ENABLE_ENC = 0x7  
  
} CorDebugJITCompilerFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="fa699-106">成员</span><span class="sxs-lookup"><span data-stu-id="fa699-106">Members</span></span>  
  
|<span data-ttu-id="fa699-107">成员</span><span class="sxs-lookup"><span data-stu-id="fa699-107">Member</span></span>|<span data-ttu-id="fa699-108">说明</span><span class="sxs-lookup"><span data-stu-id="fa699-108">Description</span></span>|  
|------------|-----------------|  
|`CORDEBUG_JIT_DEFAULT`|<span data-ttu-id="fa699-109">指定编译器应跟踪编译数据，并允许优化。</span><span class="sxs-lookup"><span data-stu-id="fa699-109">Specifies that the compiler should track compilation data, and allows optimizations.</span></span>|  
|`CORDEBUG_JIT_DISABLE_OPTIMIZATION`|<span data-ttu-id="fa699-110">指定编译器应跟踪编译数据，但禁用优化。</span><span class="sxs-lookup"><span data-stu-id="fa699-110">Specifies that the compiler should track compilation data, but disables optimizations.</span></span>|  
|`CORDEBUG_JIT_ENABLE_ENC`|<span data-ttu-id="fa699-111">指定编译器应跟踪编译数据，禁用优化，并启用 "编辑并继续" 技术。</span><span class="sxs-lookup"><span data-stu-id="fa699-111">Specifies that the compiler should track compilation data, disables optimizations, and enables Edit and Continue technologies.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fa699-112">要求</span><span class="sxs-lookup"><span data-stu-id="fa699-112">Requirements</span></span>  

 <span data-ttu-id="fa699-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fa699-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa699-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fa699-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fa699-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fa699-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fa699-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa699-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa699-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="fa699-117">See also</span></span>

- [<span data-ttu-id="fa699-118">调试枚举</span><span class="sxs-lookup"><span data-stu-id="fa699-118">Debugging Enumerations</span></span>](debugging-enumerations.md)
