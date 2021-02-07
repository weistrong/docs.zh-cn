---
description: 了解详细信息： CorArgType 枚举
title: CorArgType 枚举
ms.date: 03/30/2017
api_name:
- CorArgType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorArgType
helpviewer_keywords:
- CorArgType enumeration [.NET Framework metadata]
ms.assetid: 3c1cb268-57a0-4664-91c7-f6908ff29e32
topic_type:
- apiref
ms.openlocfilehash: de7067e6c7b825aae797d88dbd5f2ecd2f5280fa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678518"
---
# <a name="corargtype-enumeration"></a><span data-ttu-id="6535f-103">CorArgType 枚举</span><span class="sxs-lookup"><span data-stu-id="6535f-103">CorArgType Enumeration</span></span>

<span data-ttu-id="6535f-104">包含一些值，用于描述运行时句柄的本机类型。</span><span class="sxs-lookup"><span data-stu-id="6535f-104">Contains values that describe the native type of a runtime handle.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6535f-105">语法</span><span class="sxs-lookup"><span data-stu-id="6535f-105">Syntax</span></span>  
  
```cpp  
typedef enum CorArgType {  
  
    IMAGE_CEE_CS_END        = 0x0,  
    IMAGE_CEE_CS_VOID       = 0x1,  
    IMAGE_CEE_CS_I4         = 0x2,  
    IMAGE_CEE_CS_I8         = 0x3,  
    IMAGE_CEE_CS_R4         = 0x4,  
    IMAGE_CEE_CS_R8         = 0x5,  
    IMAGE_CEE_CS_PTR        = 0x6,  
    IMAGE_CEE_CS_OBJECT     = 0x7,  
    IMAGE_CEE_CS_STRUCT4    = 0x8,  
    IMAGE_CEE_CS_STRUCT32   = 0x9,  
    IMAGE_CEE_CS_BYVALUE    = 0xA  
  
} CorArgType;  
```  
  
## <a name="requirements"></a><span data-ttu-id="6535f-106">要求</span><span class="sxs-lookup"><span data-stu-id="6535f-106">Requirements</span></span>  

 <span data-ttu-id="6535f-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6535f-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6535f-108">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="6535f-108">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="6535f-109">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6535f-109">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6535f-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="6535f-110">See also</span></span>

- [<span data-ttu-id="6535f-111">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="6535f-111">Metadata Enumerations</span></span>](metadata-enumerations.md)
