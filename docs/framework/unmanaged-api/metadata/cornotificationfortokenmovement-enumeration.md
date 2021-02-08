---
description: 了解详细信息： CorNotificationForTokenMovement 枚举
title: CorNotificationForTokenMovement 枚举
ms.date: 03/30/2017
api_name:
- CorNotificationForTokenMovement
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorNotificationForTokenMovement
helpviewer_keywords:
- CorNotificationForTokenMovement enumeration [.NET Framework metadata]
ms.assetid: 1edd1670-976a-4fc8-bef7-7c41e60ad989
topic_type:
- apiref
ms.openlocfilehash: 1975598b756499c9c0b017bf7eba9a134af5185f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784309"
---
# <a name="cornotificationfortokenmovement-enumeration"></a><span data-ttu-id="49064-103">CorNotificationForTokenMovement 枚举</span><span class="sxs-lookup"><span data-stu-id="49064-103">CorNotificationForTokenMovement Enumeration</span></span>

<span data-ttu-id="49064-104">指定在进行标记重新映射时将发送到元数据 API 客户端的通知。</span><span class="sxs-lookup"><span data-stu-id="49064-104">Specifies the notifications that will be sent to the metadata API client when a token remap occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49064-105">语法</span><span class="sxs-lookup"><span data-stu-id="49064-105">Syntax</span></span>  
  
```cpp  
typedef enum CorNotificationForTokenMovement {  
  
    MDNotifyDefault             = 0x0000000f,  
    MDNotifyAll                 = 0xffffffff,  
    MDNotifyNone                = 0x00000000,  
    MDNotifyMethodDef           = 0x00000001,  
    MDNotifyMemberRef           = 0x00000002,  
    MDNotifyFieldDef            = 0x00000004,  
    MDNotifyTypeRef             = 0x00000008,  
  
    MDNotifyTypeDef             = 0x00000010,  
    MDNotifyParamDef            = 0x00000020,  
    MDNotifyInterfaceImpl       = 0x00000040,  
    MDNotifyProperty            = 0x00000080,  
    MDNotifyEvent               = 0x00000100,  
    MDNotifySignature           = 0x00000200,  
    MDNotifyTypeSpec            = 0x00000400,  
    MDNotifyCustomAttribute     = 0x00000800,  
    MDNotifySecurityValue       = 0x00001000,  
    MDNotifyPermission          = 0x00002000,  
    MDNotifyModuleRef           = 0x00004000,  
  
    MDNotifyNameSpace           = 0x00008000,  
  
    MDNotifyAssemblyRef         = 0x01000000,  
    MDNotifyFile                = 0x02000000,  
    MDNotifyExportedType        = 0x04000000,  
    MDNotifyResource            = 0x08000000  
  
} CorNotificationForTokenMovement;  
```  
  
## <a name="members"></a><span data-ttu-id="49064-106">成员</span><span class="sxs-lookup"><span data-stu-id="49064-106">Members</span></span>  
  
