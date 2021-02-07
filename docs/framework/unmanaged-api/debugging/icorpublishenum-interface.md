---
description: 了解详细信息： ICorPublishEnum 接口
title: ICorPublishEnum 接口
ms.date: 03/30/2017
api_name:
- ICorPublishEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishEnum
helpviewer_keywords:
- ICorPublishEnum interface [.NET Framework debugging]
ms.assetid: 76a136b5-e444-417a-8ade-f1596d597dc7
topic_type:
- apiref
ms.openlocfilehash: c0d50f67bd61eecbade0b226f2f569ac26712faf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721591"
---
# <a name="icorpublishenum-interface"></a><span data-ttu-id="7dc3c-103">ICorPublishEnum 接口</span><span class="sxs-lookup"><span data-stu-id="7dc3c-103">ICorPublishEnum Interface</span></span>

<span data-ttu-id="7dc3c-104">用作枚举器的抽象基接口，这些枚举器用于发布有关进程和应用程序域的信息。</span><span class="sxs-lookup"><span data-stu-id="7dc3c-104">Serves as the abstract base interface for the enumerators that are used in the publishing of information about processes and application domains.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7dc3c-105">方法</span><span class="sxs-lookup"><span data-stu-id="7dc3c-105">Methods</span></span>  
  
|<span data-ttu-id="7dc3c-106">方法</span><span class="sxs-lookup"><span data-stu-id="7dc3c-106">Method</span></span>|<span data-ttu-id="7dc3c-107">说明</span><span class="sxs-lookup"><span data-stu-id="7dc3c-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7dc3c-108">Clone 方法</span><span class="sxs-lookup"><span data-stu-id="7dc3c-108">Clone Method</span></span>](icorpublishenum-clone-method.md)|<span data-ttu-id="7dc3c-109">创建此 `ICorPublishEnum` 对象的一个副本。</span><span class="sxs-lookup"><span data-stu-id="7dc3c-109">Creates a copy of this `ICorPublishEnum` object.</span></span>|  
|[<span data-ttu-id="7dc3c-110">GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="7dc3c-110">GetCount Method</span></span>](icorpublishenum-getcount-method.md)|<span data-ttu-id="7dc3c-111">获取枚举中的项数。</span><span class="sxs-lookup"><span data-stu-id="7dc3c-111">Gets the number of items in the enumeration.</span></span>|  
|[<span data-ttu-id="7dc3c-112">Reset 方法</span><span class="sxs-lookup"><span data-stu-id="7dc3c-112">Reset Method</span></span>](icorpublishenum-reset-method.md)|<span data-ttu-id="7dc3c-113">将光标移到枚举的开头。</span><span class="sxs-lookup"><span data-stu-id="7dc3c-113">Moves the cursor of to the beginning of the enumeration.</span></span>|  
|[<span data-ttu-id="7dc3c-114">Skip 方法</span><span class="sxs-lookup"><span data-stu-id="7dc3c-114">Skip Method</span></span>](icorpublishenum-skip-method.md)|<span data-ttu-id="7dc3c-115">按指定的项数在枚举中向前移动光标。</span><span class="sxs-lookup"><span data-stu-id="7dc3c-115">Moves the cursor forward in the enumeration by the specified number of items.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7dc3c-116">备注</span><span class="sxs-lookup"><span data-stu-id="7dc3c-116">Remarks</span></span>  

 <span data-ttu-id="7dc3c-117">以下枚举器派生自 `ICorPublishEnum` ：</span><span class="sxs-lookup"><span data-stu-id="7dc3c-117">The following enumerators derive from `ICorPublishEnum`:</span></span>  
  
- [<span data-ttu-id="7dc3c-118">ICorPublishAppDomainEnum</span><span class="sxs-lookup"><span data-stu-id="7dc3c-118">ICorPublishAppDomainEnum</span></span>](icorpublishappdomainenum-interface.md)  
  
- [<span data-ttu-id="7dc3c-119">ICorPublishProcessEnum</span><span class="sxs-lookup"><span data-stu-id="7dc3c-119">ICorPublishProcessEnum</span></span>](icorpublishprocessenum-interface.md)  
  
## <a name="requirements"></a><span data-ttu-id="7dc3c-120">要求</span><span class="sxs-lookup"><span data-stu-id="7dc3c-120">Requirements</span></span>  

 <span data-ttu-id="7dc3c-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7dc3c-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7dc3c-122">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="7dc3c-122">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="7dc3c-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7dc3c-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7dc3c-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7dc3c-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7dc3c-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="7dc3c-125">See also</span></span>

- [<span data-ttu-id="7dc3c-126">CorpubPublish Coclass</span><span class="sxs-lookup"><span data-stu-id="7dc3c-126">CorpubPublish Coclass</span></span>](corpubpublish-coclass.md)
- [<span data-ttu-id="7dc3c-127">调试接口</span><span class="sxs-lookup"><span data-stu-id="7dc3c-127">Debugging Interfaces</span></span>](debugging-interfaces.md)
