---
description: 了解详细信息： CorDebugIlToNativeMappingTypes 枚举
title: CorDebugIlToNativeMappingTypes 枚举
ms.date: 03/30/2017
api_name:
- CorDebugIlToNativeMappingTypes
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugIlToNativeMappingTypes
helpviewer_keywords:
- CorDebugIIToNativeMappingTypes enumeration [.NET Framework debugging]
ms.assetid: c35e2919-42c3-4ba0-ae28-443c35f66f93
topic_type:
- apiref
ms.openlocfilehash: bcca11bf3c7574fe76684f6786d7408c80acfa43
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801626"
---
# <a name="cordebugiltonativemappingtypes-enumeration"></a><span data-ttu-id="deade-103">CorDebugIlToNativeMappingTypes 枚举</span><span class="sxs-lookup"><span data-stu-id="deade-103">CorDebugIlToNativeMappingTypes Enumeration</span></span>

<span data-ttu-id="deade-104">指示本机指令的特定范围是否由 COR_DEBUG_IL_TO_NATIVE_MAP 结构的实例表示，是否对应于一个特殊的代码区域。</span><span class="sxs-lookup"><span data-stu-id="deade-104">Indicates whether a particular range of native instructions, represented by an instance of the COR_DEBUG_IL_TO_NATIVE_MAP structure, corresponds to a special code region.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="deade-105">语法</span><span class="sxs-lookup"><span data-stu-id="deade-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugIlToNativeMappingTypes {  
    NO_MAPPING = -1,  
    PROLOG     = -2,  
    EPILOG     = -3  
} CorDebugIlToNativeMappingTypes;  
```  
  
## <a name="members"></a><span data-ttu-id="deade-106">成员</span><span class="sxs-lookup"><span data-stu-id="deade-106">Members</span></span>  
  
|<span data-ttu-id="deade-107">成员</span><span class="sxs-lookup"><span data-stu-id="deade-107">Member</span></span>|<span data-ttu-id="deade-108">说明</span><span class="sxs-lookup"><span data-stu-id="deade-108">Description</span></span>|  
|------------|-----------------|  
|`NO_MAPPING`|<span data-ttu-id="deade-109">本机指令的范围不对应于任何特殊代码区域。</span><span class="sxs-lookup"><span data-stu-id="deade-109">The range of native instructions does not correspond to any special code region.</span></span>|  
|`PROLOG`|<span data-ttu-id="deade-110">本机指令的范围对应于序言。</span><span class="sxs-lookup"><span data-stu-id="deade-110">The range of native instructions corresponds to the prolog.</span></span>|  
|`EPILOG`|<span data-ttu-id="deade-111">本机指令的范围对应于 epilog。</span><span class="sxs-lookup"><span data-stu-id="deade-111">The range of native instructions corresponds to the epilog.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="deade-112">要求</span><span class="sxs-lookup"><span data-stu-id="deade-112">Requirements</span></span>  

 <span data-ttu-id="deade-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="deade-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="deade-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="deade-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="deade-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="deade-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="deade-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="deade-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="deade-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="deade-117">See also</span></span>

- [<span data-ttu-id="deade-118">GetILToNativeMapping 方法</span><span class="sxs-lookup"><span data-stu-id="deade-118">GetILToNativeMapping Method</span></span>](icordebugcode-getiltonativemapping-method.md)
- [<span data-ttu-id="deade-119">调试枚举</span><span class="sxs-lookup"><span data-stu-id="deade-119">Debugging Enumerations</span></span>](debugging-enumerations.md)
