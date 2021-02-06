---
description: 了解详细信息： CorDebugGenerationTypes 枚举
title: CorDebugGenerationTypes 枚举
ms.date: 03/30/2017
api_name:
- CorDebugGenerationTypes
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugGenerationTypes
helpviewer_keywords:
- CorDebugGenerationTypes enumeration [.NET Framework debugging]
ms.assetid: 9f25b64f-eedd-4ae5-8b0e-cfdfb9b6c5d8
topic_type:
- apiref
ms.openlocfilehash: f86b2bc9bf947c6b285c50678f46494005bb5537
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662125"
---
# <a name="cordebuggenerationtypes-enumeration"></a><span data-ttu-id="b632b-103">CorDebugGenerationTypes 枚举</span><span class="sxs-lookup"><span data-stu-id="b632b-103">CorDebugGenerationTypes Enumeration</span></span>

<span data-ttu-id="b632b-104">指定托管堆上内存区域的生成。</span><span class="sxs-lookup"><span data-stu-id="b632b-104">Specifies the generation of a region of memory on the managed heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b632b-105">语法</span><span class="sxs-lookup"><span data-stu-id="b632b-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugGenerationTypes {  
    CorDebug_Gen0 = 0,  
    CorDebug_Gen1 = 1,  
    CorDebug_Gen2 = 2,  
    CorDebug_LOH  = 3,  
} CorDebugRegionTypes;  
```  
  
## <a name="members"></a><span data-ttu-id="b632b-106">成员</span><span class="sxs-lookup"><span data-stu-id="b632b-106">Members</span></span>  
  
|<span data-ttu-id="b632b-107">成员名称</span><span class="sxs-lookup"><span data-stu-id="b632b-107">Member name</span></span>|<span data-ttu-id="b632b-108">描述</span><span class="sxs-lookup"><span data-stu-id="b632b-108">Description</span></span>|  
|-----------------|-----------------|  
|`CorDebug_Gen0`|<span data-ttu-id="b632b-109">第 0 代。</span><span class="sxs-lookup"><span data-stu-id="b632b-109">Generation 0.</span></span>|  
|`CorDebug_Gen1`|<span data-ttu-id="b632b-110">第 1 代。</span><span class="sxs-lookup"><span data-stu-id="b632b-110">Generation 1.</span></span>|  
|`CorDebug_Gen2`|<span data-ttu-id="b632b-111">第 2 代。</span><span class="sxs-lookup"><span data-stu-id="b632b-111">Generation 2.</span></span>|  
|`CorDebug_LOH`|<span data-ttu-id="b632b-112">大型对象堆。</span><span class="sxs-lookup"><span data-stu-id="b632b-112">The large object heap.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b632b-113">备注</span><span class="sxs-lookup"><span data-stu-id="b632b-113">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b632b-114">要求</span><span class="sxs-lookup"><span data-stu-id="b632b-114">Requirements</span></span>  

 <span data-ttu-id="b632b-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b632b-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b632b-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b632b-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b632b-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b632b-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b632b-118">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b632b-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b632b-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="b632b-119">See also</span></span>

- [<span data-ttu-id="b632b-120">调试枚举</span><span class="sxs-lookup"><span data-stu-id="b632b-120">Debugging Enumerations</span></span>](debugging-enumerations.md)
