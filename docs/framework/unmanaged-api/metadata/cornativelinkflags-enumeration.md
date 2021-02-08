---
description: 了解详细信息： CorNativeLinkFlags 枚举
title: CorNativeLinkFlags 枚举
ms.date: 03/30/2017
api_name:
- CorNativeLinkFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorNativeLinkFlags
helpviewer_keywords:
- CorNativeLinkFlags enumeration [.NET Framework metadata]
ms.assetid: 8027df7c-cfad-4724-bda0-7538d9519070
topic_type:
- apiref
ms.openlocfilehash: 9025d192ca92c1160c1b072b0dcfe045fa3ceab7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784348"
---
# <a name="cornativelinkflags-enumeration"></a><span data-ttu-id="ab019-103">CorNativeLinkFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="ab019-103">CorNativeLinkFlags Enumeration</span></span>

<span data-ttu-id="ab019-104">提供链接本机代码时链接器使用的标志值。</span><span class="sxs-lookup"><span data-stu-id="ab019-104">Provides flag values used by the linker when linking native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab019-105">语法</span><span class="sxs-lookup"><span data-stu-id="ab019-105">Syntax</span></span>  
  
```cpp  
typedef enum  
{  
    nlfNone         = 0x00,  
    nlfLastError    = 0x01,  
    nlfNoMangle     = 0x02,  
    nlfMaxValue     = 0x03  
} CorNativeLinkFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="ab019-106">成员</span><span class="sxs-lookup"><span data-stu-id="ab019-106">Members</span></span>  
  
|<span data-ttu-id="ab019-107">成员</span><span class="sxs-lookup"><span data-stu-id="ab019-107">Member</span></span>|<span data-ttu-id="ab019-108">说明</span><span class="sxs-lookup"><span data-stu-id="ab019-108">Description</span></span>|  
|------------|-----------------|  
|`nlfNone`|<span data-ttu-id="ab019-109">指示无标志。</span><span class="sxs-lookup"><span data-stu-id="ab019-109">Indicates no flags.</span></span>|  
|`nlfLastError`|<span data-ttu-id="ab019-110">指示 `setLastError` 关键字。</span><span class="sxs-lookup"><span data-stu-id="ab019-110">Indicates a `setLastError` keyword.</span></span>|  
|`nlfNoMangle`|<span data-ttu-id="ab019-111">指示 `nomangle` 关键字。</span><span class="sxs-lookup"><span data-stu-id="ab019-111">Indicates a `nomangle` keyword.</span></span>|  
|`nlfMaxValue`|<span data-ttu-id="ab019-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="ab019-112">Not used.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ab019-113">要求</span><span class="sxs-lookup"><span data-stu-id="ab019-113">Requirements</span></span>  

 <span data-ttu-id="ab019-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ab019-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab019-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="ab019-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ab019-116">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ab019-116">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ab019-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ab019-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab019-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="ab019-118">See also</span></span>

- [<span data-ttu-id="ab019-119">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="ab019-119">Metadata Enumerations</span></span>](metadata-enumerations.md)