|<span data-ttu-id="49064-107">成员</span><span class="sxs-lookup"><span data-stu-id="49064-107">Member</span></span>|<span data-ttu-id="49064-108">说明</span><span class="sxs-lookup"><span data-stu-id="49064-108">Description</span></span>|  
|------------|-----------------|  
|`MDNotifyDefault`|<span data-ttu-id="49064-109">当 `mdTypeRef` 、、 `mdMethodDef` `mdMemberRef` 或 `mdFieldDef` 标记移动时通知。</span><span class="sxs-lookup"><span data-stu-id="49064-109">Notify when `mdTypeRef`, `mdMethodDef`, `mdMemberRef`, or `mdFieldDef` tokens move.</span></span>|  
|`MDNotifyAll`|<span data-ttu-id="49064-110">任何标记移动时发出通知。</span><span class="sxs-lookup"><span data-stu-id="49064-110">Notify when any token moves.</span></span>|  
|`MDNotifyNone`|<span data-ttu-id="49064-111">标记移动时不发出通知。</span><span class="sxs-lookup"><span data-stu-id="49064-111">Do not notify when tokens move.</span></span>|  
|`MDNotifyMethodDef`|<span data-ttu-id="49064-112">移动令牌时发出通知 `mdMethodDef` 。</span><span class="sxs-lookup"><span data-stu-id="49064-112">Notify when an `mdMethodDef` token moves.</span></span>|  
|`MDNotifyMemberRef`|<span data-ttu-id="49064-113">移动令牌时发出通知 `mdMemberRef` 。</span><span class="sxs-lookup"><span data-stu-id="49064-113">Notify when an `mdMemberRef` token moves.</span></span>|  
|`MDNotifyFieldDef`|<span data-ttu-id="49064-114">移动令牌时发出通知 `mdFieldDef` 。</span><span class="sxs-lookup"><span data-stu-id="49064-114">Notify when an `mdFieldDef` token moves.</span></span>|  
|`MDNotifyTypeRef`|<span data-ttu-id="49064-115">移动令牌时发出通知 `mdTypeRef` 。</span><span class="sxs-lookup"><span data-stu-id="49064-115">Notify when an `mdTypeRef` token moves.</span></span>|  
|`MDNotifyTypeDef`|<span data-ttu-id="49064-116">移动令牌时发出通知 `mdTypeDef` 。</span><span class="sxs-lookup"><span data-stu-id="49064-116">Notify when an `mdTypeDef` token moves.</span></span>|  
|`MDNotifyParamDef`|<span data-ttu-id="49064-117">移动令牌时发出通知 `mdParamDef` 。</span><span class="sxs-lookup"><span data-stu-id="49064-117">Notify when an `mdParamDef` token moves.</span></span>|  
|`MDNotifyInterfaceImpl`|<span data-ttu-id="49064-118">移动令牌时发出通知 `mdInterfaceImpl` 。</span><span class="sxs-lookup"><span data-stu-id="49064-118">Notify when an `mdInterfaceImpl` token moves.</span></span>|  
|`MDNotifyProperty`|<span data-ttu-id="49064-119">移动令牌时发出通知 `mdProperty` 。</span><span class="sxs-lookup"><span data-stu-id="49064-119">Notify when an `mdProperty` token moves.</span></span>|  
|`MDNotifyEvent`|<span data-ttu-id="49064-120">移动令牌时发出通知 `mdEvent` 。</span><span class="sxs-lookup"><span data-stu-id="49064-120">Notify when an `mdEvent` token moves.</span></span>|  
|`MDNotifySignature`|<span data-ttu-id="49064-121">移动令牌时发出通知 `mdSignature` 。</span><span class="sxs-lookup"><span data-stu-id="49064-121">Notify when an `mdSignature` token moves.</span></span>|  
|`MDNotifyTypeSpec`|<span data-ttu-id="49064-122">移动令牌时发出通知 `mdTypeSpec` 。</span><span class="sxs-lookup"><span data-stu-id="49064-122">Notify when an `mdTypeSpec` token moves.</span></span>|  
|`MDNotifyCustomAttribute`|<span data-ttu-id="49064-123">移动令牌时发出通知 `mdCustomAttribute` 。</span><span class="sxs-lookup"><span data-stu-id="49064-123">Notify when an `mdCustomAttribute` token moves.</span></span>|  
|`MDNotifySecurityValue`|<span data-ttu-id="49064-124">移动令牌时发出通知 `mdSecurityValue` 。</span><span class="sxs-lookup"><span data-stu-id="49064-124">Notify when an `mdSecurityValue` token moves.</span></span>|  
|`MDNotifyPermission`|<span data-ttu-id="49064-125">移动令牌时发出通知 `mdPermission` 。</span><span class="sxs-lookup"><span data-stu-id="49064-125">Notify when an `mdPermission` token moves.</span></span>|  
|`MDNotifyModuleRef`|<span data-ttu-id="49064-126">移动令牌时发出通知 `mdModuleRef` 。</span><span class="sxs-lookup"><span data-stu-id="49064-126">Notify when an `mdModuleRef` token moves.</span></span>|  
|`MDNotifyNameSpace`|<span data-ttu-id="49064-127">移动令牌时发出通知 `mdNameSpace` 。</span><span class="sxs-lookup"><span data-stu-id="49064-127">Notify when an `mdNameSpace` token moves.</span></span>|  
|`MDNotifyAssemblyRef`|<span data-ttu-id="49064-128">移动令牌时发出通知 `mdAssemblyRef` 。</span><span class="sxs-lookup"><span data-stu-id="49064-128">Notify when an `mdAssemblyRef` token moves.</span></span>|  
|`MDNotifyFile`|<span data-ttu-id="49064-129">移动令牌时发出通知 `mdFile` 。</span><span class="sxs-lookup"><span data-stu-id="49064-129">Notify when an `mdFile` token moves.</span></span>|  
|`MDNotifyExportedType`|<span data-ttu-id="49064-130">移动令牌时发出通知 `mdExportedType` 。</span><span class="sxs-lookup"><span data-stu-id="49064-130">Notify when an `mdExportedType` token moves.</span></span>|  
|`MDNotifyResource`|<span data-ttu-id="49064-131">移动令牌时发出通知 `mdManifestResource` 。</span><span class="sxs-lookup"><span data-stu-id="49064-131">Notify when an `mdManifestResource` token moves.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="49064-132">备注</span><span class="sxs-lookup"><span data-stu-id="49064-132">Remarks</span></span>  

 <span data-ttu-id="49064-133">标记可以重新映射 (即，在元数据合并期间移动) 。</span><span class="sxs-lookup"><span data-stu-id="49064-133">A token may be re-mapped (that is, moved) during a metadata merge.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="49064-134">要求</span><span class="sxs-lookup"><span data-stu-id="49064-134">Requirements</span></span>  

 <span data-ttu-id="49064-135">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="49064-135">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="49064-136">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="49064-136">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="49064-137">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="49064-137">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49064-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="49064-138">See also</span></span>

- [<span data-ttu-id="49064-139">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="49064-139">Metadata Enumerations</span></span>](metadata-enumerations.md)
