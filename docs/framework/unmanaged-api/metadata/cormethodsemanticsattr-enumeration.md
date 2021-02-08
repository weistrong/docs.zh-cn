---
description: 了解详细信息： CorMethodSemanticsAttr 枚举
title: CorMethodSemanticsAttr 枚举
ms.date: 03/30/2017
api_name:
- CorMethodSemanticsAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorMethodSemanticsAttr
helpviewer_keywords:
- CorMethodSemanticsAttr enumeration [.NET Framework metadata]
ms.assetid: ca2af325-eb9d-4a91-90e4-267e45b98611
topic_type:
- apiref
ms.openlocfilehash: 4079e81ae2389ff0684fd11d0751b191a7289932
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784361"
---
# <a name="cormethodsemanticsattr-enumeration"></a><span data-ttu-id="bcd4d-103">CorMethodSemanticsAttr 枚举</span><span class="sxs-lookup"><span data-stu-id="bcd4d-103">CorMethodSemanticsAttr Enumeration</span></span>

<span data-ttu-id="bcd4d-104">包含一些值，用于描述方法和关联属性或事件之间的关系。</span><span class="sxs-lookup"><span data-stu-id="bcd4d-104">Contains values that describe the relationship between a method and an associated property or event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bcd4d-105">语法</span><span class="sxs-lookup"><span data-stu-id="bcd4d-105">Syntax</span></span>  
  
```cpp  
typedef enum CorMethodSemanticsAttr {  
  
    msSetter    =   0x0001,  
    msGetter    =   0x0002,  
    msOther     =   0x0004,  
    msAddOn     =   0x0008,  
    msRemoveOn  =   0x0010,  
    msFire      =   0x0020,  
  
} CorMethodSemanticsAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="bcd4d-106">成员</span><span class="sxs-lookup"><span data-stu-id="bcd4d-106">Members</span></span>  
  
|<span data-ttu-id="bcd4d-107">成员</span><span class="sxs-lookup"><span data-stu-id="bcd4d-107">Member</span></span>|<span data-ttu-id="bcd4d-108">说明</span><span class="sxs-lookup"><span data-stu-id="bcd4d-108">Description</span></span>|  
|------------|-----------------|  
|`msSetter`|<span data-ttu-id="bcd4d-109">指定该方法是属性的 `set` 访问器。</span><span class="sxs-lookup"><span data-stu-id="bcd4d-109">Specifies that the method is a `set` accessor for a property.</span></span>|  
|`msGetter`|<span data-ttu-id="bcd4d-110">指定该方法是属性的 `get` 访问器。</span><span class="sxs-lookup"><span data-stu-id="bcd4d-110">Specifies that the method is a `get` accessor for a property.</span></span>|  
|`msOther`|<span data-ttu-id="bcd4d-111">指定该方法与在此处定义的属性或事件无关。</span><span class="sxs-lookup"><span data-stu-id="bcd4d-111">Specifies that the method has a relationship to a property or an event other than those defined here.</span></span>|  
|`msAddOn`|<span data-ttu-id="bcd4d-112">指定方法为事件添加处理程序方法。</span><span class="sxs-lookup"><span data-stu-id="bcd4d-112">Specifies that the method adds handler methods for an event.</span></span>|  
|`msRemoveOn`|<span data-ttu-id="bcd4d-113">指定该方法移除事件的处理程序方法。</span><span class="sxs-lookup"><span data-stu-id="bcd4d-113">Specifies that the method removes handler methods for an event.</span></span>|  
|`msFire`|<span data-ttu-id="bcd4d-114">指定方法引发事件。</span><span class="sxs-lookup"><span data-stu-id="bcd4d-114">Specifies that the method raises an event.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="bcd4d-115">要求</span><span class="sxs-lookup"><span data-stu-id="bcd4d-115">Requirements</span></span>  

 <span data-ttu-id="bcd4d-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bcd4d-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bcd4d-117">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="bcd4d-117">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="bcd4d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bcd4d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bcd4d-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="bcd4d-119">See also</span></span>

- [<span data-ttu-id="bcd4d-120">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="bcd4d-120">Metadata Enumerations</span></span>](metadata-enumerations.md)
