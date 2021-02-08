---
description: 了解详细信息： CorRefToDefCheck 枚举
title: CorRefToDefCheck 枚举
ms.date: 03/30/2017
api_name:
- CorRefToDefCheck
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorRefToDefCheck
helpviewer_keywords:
- CorRefToDefCheck enumeration [.NET Framework metadata]
ms.assetid: f9a80f1a-55af-4459-b095-8441aae16119
topic_type:
- apiref
ms.openlocfilehash: ca9d1c7ceb3d9f82ef8d5f1f54d869db64053e69
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784244"
---
# <a name="correftodefcheck-enumeration"></a><span data-ttu-id="e660d-103">CorRefToDefCheck 枚举</span><span class="sxs-lookup"><span data-stu-id="e660d-103">CorRefToDefCheck Enumeration</span></span>

<span data-ttu-id="e660d-104">指定用于控制将哪些引用项转换为相应定义以优化代码的标志。</span><span class="sxs-lookup"><span data-stu-id="e660d-104">Specifies flags to control which referenced items are converted to their definitions in order to optimize the code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e660d-105">语法</span><span class="sxs-lookup"><span data-stu-id="e660d-105">Syntax</span></span>  
  
```cpp  
typedef enum CorRefToDefCheck {  
    MDRefToDefDefault           = 0x00000003,  
    MDRefToDefAll               = 0xffffffff,  
    MDRefToDefNone              = 0x00000000,  
    MDTypeRefToDef              = 0x00000001,  
    MDMemberRefToDef            = 0x00000002  
} CorRefToDefCheck;  
```  
  
## <a name="members"></a><span data-ttu-id="e660d-106">成员</span><span class="sxs-lookup"><span data-stu-id="e660d-106">Members</span></span>  
  
|<span data-ttu-id="e660d-107">成员</span><span class="sxs-lookup"><span data-stu-id="e660d-107">Member</span></span>|<span data-ttu-id="e660d-108">说明</span><span class="sxs-lookup"><span data-stu-id="e660d-108">Description</span></span>|  
|------------|-----------------|  
|`MDRefToDefDefault`|<span data-ttu-id="e660d-109">指定应将类型引用和成员引用转换为定义。</span><span class="sxs-lookup"><span data-stu-id="e660d-109">Specifies that type references and member references should be converted to definitions.</span></span> <span data-ttu-id="e660d-110">这是 (&#124;) 的默认值 `MDTypeRefToDef` `MDMemberRefToDef` 。</span><span class="sxs-lookup"><span data-stu-id="e660d-110">This is the default value (`MDTypeRefToDef` &#124; `MDMemberRefToDef`).</span></span>|  
|`MDRefToDefAll`|<span data-ttu-id="e660d-111">指定所有引用项都应转换为定义。</span><span class="sxs-lookup"><span data-stu-id="e660d-111">Specifies that all referenced items should be converted to definitions.</span></span>|  
|`MDRefToDefNone`|<span data-ttu-id="e660d-112">指定不应将引用项转换为定义。</span><span class="sxs-lookup"><span data-stu-id="e660d-112">Specifies that no referenced items should be converted to definitions.</span></span>|  
|`MDTypeRefToDef`|<span data-ttu-id="e660d-113">指定仅类型引用应转换为类型定义。</span><span class="sxs-lookup"><span data-stu-id="e660d-113">Specifies that only type references should be converted to type definitions.</span></span>|  
|`MDMemberRefToDef`|<span data-ttu-id="e660d-114">指定只应将成员引用转换为定义。</span><span class="sxs-lookup"><span data-stu-id="e660d-114">Specifies that only member references should be converted to definitions.</span></span> <span data-ttu-id="e660d-115">也就是说，应将成员引用转换为方法定义或字段定义。</span><span class="sxs-lookup"><span data-stu-id="e660d-115">That is, member references should be converted to either method definitions or field definitions.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e660d-116">要求</span><span class="sxs-lookup"><span data-stu-id="e660d-116">Requirements</span></span>  

 <span data-ttu-id="e660d-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e660d-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e660d-118">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="e660d-118">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="e660d-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e660d-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e660d-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="e660d-120">See also</span></span>

- [<span data-ttu-id="e660d-121">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="e660d-121">Metadata Enumerations</span></span>](metadata-enumerations.md)
