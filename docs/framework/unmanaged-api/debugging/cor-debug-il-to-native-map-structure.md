---
description: 了解详细信息： COR_DEBUG_IL_TO_NATIVE_MAP 结构
title: COR_DEBUG_IL_TO_NATIVE_MAP 结构
ms.date: 03/30/2017
api_name:
- COR_DEBUG_IL_TO_NATIVE_MAP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_DEBUG_IL_TO_NATIVE_MAP
helpviewer_keywords:
- COR_DEBUG_IL_TO_NATIVE_MAP structure [.NET Framework debugging]
ms.assetid: 06f3b504-085f-4142-934a-25381fe23d4c
topic_type:
- apiref
ms.openlocfilehash: ec722b86f95e75d4ac00e04e8a602c6b6da64de5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747187"
---
# <a name="cor_debug_il_to_native_map-structure"></a><span data-ttu-id="5b141-103">COR_DEBUG_IL_TO_NATIVE_MAP 结构</span><span class="sxs-lookup"><span data-stu-id="5b141-103">COR_DEBUG_IL_TO_NATIVE_MAP Structure</span></span>

<span data-ttu-id="5b141-104">包含用于将 Microsoft 中间语言 (MSIL) 代码映射到本机代码的偏移量。</span><span class="sxs-lookup"><span data-stu-id="5b141-104">Contains the offsets that are used to map Microsoft intermediate language (MSIL) code to native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5b141-105">语法</span><span class="sxs-lookup"><span data-stu-id="5b141-105">Syntax</span></span>  
  
```cpp  
typedef struct COR_DEBUG_IL_TO_NATIVE_MAP {  
    ULONG32  ilOffset;  
    ULONG32  nativeStartOffset;  
    ULONG32  nativeEndOffset;  
} COR_DEBUG_IL_TO_NATIVE_MAP;  
```  
  
## <a name="members"></a><span data-ttu-id="5b141-106">成员</span><span class="sxs-lookup"><span data-stu-id="5b141-106">Members</span></span>  
  
|<span data-ttu-id="5b141-107">成员</span><span class="sxs-lookup"><span data-stu-id="5b141-107">Member</span></span>|<span data-ttu-id="5b141-108">说明</span><span class="sxs-lookup"><span data-stu-id="5b141-108">Description</span></span>|  
|------------|-----------------|  
|`ilOffset`|<span data-ttu-id="5b141-109">MSIL 代码的偏移量。</span><span class="sxs-lookup"><span data-stu-id="5b141-109">The offset of the MSIL code.</span></span>|  
|`nativeStartOffset`|<span data-ttu-id="5b141-110">本机代码起始位置的偏移量。</span><span class="sxs-lookup"><span data-stu-id="5b141-110">The offset of the start of the native code.</span></span>|  
|`nativeEndOffset`|<span data-ttu-id="5b141-111">本机代码末尾的偏移量。</span><span class="sxs-lookup"><span data-stu-id="5b141-111">The offset of the end of the native code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5b141-112">要求</span><span class="sxs-lookup"><span data-stu-id="5b141-112">Requirements</span></span>  

 <span data-ttu-id="5b141-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5b141-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5b141-114">**标头：** Corprof.idl、Cordebug.idl</span><span class="sxs-lookup"><span data-stu-id="5b141-114">**Header:** CorProf.idl, CorDebug.idl</span></span>  
  
 <span data-ttu-id="5b141-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5b141-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5b141-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5b141-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5b141-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="5b141-117">See also</span></span>

- [<span data-ttu-id="5b141-118">GetILToNativeMapping 方法</span><span class="sxs-lookup"><span data-stu-id="5b141-118">GetILToNativeMapping Method</span></span>](../profiling/icorprofilerinfo-getiltonativemapping-method.md)
- [<span data-ttu-id="5b141-119">GetILToNativeMapping 方法</span><span class="sxs-lookup"><span data-stu-id="5b141-119">GetILToNativeMapping Method</span></span>](icordebugcode-getiltonativemapping-method.md)
- [<span data-ttu-id="5b141-120">调试结构</span><span class="sxs-lookup"><span data-stu-id="5b141-120">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="5b141-121">调试</span><span class="sxs-lookup"><span data-stu-id="5b141-121">Debugging</span></span>](index.md)
