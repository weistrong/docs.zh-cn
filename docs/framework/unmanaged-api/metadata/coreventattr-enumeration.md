---
description: 了解详细信息： CorEventAttr 枚举
title: CorEventAttr 枚举
ms.date: 03/30/2017
api_name:
- CorEventAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorEventAttr
helpviewer_keywords:
- CorEventAttr enumeration [.NET Framework metadata]
ms.assetid: dc2b3281-3820-487e-930d-350b66dc6417
topic_type:
- apiref
ms.openlocfilehash: 70f05eacf2cc7c7975b9b52d402cceb60bbea426
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784504"
---
# <a name="coreventattr-enumeration"></a><span data-ttu-id="ab41a-103">CorEventAttr 枚举</span><span class="sxs-lookup"><span data-stu-id="ab41a-103">CorEventAttr Enumeration</span></span>

<span data-ttu-id="ab41a-104">包含一些值，用于描述事件的元数据。</span><span class="sxs-lookup"><span data-stu-id="ab41a-104">Contains values that describe the metadata of an event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab41a-105">语法</span><span class="sxs-lookup"><span data-stu-id="ab41a-105">Syntax</span></span>  
  
```cpp  
typedef enum CorEventAttr {  
  
    evSpecialName           =   0x0200,  
  
    evReservedMask          =   0x0400,  
    evRTSpecialName         =   0x0400,  
  
} CorEventAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="ab41a-106">成员</span><span class="sxs-lookup"><span data-stu-id="ab41a-106">Members</span></span>  
  
|<span data-ttu-id="ab41a-107">成员</span><span class="sxs-lookup"><span data-stu-id="ab41a-107">Member</span></span>|<span data-ttu-id="ab41a-108">说明</span><span class="sxs-lookup"><span data-stu-id="ab41a-108">Description</span></span>|  
|------------|-----------------|  
|`evSpecialName`|<span data-ttu-id="ab41a-109">指定事件是特殊的，其名称描述了操作方法。</span><span class="sxs-lookup"><span data-stu-id="ab41a-109">Specifies that the event is special, and that its name describes how.</span></span>|  
|`evReservedMask`|<span data-ttu-id="ab41a-110">保留供公共语言运行时内部使用。</span><span class="sxs-lookup"><span data-stu-id="ab41a-110">Reserved for internal use by the common language runtime.</span></span>|  
|`evRTSpecialName`|<span data-ttu-id="ab41a-111">指定公共语言运行时应检查事件名称的编码。</span><span class="sxs-lookup"><span data-stu-id="ab41a-111">Specifies that the common language runtime should check the encoding of the event name.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ab41a-112">要求</span><span class="sxs-lookup"><span data-stu-id="ab41a-112">Requirements</span></span>  

 <span data-ttu-id="ab41a-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ab41a-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab41a-114">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="ab41a-114">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="ab41a-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ab41a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab41a-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="ab41a-116">See also</span></span>

- [<span data-ttu-id="ab41a-117">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="ab41a-117">Metadata Enumerations</span></span>](metadata-enumerations.md)
