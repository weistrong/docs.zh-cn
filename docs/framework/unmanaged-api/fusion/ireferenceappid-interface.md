---
description: 了解详细信息： IReferenceAppId 接口
title: IReferenceAppId 接口
ms.date: 03/30/2017
api_name:
- IReferenceAppId
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IReferenceAppId
helpviewer_keywords:
- IReferenceAppId interface [.NET Framework fusion]
ms.assetid: 8eb9e565-f358-43ce-900e-a8f8a5aa6cfb
topic_type:
- apiref
ms.openlocfilehash: 66838d6ae66aa7de05d899e9fa980308718e2a38
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800066"
---
# <a name="ireferenceappid-interface"></a><span data-ttu-id="a836d-103">IReferenceAppId 接口</span><span class="sxs-lookup"><span data-stu-id="a836d-103">IReferenceAppId Interface</span></span>

<span data-ttu-id="a836d-104">表示对当前范围内的应用程序的唯一标识符的引用。</span><span class="sxs-lookup"><span data-stu-id="a836d-104">Represents a reference to the unique identifier for the application in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a836d-105">方法</span><span class="sxs-lookup"><span data-stu-id="a836d-105">Methods</span></span>  
  
|<span data-ttu-id="a836d-106">方法</span><span class="sxs-lookup"><span data-stu-id="a836d-106">Method</span></span>|<span data-ttu-id="a836d-107">说明</span><span class="sxs-lookup"><span data-stu-id="a836d-107">Description</span></span>|  
|------------|-----------------|  
|`IReferenceAppId::get_CodeBase`|<span data-ttu-id="a836d-108">获取一个指针，该指针指向由此引用的应用程序的代码标识符的字符串表示形式 `IReferenceAppId` 。</span><span class="sxs-lookup"><span data-stu-id="a836d-108">Gets a pointer to a string representation of the code identifier for the application referenced by this `IReferenceAppId`.</span></span>|  
|`IReferenceAppId::put_CodeBase`|<span data-ttu-id="a836d-109">设置由此引用的应用程序的代码标识符 `IReferenceAppId` 。</span><span class="sxs-lookup"><span data-stu-id="a836d-109">Sets the code identifier for the application referenced by this `IReferenceAppId`.</span></span>|  
|`IReferenceAppId::EnumAppPath`|<span data-ttu-id="a836d-110">获取一个接口指针，该指针指向一个 `IEnumReferenceIdentity` 实例，该实例包含 `IReferenceIdentity` 表示此的成员的实例 `IReferenceAppId` 。</span><span class="sxs-lookup"><span data-stu-id="a836d-110">Gets an interface pointer to an `IEnumReferenceIdentity` instance containing the `IReferenceIdentity` instances that represent members of this `IReferenceAppId`.</span></span>|  
|`IReferenceAppId::get_SubscriptionId`|<span data-ttu-id="a836d-111">获取一个指针，该指针指向此的订阅的标记标识符的字符串表示形式 `IReferenceAppId` 。</span><span class="sxs-lookup"><span data-stu-id="a836d-111">Gets a pointer to a string representation of the token identifier for a subscription to this `IReferenceAppId`.</span></span>|  
|`IReferenceAppId::put_SubscriptionId`|<span data-ttu-id="a836d-112">将此订阅的标记标识符设置为 `IReferenceAppId` 指定的字符串值。</span><span class="sxs-lookup"><span data-stu-id="a836d-112">Sets the token identifier for a subscription to this `IReferenceAppId` to the specified string value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a836d-113">要求</span><span class="sxs-lookup"><span data-stu-id="a836d-113">Requirements</span></span>  

 <span data-ttu-id="a836d-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a836d-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a836d-115">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="a836d-115">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="a836d-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a836d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a836d-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="a836d-117">See also</span></span>

- [<span data-ttu-id="a836d-118">合成接口</span><span class="sxs-lookup"><span data-stu-id="a836d-118">Fusion Interfaces</span></span>](fusion-interfaces.md)
- [<span data-ttu-id="a836d-119">IEnumReferenceIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="a836d-119">IEnumReferenceIdentity Interface</span></span>](ienumreferenceidentity-interface.md)
- [<span data-ttu-id="a836d-120">IReferenceIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="a836d-120">IReferenceIdentity Interface</span></span>](ireferenceidentity-interface.md)
