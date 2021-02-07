---
description: 了解详细信息： COR_FIELD_OFFSET 结构
title: COR_FIELD_OFFSET 结构
ms.date: 03/30/2017
api_name:
- COR_FIELD_OFFSET
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_FIELD_OFFSET
helpviewer_keywords:
- COR_FIELD_OFFSET structure [.NET Framework metadata]
ms.assetid: cced5298-277f-4a5a-8ecf-a0050c1096ea
topic_type:
- apiref
ms.openlocfilehash: 7976e79a5484fa467d7ac887a4e1a7fa324abf69
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678622"
---
# <a name="cor_field_offset-structure"></a><span data-ttu-id="3df75-103">COR_FIELD_OFFSET 结构</span><span class="sxs-lookup"><span data-stu-id="3df75-103">COR_FIELD_OFFSET Structure</span></span>

<span data-ttu-id="3df75-104">存储一个类中的指定字段的偏移量。</span><span class="sxs-lookup"><span data-stu-id="3df75-104">Stores the offset, within a class, of the specified field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3df75-105">语法</span><span class="sxs-lookup"><span data-stu-id="3df75-105">Syntax</span></span>  
  
```cpp  
typedef struct COR_FIELD_OFFSET {  
    mdFieldDef  ridOfField;  
    ULONG       ulOffset;  
} COR_FIELD_OFFSET;  
```  
  
## <a name="members"></a><span data-ttu-id="3df75-106">成员</span><span class="sxs-lookup"><span data-stu-id="3df75-106">Members</span></span>  
  
|<span data-ttu-id="3df75-107">成员</span><span class="sxs-lookup"><span data-stu-id="3df75-107">Member</span></span>|<span data-ttu-id="3df75-108">说明</span><span class="sxs-lookup"><span data-stu-id="3df75-108">Description</span></span>|  
|------------|-----------------|  
|`ridOfField`|<span data-ttu-id="3df75-109">`mdFieldDef`表示字段的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="3df75-109">An `mdFieldDef` metadata token that represents the field.</span></span>|  
|`ulOffset`|<span data-ttu-id="3df75-110">字段在其类中的偏移量。</span><span class="sxs-lookup"><span data-stu-id="3df75-110">The field's offset within its class.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3df75-111">备注</span><span class="sxs-lookup"><span data-stu-id="3df75-111">Remarks</span></span>  

 <span data-ttu-id="3df75-112">[IMetaDataImport：： GetClassLayout](imetadataimport-getclasslayout-method.md) 和 [IMetaDataEmit：： SetClassLayout](imetadataemit-setclasslayout-method.md) 方法采用类型的参数 `COR_FIELD_OFFSET` 。</span><span class="sxs-lookup"><span data-stu-id="3df75-112">[IMetaDataImport::GetClassLayout](imetadataimport-getclasslayout-method.md) and [IMetaDataEmit::SetClassLayout](imetadataemit-setclasslayout-method.md) methods take a parameter of type `COR_FIELD_OFFSET`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3df75-113">要求</span><span class="sxs-lookup"><span data-stu-id="3df75-113">Requirements</span></span>  

 <span data-ttu-id="3df75-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3df75-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3df75-115">**标头：** Corhdr.h，Corprof.idl</span><span class="sxs-lookup"><span data-stu-id="3df75-115">**Header:** CorHdr.h, CorProf.idl</span></span>  
  
 <span data-ttu-id="3df75-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3df75-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3df75-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="3df75-117">See also</span></span>

- [<span data-ttu-id="3df75-118">元数据结构</span><span class="sxs-lookup"><span data-stu-id="3df75-118">Metadata Structures</span></span>](metadata-structures.md)
- [<span data-ttu-id="3df75-119">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="3df75-119">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="3df75-120">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="3df75-120">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
