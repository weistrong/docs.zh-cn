---
description: 了解详细信息： IEnumIDENTITY_ATTRIBUTE 接口
title: IEnumIDENTITY_ATTRIBUTE 接口
ms.date: 03/30/2017
api_name:
- IEnumIDENTITY_ATTRIBUTE
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumIDENTITY_ATTRIBUTE
helpviewer_keywords:
- IEnumIDENTITY_ATTRIBUTE interface [.NET Framework fusion]
ms.assetid: c2ec2748-e9ae-4e1b-80db-6fcec5cb81a1
topic_type:
- apiref
ms.openlocfilehash: b621a722e35d5b31f487e8823b1627fdfe1e7888
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800142"
---
# <a name="ienumidentity_attribute-interface"></a><span data-ttu-id="e21f4-103">IEnumIDENTITY_ATTRIBUTE 接口</span><span class="sxs-lookup"><span data-stu-id="e21f4-103">IEnumIDENTITY_ATTRIBUTE Interface</span></span>

<span data-ttu-id="e21f4-104">用作当前范围中代码对象的特性的枚举数。</span><span class="sxs-lookup"><span data-stu-id="e21f4-104">Serves as an enumerator for the attributes of the code object in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e21f4-105">方法</span><span class="sxs-lookup"><span data-stu-id="e21f4-105">Methods</span></span>  
  
|<span data-ttu-id="e21f4-106">方法</span><span class="sxs-lookup"><span data-stu-id="e21f4-106">Method</span></span>|<span data-ttu-id="e21f4-107">说明</span><span class="sxs-lookup"><span data-stu-id="e21f4-107">Description</span></span>|  
|------------|-----------------|  
|`IEnumIDENTITY_ATTRIBUTE::Clone`|<span data-ttu-id="e21f4-108">获取一个接口指针，该指针指向 `IEnumIDENTITY_ATTRIBUTE` 包含与此相同的成员的新 `IEnumIDENTITY_ATTRIBUTE` 。</span><span class="sxs-lookup"><span data-stu-id="e21f4-108">Gets an interface pointer to a new `IEnumIDENTITY_ATTRIBUTE` that contains the same members as this `IEnumIDENTITY_ATTRIBUTE`.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::CurrentIntoBuffer`|<span data-ttu-id="e21f4-109">将此中包含的数据写入 `IEnumIDENTITY_ATTRIBUTE` 指定的数据缓冲区。</span><span class="sxs-lookup"><span data-stu-id="e21f4-109">Writes the data contained in the elements of this `IEnumIDENTITY_ATTRIBUTE` to the specified data buffer.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::Next`|<span data-ttu-id="e21f4-110">从当前位置开始，获取指定数目的属性。</span><span class="sxs-lookup"><span data-stu-id="e21f4-110">Gets the specified number of attributes, starting at the current position.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::Reset`|<span data-ttu-id="e21f4-111">将指令指针移到此的开头 `IEnumIDENTITY_ATTRIBUTE` 。</span><span class="sxs-lookup"><span data-stu-id="e21f4-111">Moves the instruction pointer to the beginning of this `IEnumIDENTITY_ATTRIBUTE`.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::Skip`|<span data-ttu-id="e21f4-112">从当前位置开始，将指令指针向前移动指定数量的元素。</span><span class="sxs-lookup"><span data-stu-id="e21f4-112">Moves the instruction pointer forward by the specified number of elements, starting at the current position.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e21f4-113">要求</span><span class="sxs-lookup"><span data-stu-id="e21f4-113">Requirements</span></span>  

 <span data-ttu-id="e21f4-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e21f4-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e21f4-115">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="e21f4-115">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="e21f4-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e21f4-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e21f4-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="e21f4-117">See also</span></span>

- [<span data-ttu-id="e21f4-118">合成接口</span><span class="sxs-lookup"><span data-stu-id="e21f4-118">Fusion Interfaces</span></span>](fusion-interfaces.md)
