---
description: 了解详细信息： CorSaveSize 枚举
title: CorSaveSize 枚举
ms.date: 03/30/2017
api_name:
- CorSaveSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSaveSize
helpviewer_keywords:
- CorSaveSize enumeration [.NET Framework metadata]
ms.assetid: eb95ce39-5688-43c1-a34d-578794b32faa
topic_type:
- apiref
ms.openlocfilehash: 47e2d4d77f58f8f1c2135da5867dfa47cedfd83d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784218"
---
# <a name="corsavesize-enumeration"></a><span data-ttu-id="abcae-103">CorSaveSize 枚举</span><span class="sxs-lookup"><span data-stu-id="abcae-103">CorSaveSize Enumeration</span></span>

<span data-ttu-id="abcae-104">包含一些值，用于指示查询保存操作的大小时所需的精度级别。</span><span class="sxs-lookup"><span data-stu-id="abcae-104">Contains values indicating the level of precision required when querying for the size of a save operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="abcae-105">语法</span><span class="sxs-lookup"><span data-stu-id="abcae-105">Syntax</span></span>  
  
```cpp  
typedef enum CorSaveSize {  
    cssAccurate                = 0x0000,
    cssQuick                   = 0x0001,
    cssDiscardTransientCAs     = 0x0002  
} CorSaveSize;  
```  
  
## <a name="members"></a><span data-ttu-id="abcae-106">成员</span><span class="sxs-lookup"><span data-stu-id="abcae-106">Members</span></span>  
  
|<span data-ttu-id="abcae-107">成员</span><span class="sxs-lookup"><span data-stu-id="abcae-107">Member</span></span>|<span data-ttu-id="abcae-108">说明</span><span class="sxs-lookup"><span data-stu-id="abcae-108">Description</span></span>|  
|------------|-----------------|  
|`cssAccurate`|<span data-ttu-id="abcae-109">指定返回值应是精确的。</span><span class="sxs-lookup"><span data-stu-id="abcae-109">Specifies that the return value should be exact.</span></span>|  
|`cssQuick`|<span data-ttu-id="abcae-110">指定应估算返回值。</span><span class="sxs-lookup"><span data-stu-id="abcae-110">Specifies that the return value should be estimated.</span></span>|  
|`cssDiscardTransientCAs`|<span data-ttu-id="abcae-111">指定应删除可放弃类型。</span><span class="sxs-lookup"><span data-stu-id="abcae-111">Specifies that discardable types should be removed.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="abcae-112">要求</span><span class="sxs-lookup"><span data-stu-id="abcae-112">Requirements</span></span>  

 <span data-ttu-id="abcae-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="abcae-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="abcae-114">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="abcae-114">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="abcae-115">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="abcae-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="abcae-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="abcae-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="abcae-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="abcae-117">See also</span></span>

- [<span data-ttu-id="abcae-118">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="abcae-118">Metadata Enumerations</span></span>](metadata-enumerations.md)
