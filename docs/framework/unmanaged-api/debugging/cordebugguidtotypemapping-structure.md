---
description: 了解详细信息： CorDebugGuidToTypeMapping 结构
title: CorDebugGuidToTypeMapping 结构
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CorDebugGuidToTypeMapping
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugGuidToTypeMapping
helpviewer_keywords:
- CorDebugGuidToTypeMapping structure [.NET Framework debugging]
ms.assetid: 57dbccd9-b16d-4da3-ae25-7a2cf9adf679
topic_type:
- apiref
ms.openlocfilehash: 5f6e99a17483b4fc16eb36ebb5fb5fd81380944b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801613"
---
# <a name="cordebugguidtotypemapping-structure"></a><span data-ttu-id="3aff3-103">CorDebugGuidToTypeMapping 结构</span><span class="sxs-lookup"><span data-stu-id="3aff3-103">CorDebugGuidToTypeMapping Structure</span></span>

<span data-ttu-id="3aff3-104">将 Windows 运行时 GUID 映射到其对应的 ICorDebugType 对象。</span><span class="sxs-lookup"><span data-stu-id="3aff3-104">Maps a Windows Runtime GUID to its corresponding ICorDebugType object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3aff3-105">语法</span><span class="sxs-lookup"><span data-stu-id="3aff3-105">Syntax</span></span>  
  
```cpp
typedef struct CorDebugGuidToTypeMapping {  
    GUID iid;  
    ICorDebugType *pType;  
} CorDebugGuidToTypeMapping;  
```  
  
## <a name="members"></a><span data-ttu-id="3aff3-106">成员</span><span class="sxs-lookup"><span data-stu-id="3aff3-106">Members</span></span>  
  
|<span data-ttu-id="3aff3-107">成员</span><span class="sxs-lookup"><span data-stu-id="3aff3-107">Member</span></span>|<span data-ttu-id="3aff3-108">说明</span><span class="sxs-lookup"><span data-stu-id="3aff3-108">Description</span></span>|  
|------------|-----------------|  
|`iid`|<span data-ttu-id="3aff3-109">缓存的 Windows 运行时类型的 GUID。</span><span class="sxs-lookup"><span data-stu-id="3aff3-109">The GUID of the cached Windows Runtime type.</span></span>|  
|`pType`|<span data-ttu-id="3aff3-110">指向 ICorDebugType 对象的指针，该对象提供有关缓存类型的信息。</span><span class="sxs-lookup"><span data-stu-id="3aff3-110">A pointer to an ICorDebugType object that provides information about the cached type.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3aff3-111">要求</span><span class="sxs-lookup"><span data-stu-id="3aff3-111">Requirements</span></span>  

 <span data-ttu-id="3aff3-112">**平台：** Windows 运行时。</span><span class="sxs-lookup"><span data-stu-id="3aff3-112">**Platforms:** Windows Runtime.</span></span>  
  
 <span data-ttu-id="3aff3-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3aff3-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3aff3-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3aff3-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3aff3-115">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3aff3-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3aff3-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="3aff3-116">See also</span></span>

- [<span data-ttu-id="3aff3-117">调试结构</span><span class="sxs-lookup"><span data-stu-id="3aff3-117">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="3aff3-118">调试</span><span class="sxs-lookup"><span data-stu-id="3aff3-118">Debugging</span></span>](index.md)
