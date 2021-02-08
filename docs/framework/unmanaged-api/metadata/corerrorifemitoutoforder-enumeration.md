---
description: 了解详细信息： CorErrorIfEmitOutOfOrder 枚举
title: CorErrorIfEmitOutOfOrder 枚举
ms.date: 03/30/2017
api_name:
- CorErrorIfEmitOutOfOrder
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorErrorIfEmitOutOfOrder
helpviewer_keywords:
- CorErrorIfEmitOutOfOrder enumeration [.NET Framework metadata]
ms.assetid: 6d758aad-29a7-44fe-9481-bbff5b799a32
topic_type:
- apiref
ms.openlocfilehash: b45d3204ae386b7ad9d7ab1daccdfdef35e2ad9e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784517"
---
# <a name="corerrorifemitoutoforder-enumeration"></a><span data-ttu-id="e0b64-103">CorErrorIfEmitOutOfOrder 枚举</span><span class="sxs-lookup"><span data-stu-id="e0b64-103">CorErrorIfEmitOutOfOrder Enumeration</span></span>

<span data-ttu-id="e0b64-104">包含一些标志值，用于指示无序发出元数据时应生成错误消息的条件。</span><span class="sxs-lookup"><span data-stu-id="e0b64-104">Contains flag values that indicate the conditions under which an error message should be generated when metadata is emitted out of order.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0b64-105">语法</span><span class="sxs-lookup"><span data-stu-id="e0b64-105">Syntax</span></span>  
  
```cpp  
typedef enum CorErrorIfEmitOutOfOrder {  
  
    MDErrorOutOfOrderDefault    = 0x00000000,  
    MDErrorOutOfOrderNone       = 0x00000000,  
    MDErrorOutOfOrderAll        = 0xffffffff,  
    MDMethodOutOfOrder          = 0x00000001,  
    MDFieldOutOfOrder           = 0x00000002,  
    MDParamOutOfOrder           = 0x00000004,  
    MDPropertyOutOfOrder        = 0x00000008,  
    MDEventOutOfOrder           = 0x00000010  
  
} CorErrorIfEmitOutOfOrder;  
```  
  
## <a name="members"></a><span data-ttu-id="e0b64-106">成员</span><span class="sxs-lookup"><span data-stu-id="e0b64-106">Members</span></span>  
  
|<span data-ttu-id="e0b64-107">成员</span><span class="sxs-lookup"><span data-stu-id="e0b64-107">Member</span></span>|<span data-ttu-id="e0b64-108">说明</span><span class="sxs-lookup"><span data-stu-id="e0b64-108">Description</span></span>|  
|------------|-----------------|  
|`MDErrorOutOfOrderDefault`|<span data-ttu-id="e0b64-109">指示默认行为，不会生成错误消息。</span><span class="sxs-lookup"><span data-stu-id="e0b64-109">Indicates the default behavior, which does not generate error messages.</span></span>|  
|`MDErrorOutOfOrderNone`|<span data-ttu-id="e0b64-110">指示编译器不应生成错误消息。</span><span class="sxs-lookup"><span data-stu-id="e0b64-110">Indicates that the compiler should not generate error messages.</span></span>|  
|`MDErrorOutOfOrderAll`|<span data-ttu-id="e0b64-111">指示当字段、属性、事件、方法或参数的顺序发出时，编译器应生成错误消息。</span><span class="sxs-lookup"><span data-stu-id="e0b64-111">Indicates that the compiler should generate an error message when a field, property, event, method, or parameter is emitted out of order.</span></span>|  
|`MDMethodOutOfOrder`|<span data-ttu-id="e0b64-112">指示当方法无序发出时，编译器应生成错误消息。</span><span class="sxs-lookup"><span data-stu-id="e0b64-112">Indicates that the compiler should generate an error message when a method is emitted out of order.</span></span>|  
|`MDFieldOutOfOrder`|<span data-ttu-id="e0b64-113">指示当字段按顺序发出时，编译器应生成错误消息。</span><span class="sxs-lookup"><span data-stu-id="e0b64-113">Indicates that the compiler should generate an error message when a field is emitted out of order.</span></span>|  
|`MDParamOutOfOrder`|<span data-ttu-id="e0b64-114">指示当参数不按顺序发出时，编译器应生成错误消息。</span><span class="sxs-lookup"><span data-stu-id="e0b64-114">Indicates that the compiler should generate an error message when a parameter is emitted out of order.</span></span>|  
|`MDPropertyOutOfOrder`|<span data-ttu-id="e0b64-115">指示当某个属性未按顺序发出时，编译器应生成错误消息。</span><span class="sxs-lookup"><span data-stu-id="e0b64-115">Indicates that the compiler should generate an error message when a property is emitted out of order.</span></span>|  
|`MDEventOutOfOrder`|<span data-ttu-id="e0b64-116">指示当事件顺序发出时，编译器应生成错误消息。</span><span class="sxs-lookup"><span data-stu-id="e0b64-116">Indicates that the compiler should generate an error message when an event is emitted out of order.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e0b64-117">要求</span><span class="sxs-lookup"><span data-stu-id="e0b64-117">Requirements</span></span>  

 <span data-ttu-id="e0b64-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e0b64-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e0b64-119">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="e0b64-119">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="e0b64-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e0b64-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0b64-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="e0b64-121">See also</span></span>

- [<span data-ttu-id="e0b64-122">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="e0b64-122">Metadata Enumerations</span></span>](metadata-enumerations.md)
