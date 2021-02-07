---
description: 了解详细信息： COR_FIELD 结构
title: COR_FIELD 结构
ms.date: 03/30/2017
api_name:
- COR_FIELD
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_FIELD
helpviewer_keywords:
- COR_FIELD structure [.NET Framework debugging]
ms.assetid: c0822423-a9df-4961-950d-50dcc152f863
topic_type:
- apiref
ms.openlocfilehash: a3e9dcc2a5c3bb2abae42dab4292c1d285df5ad7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747102"
---
# <a name="cor_field-structure"></a><span data-ttu-id="21b03-103">COR_FIELD 结构</span><span class="sxs-lookup"><span data-stu-id="21b03-103">COR_FIELD Structure</span></span>

<span data-ttu-id="21b03-104">提供有关对象中的某个字段的信息。</span><span class="sxs-lookup"><span data-stu-id="21b03-104">Provides information about a field in an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="21b03-105">语法</span><span class="sxs-lookup"><span data-stu-id="21b03-105">Syntax</span></span>  
  
```cpp  
typedef struct COR_FIELD{  
    mdFieldDef token;  
    ULONG32 offset;  
    COR_TYPEID id;  
    CorElementType fieldType;  
} COR_FIELD;  
```  
  
## <a name="members"></a><span data-ttu-id="21b03-106">成员</span><span class="sxs-lookup"><span data-stu-id="21b03-106">Members</span></span>  
  
|<span data-ttu-id="21b03-107">成员</span><span class="sxs-lookup"><span data-stu-id="21b03-107">Member</span></span>|<span data-ttu-id="21b03-108">说明</span><span class="sxs-lookup"><span data-stu-id="21b03-108">Description</span></span>|  
|------------|-----------------|  
|`token`|<span data-ttu-id="21b03-109">`mdFieldDef`可用于获取字段信息的标记。</span><span class="sxs-lookup"><span data-stu-id="21b03-109">An `mdFieldDef` token that can be used to get field information.</span></span>|  
|`offset`|<span data-ttu-id="21b03-110">对象中字段数据的偏移量（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="21b03-110">The offset, in bytes, to the field data in the object.</span></span>|  
|`id`|<span data-ttu-id="21b03-111">标识此字段的类型的 [COR_TYPEID](cor-typeid-structure.md) 值。</span><span class="sxs-lookup"><span data-stu-id="21b03-111">A [COR_TYPEID](cor-typeid-structure.md) value that identifies the type of this field.</span></span>|  
|`fieldType`|<span data-ttu-id="21b03-112">一个 CorElementType 枚举值，该值指示字段的类型。</span><span class="sxs-lookup"><span data-stu-id="21b03-112">A CorElementType enumeration value that indicates the type of the field.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="21b03-113">备注</span><span class="sxs-lookup"><span data-stu-id="21b03-113">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="21b03-114">要求</span><span class="sxs-lookup"><span data-stu-id="21b03-114">Requirements</span></span>  

 <span data-ttu-id="21b03-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="21b03-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="21b03-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="21b03-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="21b03-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="21b03-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="21b03-118">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="21b03-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="21b03-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="21b03-119">See also</span></span>

- [<span data-ttu-id="21b03-120">调试结构</span><span class="sxs-lookup"><span data-stu-id="21b03-120">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="21b03-121">调试</span><span class="sxs-lookup"><span data-stu-id="21b03-121">Debugging</span></span>](index.md)
