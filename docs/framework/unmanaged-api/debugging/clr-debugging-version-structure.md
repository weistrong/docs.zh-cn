---
description: 了解详细信息： CLR_DEBUGGING_VERSION 结构
title: CLR_DEBUGGING_VERSION 结构
ms.date: 03/30/2017
api_name:
- CLR_DEBUGGING_VERSION
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CLR_DEBUGGING_VERSION
helpviewer_keywords:
- CLR_DEBUGGING_VERSION structure [.NET Framework debugging]
ms.assetid: 4d821186-3ddf-405a-ac44-d79438a9f7f3
topic_type:
- apiref
ms.openlocfilehash: 2d274a91948b98dc309cd5670c3dd3bf6cd01e2b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772778"
---
# <a name="clr_debugging_version-structure"></a><span data-ttu-id="cc3c5-103">CLR_DEBUGGING_VERSION 结构</span><span class="sxs-lookup"><span data-stu-id="cc3c5-103">CLR_DEBUGGING_VERSION Structure</span></span>

<span data-ttu-id="cc3c5-104">出于调试目的，定义公共语言运行时 (CLR) 的产品版本。</span><span class="sxs-lookup"><span data-stu-id="cc3c5-104">Defines the product version of the common language runtime (CLR) for debugging purposes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc3c5-105">语法</span><span class="sxs-lookup"><span data-stu-id="cc3c5-105">Syntax</span></span>  
  
```cpp  
typedef struct _CLR_DEBUGGING_VERSION  
{  
    WORD wStructVersion;
    WORD wMajor;
    WORD wMinor;
    WORD wBuild;
    WORD wRevision;
} CLR_DEBUGGING_VERSION;
```  
  
## <a name="members"></a><span data-ttu-id="cc3c5-106">成员</span><span class="sxs-lookup"><span data-stu-id="cc3c5-106">Members</span></span>  
  
|<span data-ttu-id="cc3c5-107">成员</span><span class="sxs-lookup"><span data-stu-id="cc3c5-107">Member</span></span>|<span data-ttu-id="cc3c5-108">说明</span><span class="sxs-lookup"><span data-stu-id="cc3c5-108">Description</span></span>|  
|------------|-----------------|  
|`wStructVersion`|<span data-ttu-id="cc3c5-109">结构版本号</span><span class="sxs-lookup"><span data-stu-id="cc3c5-109">The structure version number</span></span>|  
|`wMajor`|<span data-ttu-id="cc3c5-110">主版本号。</span><span class="sxs-lookup"><span data-stu-id="cc3c5-110">The major version number.</span></span>|  
|`wMinor`|<span data-ttu-id="cc3c5-111">次版本号。</span><span class="sxs-lookup"><span data-stu-id="cc3c5-111">The minor version number.</span></span>|  
|`wBuild`|<span data-ttu-id="cc3c5-112">内部版本号。</span><span class="sxs-lookup"><span data-stu-id="cc3c5-112">The build number.</span></span>|  
|`wRevision`|<span data-ttu-id="cc3c5-113">修订号。</span><span class="sxs-lookup"><span data-stu-id="cc3c5-113">The revision number.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cc3c5-114">备注</span><span class="sxs-lookup"><span data-stu-id="cc3c5-114">Remarks</span></span>  

 <span data-ttu-id="cc3c5-115">`CLR_DEBUGGING_VERSION`结构与 COR_VERSION 结构相同，但 `CLR_DEBUGGING_VERSION` 结构提供了 () 的附加结构版本字段 `wStructVersion` 。</span><span class="sxs-lookup"><span data-stu-id="cc3c5-115">The `CLR_DEBUGGING_VERSION` structure is the same as the COR_VERSION structure, however, the `CLR_DEBUGGING_VERSION` structure provides an additional structure version field (`wStructVersion`).</span></span> <span data-ttu-id="cc3c5-116">此字段当前必须设置为零。</span><span class="sxs-lookup"><span data-stu-id="cc3c5-116">Currently, this field must be set to zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc3c5-117">要求</span><span class="sxs-lookup"><span data-stu-id="cc3c5-117">Requirements</span></span>  

 <span data-ttu-id="cc3c5-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cc3c5-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc3c5-119">**标头：** Cordebug.idl .idl</span><span class="sxs-lookup"><span data-stu-id="cc3c5-119">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="cc3c5-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cc3c5-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cc3c5-121">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cc3c5-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc3c5-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="cc3c5-122">See also</span></span>

- [<span data-ttu-id="cc3c5-123">调试结构</span><span class="sxs-lookup"><span data-stu-id="cc3c5-123">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="cc3c5-124">调试</span><span class="sxs-lookup"><span data-stu-id="cc3c5-124">Debugging</span></span>](index.md)
