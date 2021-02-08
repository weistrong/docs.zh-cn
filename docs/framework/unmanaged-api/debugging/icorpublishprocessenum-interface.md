---
description: 了解详细信息： ICorPublishProcessEnum 接口
title: ICorPublishProcessEnum 接口
ms.date: 03/30/2017
api_name:
- ICorPublishProcessEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcessEnum
helpviewer_keywords:
- ICorPublishProcessEnum interface [.NET Framework debugging]
ms.assetid: aac8fcf9-ac09-437c-bd5c-2fda14ae1007
topic_type:
- apiref
ms.openlocfilehash: 87d80d066995dbeca67f461e01652dd3deb3bf1b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790485"
---
# <a name="icorpublishprocessenum-interface"></a><span data-ttu-id="62dbe-103">ICorPublishProcessEnum 接口</span><span class="sxs-lookup"><span data-stu-id="62dbe-103">ICorPublishProcessEnum Interface</span></span>

<span data-ttu-id="62dbe-104">[ICorPublishEnum](icorpublishenum-interface.md)接口的子类，提供遍历[ICorPublishProcess](icorpublishprocess-interface.md)对象集合的方法。</span><span class="sxs-lookup"><span data-stu-id="62dbe-104">A subclass of the [ICorPublishEnum](icorpublishenum-interface.md) interface that provides methods to traverse a collection of [ICorPublishProcess](icorpublishprocess-interface.md) objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="62dbe-105">方法</span><span class="sxs-lookup"><span data-stu-id="62dbe-105">Methods</span></span>  
  
|<span data-ttu-id="62dbe-106">方法</span><span class="sxs-lookup"><span data-stu-id="62dbe-106">Method</span></span>|<span data-ttu-id="62dbe-107">说明</span><span class="sxs-lookup"><span data-stu-id="62dbe-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="62dbe-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="62dbe-108">Next Method</span></span>](icorpublishprocessenum-next-method.md)|<span data-ttu-id="62dbe-109">`ICorPublishProcess`从当前位置开始，获取集合中指定数量的实例。</span><span class="sxs-lookup"><span data-stu-id="62dbe-109">Gets the specified number of `ICorPublishProcess` instances from the collection, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="62dbe-110">备注</span><span class="sxs-lookup"><span data-stu-id="62dbe-110">Remarks</span></span>  

 <span data-ttu-id="62dbe-111">`ICorPublishProcessEnum`接口实现抽象接口的方法[ICorPublishEnum](icorpublishenum-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="62dbe-111">The `ICorPublishProcessEnum` interface implements the methods of the abstract interface, [ICorPublishEnum](icorpublishenum-interface.md).</span></span>  
  
 <span data-ttu-id="62dbe-112">`ICorPublishProcessEnum`实例由[ICorPublish：： EnumProcesses](icorpublish-enumprocesses-method.md)方法创建。</span><span class="sxs-lookup"><span data-stu-id="62dbe-112">An `ICorPublishProcessEnum` instance is created by the [ICorPublish::EnumProcesses](icorpublish-enumprocesses-method.md) method.</span></span> <span data-ttu-id="62dbe-113">对象集合的遍历 `ICorPublishProcess` 基于创建实例时给定的筛选条件 `ICorPublishProcessEnum` 。</span><span class="sxs-lookup"><span data-stu-id="62dbe-113">The traversal of the collection of `ICorPublishProcess` objects is based on the filter criteria given at the time the `ICorPublishProcessEnum` instance was created.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="62dbe-114">要求</span><span class="sxs-lookup"><span data-stu-id="62dbe-114">Requirements</span></span>  

 <span data-ttu-id="62dbe-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="62dbe-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="62dbe-116">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="62dbe-116">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="62dbe-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="62dbe-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="62dbe-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="62dbe-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62dbe-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="62dbe-119">See also</span></span>

- [<span data-ttu-id="62dbe-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="62dbe-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="62dbe-121">CorpubPublish Coclass</span><span class="sxs-lookup"><span data-stu-id="62dbe-121">CorpubPublish Coclass</span></span>](corpubpublish-coclass.md)
