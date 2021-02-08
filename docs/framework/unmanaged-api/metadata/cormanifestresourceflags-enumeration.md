---
description: 了解详细信息： CorManifestResourceFlags 枚举
title: CorManifestResourceFlags 枚举
ms.date: 03/30/2017
api_name:
- CorManifestResourceFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorManifestResourceFlags
helpviewer_keywords:
- CorManifestResourceFlags enumeration [.NET Framework metadata]
ms.assetid: 1b0306b7-622b-4b57-8edc-3c713bb147ae
topic_type:
- apiref
ms.openlocfilehash: a863e1248bf5274e12fc16d2edea6b28dd493963
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784400"
---
# <a name="cormanifestresourceflags-enumeration"></a><span data-ttu-id="11a44-103">CorManifestResourceFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="11a44-103">CorManifestResourceFlags Enumeration</span></span>

<span data-ttu-id="11a44-104">指示程序集清单中编码的资源的可见性。</span><span class="sxs-lookup"><span data-stu-id="11a44-104">Indicates the visibility of resources encoded in an assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="11a44-105">语法</span><span class="sxs-lookup"><span data-stu-id="11a44-105">Syntax</span></span>  
  
```cpp  
typedef enum CorManifestResourceFlags {  
  
    mrVisibilityMask        =   0x0007,  
    mrPublic                =   0x0001,  
    mrPrivate               =   0x0002  
  
} CorManifestResourceFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="11a44-106">成员</span><span class="sxs-lookup"><span data-stu-id="11a44-106">Members</span></span>  
  
|<span data-ttu-id="11a44-107">成员</span><span class="sxs-lookup"><span data-stu-id="11a44-107">Member</span></span>|<span data-ttu-id="11a44-108">说明</span><span class="sxs-lookup"><span data-stu-id="11a44-108">Description</span></span>|  
|------------|-----------------|  
|`mrVisibilityMask`|<span data-ttu-id="11a44-109">保留。</span><span class="sxs-lookup"><span data-stu-id="11a44-109">Reserved.</span></span>|  
|`mrPublic`|<span data-ttu-id="11a44-110">资源是公共的。</span><span class="sxs-lookup"><span data-stu-id="11a44-110">The resources are public.</span></span>|  
|`mrPrivate`|<span data-ttu-id="11a44-111">资源是专用的。</span><span class="sxs-lookup"><span data-stu-id="11a44-111">The resources are private.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="11a44-112">要求</span><span class="sxs-lookup"><span data-stu-id="11a44-112">Requirements</span></span>  

 <span data-ttu-id="11a44-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="11a44-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="11a44-114">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="11a44-114">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="11a44-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="11a44-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="11a44-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="11a44-116">See also</span></span>

- [<span data-ttu-id="11a44-117">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="11a44-117">Metadata Enumerations</span></span>](metadata-enumerations.md)
