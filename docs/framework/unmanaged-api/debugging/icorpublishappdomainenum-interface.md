---
description: 了解详细信息： ICorPublishAppDomainEnum 接口
title: ICorPublishAppDomainEnum 接口
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomainEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomainEnum
helpviewer_keywords:
- ICorPublishAppDomainEnum interface [.NET Framework debugging]
ms.assetid: bb798c56-042e-475d-a245-b6fac36d0c07
topic_type:
- apiref
ms.openlocfilehash: 4e84af576103a792308fd44f903f2ae4daa5d736
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721783"
---
# <a name="icorpublishappdomainenum-interface"></a><span data-ttu-id="696f3-103">ICorPublishAppDomainEnum 接口</span><span class="sxs-lookup"><span data-stu-id="696f3-103">ICorPublishAppDomainEnum Interface</span></span>

<span data-ttu-id="696f3-104">[ICorPublishEnum](icorpublishenum-interface.md)接口的子类，它提供了用于遍历进程中当前存在的[ICorPublishAppDomain](icorpublishappdomain-interface.md)对象的集合的方法。</span><span class="sxs-lookup"><span data-stu-id="696f3-104">A subclass of the [ICorPublishEnum](icorpublishenum-interface.md) interface that provides methods to traverse a collection of [ICorPublishAppDomain](icorpublishappdomain-interface.md) objects that currently exist within a process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="696f3-105">方法</span><span class="sxs-lookup"><span data-stu-id="696f3-105">Methods</span></span>  
  
|<span data-ttu-id="696f3-106">方法</span><span class="sxs-lookup"><span data-stu-id="696f3-106">Method</span></span>|<span data-ttu-id="696f3-107">说明</span><span class="sxs-lookup"><span data-stu-id="696f3-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="696f3-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="696f3-108">Next Method</span></span>](icorpublishappdomainenum-next-method.md)|<span data-ttu-id="696f3-109">`ICorPublishAppDomain`从当前位置开始，获取集合中指定数量的实例。</span><span class="sxs-lookup"><span data-stu-id="696f3-109">Gets the specified number of `ICorPublishAppDomain` instances from the collection, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="696f3-110">备注</span><span class="sxs-lookup"><span data-stu-id="696f3-110">Remarks</span></span>  

 <span data-ttu-id="696f3-111">`ICorPublishAppDomainEnum`接口实现抽象接口的方法[ICorPublishEnum](icorpublishenum-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="696f3-111">The `ICorPublishAppDomainEnum` interface implements the methods of the abstract interface, [ICorPublishEnum](icorpublishenum-interface.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="696f3-112">要求</span><span class="sxs-lookup"><span data-stu-id="696f3-112">Requirements</span></span>  

 <span data-ttu-id="696f3-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="696f3-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="696f3-114">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="696f3-114">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="696f3-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="696f3-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="696f3-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="696f3-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="696f3-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="696f3-117">See also</span></span>

- [<span data-ttu-id="696f3-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="696f3-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="696f3-119">CorpubPublish Coclass</span><span class="sxs-lookup"><span data-stu-id="696f3-119">CorpubPublish Coclass</span></span>](corpubpublish-coclass.md)
