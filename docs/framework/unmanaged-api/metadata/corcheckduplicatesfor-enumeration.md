---
description: 了解详细信息： CorCheckDuplicatesFor 枚举
title: CorCheckDuplicatesFor 枚举
ms.date: 03/30/2017
api_name:
- CorCheckDuplicatesFor
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorCheckDuplicatesFor
helpviewer_keywords:
- CorCheckDuplicatesFor enumeration [.NET Framework metadata]
ms.assetid: d8ec8d3c-70f7-4cc6-9957-68068fd8f49c
topic_type:
- apiref
ms.openlocfilehash: 5649fc6bc66dd282b64fb5064e302a9f77420cd6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678414"
---
# <a name="corcheckduplicatesfor-enumeration"></a><span data-ttu-id="ea707-103">CorCheckDuplicatesFor 枚举</span><span class="sxs-lookup"><span data-stu-id="ea707-103">CorCheckDuplicatesFor Enumeration</span></span>

<span data-ttu-id="ea707-104">指定将检查重复项的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="ea707-104">Specifies the metadata tokens that will be checked for duplicates.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea707-105">语法</span><span class="sxs-lookup"><span data-stu-id="ea707-105">Syntax</span></span>  
  
```cpp  
typedef enum CorCheckDuplicatesFor {  
  
    MDDupAll                    = 0xffffffff,  
    MDDupENC                    = MDDupAll,  
    MDNoDupChecks               = 0x00000000,  
    MDDupTypeDef                = 0x00000001,  
    MDDupInterfaceImpl          = 0x00000002,  
    MDDupMethodDef              = 0x00000004,  
    MDDupTypeRef                = 0x00000008,  
    MDDupMemberRef              = 0x00000010,  
    MDDupCustomAttribute        = 0x00000020,  
    MDDupParamDef               = 0x00000040,  
    MDDupPermission             = 0x00000080,  
    MDDupProperty               = 0x00000100,  
    MDDupEvent                  = 0x00000200,  
    MDDupFieldDef               = 0x00000400,  
    MDDupSignature              = 0x00000800,  
    MDDupModuleRef              = 0x00001000,  
    MDDupTypeSpec               = 0x00002000,  
    MDDupImplMap                = 0x00004000,  
    MDDupAssemblyRef            = 0x00008000,  
    MDDupFile                   = 0x00010000,  
    MDDupExportedType           = 0x00020000,  
    MDDupManifestResource       = 0x00040000,  
    MDDupGenericParam           = 0x00080000,  
    MDDupMethodSpec             = 0x00100000,  
    MDDupGenericParamConstraint = 0x00200000,  
  
    MDDupAssembly               = 0x10000000,  
  
    MDDupDefault =
        MDNoDupChecks | MDDupTypeRef | MDDupMemberRef |
        MDDupSignature | MDDupTypeSpec | MDDupMethodSpec  
  
} CorCheckDuplicatesFor;  
```  
  
## <a name="members"></a><span data-ttu-id="ea707-106">成员</span><span class="sxs-lookup"><span data-stu-id="ea707-106">Members</span></span>  
  
