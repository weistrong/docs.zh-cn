---
description: 了解详细信息： IEnumReferenceIdentity 接口
title: IEnumReferenceIdentity 接口
ms.date: 03/30/2017
api_name:
- IEnumReferenceIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumReferenceIdentity
helpviewer_keywords:
- IEnumReferenceIdentity interface [.NET Framework fusion]
ms.assetid: a17b3155-7216-4e16-8c9f-abce21f549e7
topic_type:
- apiref
ms.openlocfilehash: a7f17793fd737b5153c27dae59fb2aa87b46cf48
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100465296"
---
# <a name="ienumreferenceidentity-interface"></a><span data-ttu-id="19180-103">IEnumReferenceIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="19180-103">IEnumReferenceIdentity Interface</span></span>

<span data-ttu-id="19180-104">用作对象集合的枚举器 `IReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="19180-104">Serves as an enumerator for a collection of `IReferenceIdentity` objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="19180-105">方法</span><span class="sxs-lookup"><span data-stu-id="19180-105">Methods</span></span>  
  
|<span data-ttu-id="19180-106">方法</span><span class="sxs-lookup"><span data-stu-id="19180-106">Method</span></span>|<span data-ttu-id="19180-107">说明</span><span class="sxs-lookup"><span data-stu-id="19180-107">Description</span></span>|  
|------------|-----------------|  
|`IEnumReferenceIdentity::Clone`|<span data-ttu-id="19180-108">获取一个接口指针，该指针指向 `IEnumReferenceIdentity` 包含与此相同的成员的新 `IEnumReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="19180-108">Gets an interface pointer to a new `IEnumReferenceIdentity` that contains the same members as this `IEnumReferenceIdentity`.</span></span>|  
|`IEnumReferenceIdentity::Next`|<span data-ttu-id="19180-109">`IReferenceIdentity`从当前位置开始，获取指定数目的对象。</span><span class="sxs-lookup"><span data-stu-id="19180-109">Gets the specified number of `IReferenceIdentity` objects, starting at the current position.</span></span>|  
|`IEnumReferenceIdentity::Reset`|<span data-ttu-id="19180-110">将指令指针移到此的开头 `IEnumReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="19180-110">Moves the instruction pointer to the beginning of this `IEnumReferenceIdentity`.</span></span>|  
|`IEnumReferenceIdentity::Skip`|<span data-ttu-id="19180-111">从当前位置开始，将指令指针向前移动指定数量的元素。</span><span class="sxs-lookup"><span data-stu-id="19180-111">Moves the instruction pointer forward by the specified number of elements, starting at the current position.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="19180-112">要求</span><span class="sxs-lookup"><span data-stu-id="19180-112">Requirements</span></span>  

 <span data-ttu-id="19180-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="19180-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="19180-114">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="19180-114">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="19180-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="19180-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19180-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="19180-116">See also</span></span>

- [<span data-ttu-id="19180-117">合成接口</span><span class="sxs-lookup"><span data-stu-id="19180-117">Fusion Interfaces</span></span>](fusion-interfaces.md)
- [<span data-ttu-id="19180-118">IReferenceIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="19180-118">IReferenceIdentity Interface</span></span>](ireferenceidentity-interface.md)
