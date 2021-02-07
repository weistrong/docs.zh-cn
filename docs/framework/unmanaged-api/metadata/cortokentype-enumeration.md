---
description: 了解详细信息： CorTokenType 枚举
title: CorTokenType 枚举
ms.date: 03/30/2017
api_name:
- CorTokenType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorTokenType
helpviewer_keywords:
- CorTokenType enumeration [.NET Framework metadata]
ms.assetid: 93c9a369-225f-4eff-9b78-3fbee4902cf1
topic_type:
- apiref
ms.openlocfilehash: 954bddccd8fe20be46080f8843bcf754e0cf1bbb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678401"
---
# <a name="cortokentype-enumeration"></a><span data-ttu-id="ec906-103">CorTokenType 枚举</span><span class="sxs-lookup"><span data-stu-id="ec906-103">CorTokenType Enumeration</span></span>

<span data-ttu-id="ec906-104">指示元数据标记的类型。</span><span class="sxs-lookup"><span data-stu-id="ec906-104">Indicates the type of a metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec906-105">语法</span><span class="sxs-lookup"><span data-stu-id="ec906-105">Syntax</span></span>  
  
```cpp  
typedef enum CorTokenType {  
  
    mdtModule                       = 0x00000000,  
    mdtTypeRef                      = 0x01000000,  
    mdtTypeDef                      = 0x02000000,  
    mdtFieldDef                     = 0x04000000,  
    mdtMethodDef                    = 0x06000000,  
    mdtParamDef                     = 0x08000000,  
    mdtInterfaceImpl                = 0x09000000,  
    mdtMemberRef                    = 0x0a000000,  
    mdtCustomAttribute              = 0x0c000000,  
    mdtPermission                   = 0x0e000000,  
    mdtSignature                    = 0x11000000,  
    mdtEvent                        = 0x14000000,  
    mdtProperty                     = 0x17000000,  
    mdtModuleRef                    = 0x1a000000,  
    mdtTypeSpec                     = 0x1b000000,  
    mdtAssembly                     = 0x20000000,  
    mdtAssemblyRef                  = 0x23000000,  
    mdtFile                         = 0x26000000,  
    mdtExportedType                 = 0x27000000,  
    mdtManifestResource             = 0x28000000,  
    mdtGenericParam                 = 0x2a000000,  
    mdtMethodSpec                   = 0x2b000000,  
    mdtGenericParamConstraint       = 0x2c000000,  
    mdtString                       = 0x70000000,  
    mdtName                         = 0x71000000,  
    mdtBaseType                     = 0x72000000  
  
} CorTokenType;  
```  
  
## <a name="members"></a><span data-ttu-id="ec906-106">成员</span><span class="sxs-lookup"><span data-stu-id="ec906-106">Members</span></span>  
  