|<span data-ttu-id="ea707-107">成员</span><span class="sxs-lookup"><span data-stu-id="ea707-107">Member</span></span>|<span data-ttu-id="ea707-108">说明</span><span class="sxs-lookup"><span data-stu-id="ea707-108">Description</span></span>|  
|------------|-----------------|  
|`MDDupAll`|<span data-ttu-id="ea707-109">检查所有元数据标记的重复项。</span><span class="sxs-lookup"><span data-stu-id="ea707-109">Check all metadata tokens for duplicates.</span></span>|  
|`MDDupENC`|<span data-ttu-id="ea707-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="ea707-110">Not used.</span></span>|  
|`MDNoDupChecks`|<span data-ttu-id="ea707-111">请勿检查重复项的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="ea707-111">Do not check metadata tokens for duplicates.</span></span>|  
|`MDDupTypeDef`|<span data-ttu-id="ea707-112">检查标记的重复项 `mdTypeDef` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-112">Check for duplicates of `mdTypeDef` tokens.</span></span>|  
|`MDDupInterfaceImpl`|<span data-ttu-id="ea707-113">检查标记的重复项 `mdInterfaceImpl` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-113">Check for duplicates of `mdInterfaceImpl` tokens.</span></span>|  
|`MDDupMethodDef`|<span data-ttu-id="ea707-114">检查标记的重复项 `mdMethodDef` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-114">Check for duplicates of `mdMethodDef` tokens.</span></span>|  
|`MDDupTypeRef`|<span data-ttu-id="ea707-115">检查标记的重复项 `mdTypeRef` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-115">Check for duplicates of `mdTypeRef` tokens.</span></span>|  
|`MDDupMemberRef`|<span data-ttu-id="ea707-116">检查标记的重复项 `mdMemberRef` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-116">Check for duplicates of `mdMemberRef` tokens.</span></span>|  
|`MDDupCustomAttribute`|<span data-ttu-id="ea707-117">检查标记的重复项 `mdCustomAttribute` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-117">Check for duplicates of `mdCustomAttribute` tokens.</span></span>|  
|`MDDupParamDef`|<span data-ttu-id="ea707-118">检查标记的重复项 `mdParamDef` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-118">Check for duplicates of `mdParamDef` tokens.</span></span>|  
|`MDDupPermission`|<span data-ttu-id="ea707-119">检查标记的重复项 `mdPermission` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-119">Check for duplicates of `mdPermission` tokens.</span></span>|  
|`MDDupProperty`|<span data-ttu-id="ea707-120">检查标记的重复项 `mdProperty` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-120">Check for duplicates of `mdProperty` tokens.</span></span>|  
|`MDDupEvent`|<span data-ttu-id="ea707-121">检查标记的重复项 `mdEvent` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-121">Check for duplicates of `mdEvent` tokens.</span></span>|  
|`MDDupFieldDef`|<span data-ttu-id="ea707-122">检查标记的重复项 `mdFieldDef` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-122">Check for duplicates of `mdFieldDef` tokens.</span></span>|  
|`MDDupSignature`|<span data-ttu-id="ea707-123">检查标记的重复项 `mdSignature` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-123">Check for duplicates of `mdSignature` tokens.</span></span>|  
|`MDDupModuleRef`|<span data-ttu-id="ea707-124">检查标记的重复项 `mdModuleRef` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-124">Check for duplicates of `mdModuleRef` tokens.</span></span>|  
|`MDDupTypeSpec`|<span data-ttu-id="ea707-125">检查标记的重复项 `mdTypeSpec` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-125">Check for duplicates of `mdTypeSpec` tokens.</span></span>|  
|`MDDupImplMap`|<span data-ttu-id="ea707-126">检查标记的重复项 `mdImplMap` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-126">Check for duplicates of `mdImplMap` tokens.</span></span>|  
|`MDDupAssemblyRef`|<span data-ttu-id="ea707-127">检查标记的重复项 `mdAssemblyRef` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-127">Check for duplicates of `mdAssemblyRef` tokens.</span></span>|  
|`MDDupFile`|<span data-ttu-id="ea707-128">检查标记的重复项 `mdFile` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-128">Check for duplicates of `mdFile` tokens.</span></span>|  
|`MDDupExportedType`|<span data-ttu-id="ea707-129">检查标记的重复项 `mdExportedType` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-129">Check for duplicates of `mdExportedType` tokens.</span></span>|  
|`MDDupManifestResource`|<span data-ttu-id="ea707-130">检查标记的重复项 `mdManifestResource` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-130">Check for duplicates of `mdManifestResource` tokens.</span></span>|  
|`MDDupGenericParam`|<span data-ttu-id="ea707-131">检查标记的重复项 `mdGenericParam` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-131">Check for duplicates of `mdGenericParam` tokens.</span></span>|  
|`MDDupMethodSpec`|<span data-ttu-id="ea707-132">检查标记的重复项 `mdMethodSpec` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-132">Check for duplicates of `mdMethodSpec` tokens.</span></span>|  
|`MDDupGenericParamConstraint`|<span data-ttu-id="ea707-133">检查标记的重复项 `mdGenericParamConstraint` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-133">Check for duplicates of `mdGenericParamConstraint` tokens.</span></span>|  
|`MDDupAssembly`|<span data-ttu-id="ea707-134">检查标记的重复项 `mdAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-134">Check for duplicates of `mdAssembly` tokens.</span></span>|  
|`MDDupDefault`|<span data-ttu-id="ea707-135">检查、、、 `mdMemberRef` `mdTypeRef` `mdSignature` `mdTypeSpec` 和标记的重复项 `mdMethodSpec` 。</span><span class="sxs-lookup"><span data-stu-id="ea707-135">Check for duplicates of `mdMemberRef`, `mdTypeRef`, `mdSignature`, `mdTypeSpec`, and `mdMethodSpec` tokens.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ea707-136">要求</span><span class="sxs-lookup"><span data-stu-id="ea707-136">Requirements</span></span>  

 <span data-ttu-id="ea707-137">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ea707-137">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ea707-138">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="ea707-138">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="ea707-139">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ea707-139">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ea707-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="ea707-140">See also</span></span>

- [<span data-ttu-id="ea707-141">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="ea707-141">Metadata Enumerations</span></span>](metadata-enumerations.md)
