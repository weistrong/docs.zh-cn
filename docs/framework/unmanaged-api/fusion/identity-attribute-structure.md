---
description: 了解详细信息： IDENTITY_ATTRIBUTE 结构
title: IDENTITY_ATTRIBUTE 结构
ms.date: 03/30/2017
api_name:
- IDENTITY_ATTRIBUTE
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IDENTITY_ATTRIBUTE
helpviewer_keywords:
- IDENTITY_ATTRIBUTE structure [.NET Framework fusion]
ms.assetid: 1ee7c434-9681-4fa8-badd-652cb1a9742b
topic_type:
- apiref
ms.openlocfilehash: 52610961ab202fc79351073eac1846a1a63889e3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800170"
---
# <a name="identity_attribute-structure"></a><span data-ttu-id="e2d72-103">IDENTITY_ATTRIBUTE 结构</span><span class="sxs-lookup"><span data-stu-id="e2d72-103">IDENTITY_ATTRIBUTE Structure</span></span>

<span data-ttu-id="e2d72-104">包含有关 [IDefinitionIdentity](idefinitionidentity-interface.md) 实例的元数据属性信息。</span><span class="sxs-lookup"><span data-stu-id="e2d72-104">Contains metadata attribute information about an [IDefinitionIdentity](idefinitionidentity-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2d72-105">语法</span><span class="sxs-lookup"><span data-stu-id="e2d72-105">Syntax</span></span>  
  
```cpp  
typedef struct _IDENTITY_ATTRIBUTE {  
    LPCWSTR  pszNamespace;  
    LPCWSTR  pszName;  
    LPCWSTR  pszValue;  
} IDENTITY_ATTRIBUTE;  
```  
  
## <a name="members"></a><span data-ttu-id="e2d72-106">成员</span><span class="sxs-lookup"><span data-stu-id="e2d72-106">Members</span></span>  
  
|<span data-ttu-id="e2d72-107">成员</span><span class="sxs-lookup"><span data-stu-id="e2d72-107">Member</span></span>|<span data-ttu-id="e2d72-108">说明</span><span class="sxs-lookup"><span data-stu-id="e2d72-108">Description</span></span>|  
|------------|-----------------|  
|`pszNamespace`|<span data-ttu-id="e2d72-109">指向以 null 结尾的字符串的指针，该字符串包含特性所在的命名空间。</span><span class="sxs-lookup"><span data-stu-id="e2d72-109">A pointer to a null-terminated character string that contains the namespace the attribute is in.</span></span>|  
|`pszName`|<span data-ttu-id="e2d72-110">指向以 null 结尾的字符串的指针，该字符串包含属性的名称。</span><span class="sxs-lookup"><span data-stu-id="e2d72-110">A pointer to a null-terminated character string that contains the name of the attribute.</span></span>|  
|`pszValue`|<span data-ttu-id="e2d72-111">指向以 null 结尾的字符串的指针，该字符串包含属性的值。</span><span class="sxs-lookup"><span data-stu-id="e2d72-111">A pointer to a null-terminated character string that contains the value of the attribute.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e2d72-112">备注</span><span class="sxs-lookup"><span data-stu-id="e2d72-112">Remarks</span></span>  

 <span data-ttu-id="e2d72-113">该 `IDENTITY_ATTRIBUTE` 结构包含三个指向以 null 结尾的字符串的指针。</span><span class="sxs-lookup"><span data-stu-id="e2d72-113">The `IDENTITY_ATTRIBUTE` structure contains three pointers to null-terminated character strings.</span></span> <span data-ttu-id="e2d72-114">这三个字符串描述了一个属性。</span><span class="sxs-lookup"><span data-stu-id="e2d72-114">These three strings describe one attribute.</span></span>  
  
 <span data-ttu-id="e2d72-115">结构的实例 `IDENTITY_ATTRIBUTE` 与 [IDENTITY_ATTRIBUTE_BLOB](identity-attribute-blob-structure.md) 结构的实例相关联。</span><span class="sxs-lookup"><span data-stu-id="e2d72-115">An instance of an `IDENTITY_ATTRIBUTE` structure is associated with an instance of an [IDENTITY_ATTRIBUTE_BLOB](identity-attribute-blob-structure.md) structure.</span></span> <span data-ttu-id="e2d72-116">`IDENTITY_ATTRIBUTE`结构包含实际的字符串，相应的 `IDENTITY_ATTRIBUTE_BLOB` 结构列出了结构中列出的三个字符串的偏移量 `IDENTITY_ATTRIBUTE` 。</span><span class="sxs-lookup"><span data-stu-id="e2d72-116">The `IDENTITY_ATTRIBUTE` structure contains the actual strings, and the corresponding `IDENTITY_ATTRIBUTE_BLOB` structure lists the offsets to the three strings listed in the `IDENTITY_ATTRIBUTE` structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e2d72-117">要求</span><span class="sxs-lookup"><span data-stu-id="e2d72-117">Requirements</span></span>  

 <span data-ttu-id="e2d72-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e2d72-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e2d72-119">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="e2d72-119">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="e2d72-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e2d72-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2d72-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="e2d72-121">See also</span></span>

- [<span data-ttu-id="e2d72-122">IDefinitionIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="e2d72-122">IDefinitionIdentity Interface</span></span>](idefinitionidentity-interface.md)
- [<span data-ttu-id="e2d72-123">IDENTITY_ATTRIBUTE_BLOB 结构</span><span class="sxs-lookup"><span data-stu-id="e2d72-123">IDENTITY_ATTRIBUTE_BLOB Structure</span></span>](identity-attribute-blob-structure.md)
- [<span data-ttu-id="e2d72-124">合成结构</span><span class="sxs-lookup"><span data-stu-id="e2d72-124">Fusion Structures</span></span>](fusion-structures.md)