|<span data-ttu-id="ec906-107">成员</span><span class="sxs-lookup"><span data-stu-id="ec906-107">Member</span></span>|<span data-ttu-id="ec906-108">说明</span><span class="sxs-lookup"><span data-stu-id="ec906-108">Description</span></span>|  
|------------|-----------------|  
|`mdtModule`|<span data-ttu-id="ec906-109">`mdModule`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-109">An `mdModule` token.</span></span>|  
|`mdtTypeRef`|<span data-ttu-id="ec906-110">`mdTypeRef`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-110">An `mdTypeRef` token.</span></span>|  
|`mdtTypeDef`|<span data-ttu-id="ec906-111">`mdTypeDef`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-111">An `mdTypeDef` token.</span></span>|  
|`mdtFieldDef`|<span data-ttu-id="ec906-112">`mdFieldDef`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-112">An `mdFieldDef` token.</span></span>|  
|`mdtMethodDef`|<span data-ttu-id="ec906-113">`mdMethodDef`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-113">An `mdMethodDef` token.</span></span>|  
|`mdtParamDef`|<span data-ttu-id="ec906-114">`mdParamDef`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-114">An `mdParamDef` token.</span></span>|  
|`mdtInterfaceImpl`|<span data-ttu-id="ec906-115">`mdInterfaceImpl`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-115">An `mdInterfaceImpl` token.</span></span>|  
|`mdtMemberRef`|<span data-ttu-id="ec906-116">`mdMemberRef`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-116">An `mdMemberRef` token.</span></span>|  
|`mdtCustomAttribute`|<span data-ttu-id="ec906-117">`mdCustomAttribute`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-117">An `mdCustomAttribute` token.</span></span>|  
|`mdtPermission`|<span data-ttu-id="ec906-118">`mdPermission`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-118">An `mdPermission` token.</span></span>|  
|`mdtSignature`|<span data-ttu-id="ec906-119">`mdSignature`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-119">An `mdSignature` token.</span></span>|  
|`mdtEvent`|<span data-ttu-id="ec906-120">`mdEvent`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-120">An `mdEvent` token.</span></span>|  
|`mdtProperty`|<span data-ttu-id="ec906-121">`mdProperty`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-121">An `mdProperty` token.</span></span>|  
|`mdtModuleRef`|<span data-ttu-id="ec906-122">`mdModuleRef`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-122">An `mdModuleRef` token.</span></span>|  
|`mdtTypeSpec`|<span data-ttu-id="ec906-123">`mdTypeSpec`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-123">An `mdTypeSpec` token.</span></span>|  
|`mdtAssembly`|<span data-ttu-id="ec906-124">`mdAssembly`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-124">An `mdAssembly` token.</span></span>|  
|`mdtAssemblyRef`|<span data-ttu-id="ec906-125">`mdAssemblyRef`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-125">An `mdAssemblyRef` token.</span></span>|  
|`mdtFile`|<span data-ttu-id="ec906-126">`mdFile`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-126">An `mdFile` token.</span></span>|  
|`mdtExportedType`|<span data-ttu-id="ec906-127">`mdExportedType`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-127">An `mdExportedType` token.</span></span>|  
|`mdtManifestResource`|<span data-ttu-id="ec906-128">`mdManifestResource`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-128">An `mdManifestResource` token.</span></span>|  
|`mdtGenericParam`|<span data-ttu-id="ec906-129">`mdGenericParam`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-129">An `mdGenericParam` token.</span></span>|  
|`mdtMethodSpec`|<span data-ttu-id="ec906-130">`mdMethodSpec`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-130">An `mdMethodSpec` token.</span></span>|  
|`mdtGenericParamConstraint`|<span data-ttu-id="ec906-131">`mdGenericParamConstraint`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-131">An `mdGenericParamConstraint` token.</span></span>|  
|`mdtString`|<span data-ttu-id="ec906-132">`mdString`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-132">An `mdString` token.</span></span>|  
|`mdtName`|<span data-ttu-id="ec906-133">`mdName`标记。</span><span class="sxs-lookup"><span data-stu-id="ec906-133">An `mdName` token.</span></span>|  
|`mdtBaseType`|<span data-ttu-id="ec906-134">未使用。</span><span class="sxs-lookup"><span data-stu-id="ec906-134">Not used.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ec906-135">备注</span><span class="sxs-lookup"><span data-stu-id="ec906-135">Remarks</span></span>  

 <span data-ttu-id="ec906-136">每个值都等于对应的元数据标记中的顶部字节的值。</span><span class="sxs-lookup"><span data-stu-id="ec906-136">Each value is equal to the value of the top byte in the corresponding metadata token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ec906-137">要求</span><span class="sxs-lookup"><span data-stu-id="ec906-137">Requirements</span></span>  

 <span data-ttu-id="ec906-138">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ec906-138">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec906-139">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="ec906-139">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="ec906-140">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ec906-140">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec906-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="ec906-141">See also</span></span>

- [<span data-ttu-id="ec906-142">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="ec906-142">Metadata Enumerations</span></span>](metadata-enumerations.md)
