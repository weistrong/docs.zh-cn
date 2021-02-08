---
description: 了解详细信息： CorNativeLinkType 枚举
title: CorNativeLinkType 枚举
ms.date: 03/30/2017
api_name:
- CorNativeLinkType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorNativeLinkType
helpviewer_keywords:
- CorNativeLinkType enumeration [.NET Framework metadata]
ms.assetid: 4f86ff37-2dab-4e64-819a-76b3bfe828ff
topic_type:
- apiref
ms.openlocfilehash: 40efc75a793da8b024eff3d7c2c620123eca08b2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784335"
---
# <a name="cornativelinktype-enumeration"></a><span data-ttu-id="17ce2-103">CorNativeLinkType 枚举</span><span class="sxs-lookup"><span data-stu-id="17ce2-103">CorNativeLinkType Enumeration</span></span>

<span data-ttu-id="17ce2-104">提供一些值，用于指示本机代码中链接的类型。</span><span class="sxs-lookup"><span data-stu-id="17ce2-104">Provides values that indicate the type linked in native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="17ce2-105">语法</span><span class="sxs-lookup"><span data-stu-id="17ce2-105">Syntax</span></span>  
  
```cpp  
typedef enum
{  
    nltNone       = 1,  
    nltAnsi       = 2,  
    nltUnicode    = 3,  
    nltAuto       = 4,  
    nltOle        = 5,  
    nltMaxValue   = 7  
} CorNativeLinkType;  
```  
  
## <a name="members"></a><span data-ttu-id="17ce2-106">成员</span><span class="sxs-lookup"><span data-stu-id="17ce2-106">Members</span></span>  
  
|<span data-ttu-id="17ce2-107">成员</span><span class="sxs-lookup"><span data-stu-id="17ce2-107">Member</span></span>|<span data-ttu-id="17ce2-108">说明</span><span class="sxs-lookup"><span data-stu-id="17ce2-108">Description</span></span>|  
|------------|-----------------|  
|`nltNone`|<span data-ttu-id="17ce2-109">指示未指定任何关键字。</span><span class="sxs-lookup"><span data-stu-id="17ce2-109">Indicates that none of the keywords are specified.</span></span>|  
|`nltAnsi`|<span data-ttu-id="17ce2-110">指示指定了 ANSI 关键字。</span><span class="sxs-lookup"><span data-stu-id="17ce2-110">Indicates that an ANSI keyword is specified.</span></span>|  
|`nltUnicode`|<span data-ttu-id="17ce2-111">指示指定了 Unicode 关键字</span><span class="sxs-lookup"><span data-stu-id="17ce2-111">Indicates that a Unicode keyword is specified</span></span>|  
|`nltAuto`|<span data-ttu-id="17ce2-112">指示指定了 auto 关键字。</span><span class="sxs-lookup"><span data-stu-id="17ce2-112">Indicates that an auto keyword is specified.</span></span>|  
|`nltOle`|<span data-ttu-id="17ce2-113">指示指定了 OLE 关键字。</span><span class="sxs-lookup"><span data-stu-id="17ce2-113">Indicates that an OLE keyword is specified.</span></span>|  
|`nltMaxValue`|<span data-ttu-id="17ce2-114">未使用。</span><span class="sxs-lookup"><span data-stu-id="17ce2-114">Not used.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="17ce2-115">要求</span><span class="sxs-lookup"><span data-stu-id="17ce2-115">Requirements</span></span>  

 <span data-ttu-id="17ce2-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="17ce2-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="17ce2-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="17ce2-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="17ce2-118">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="17ce2-118">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="17ce2-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="17ce2-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="17ce2-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="17ce2-120">See also</span></span>

- [<span data-ttu-id="17ce2-121">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="17ce2-121">Metadata Enumerations</span></span>](metadata-enumerations.md)
