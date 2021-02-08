---
description: 了解详细信息： ICLRIoCompletionManager 接口
title: ICLRIoCompletionManager 接口
ms.date: 03/30/2017
api_name:
- ICLRIoCompletionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRIoCompletionManager
helpviewer_keywords:
- ICLRIoCompletionManager interface [.NET Framework hosting]
ms.assetid: c6c3ace6-e5e7-4450-8cc5-a9a48208c493
topic_type:
- apiref
ms.openlocfilehash: b2d18f9c9900d448f0c6517520c303eb4258f8d3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789877"
---
# <a name="iclriocompletionmanager-interface"></a><span data-ttu-id="0e903-103">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="0e903-103">ICLRIoCompletionManager Interface</span></span>

<span data-ttu-id="0e903-104">实现一个回调方法，该方法允许宿主通知公共语言运行时 (CLR) 指定 i/o 请求的状态。</span><span class="sxs-lookup"><span data-stu-id="0e903-104">Implements a callback method that allows the host to notify the common language runtime (CLR) of the status of specified I/O requests.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0e903-105">方法</span><span class="sxs-lookup"><span data-stu-id="0e903-105">Methods</span></span>  
  
|<span data-ttu-id="0e903-106">方法</span><span class="sxs-lookup"><span data-stu-id="0e903-106">Method</span></span>|<span data-ttu-id="0e903-107">说明</span><span class="sxs-lookup"><span data-stu-id="0e903-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0e903-108">OnComplete 方法</span><span class="sxs-lookup"><span data-stu-id="0e903-108">OnComplete Method</span></span>](iclriocompletionmanager-oncomplete-method.md)|<span data-ttu-id="0e903-109">使用对 [IHostIoCompletionManager：： Bind](ihostiocompletionmanager-bind-method.md) 方法的调用，将发出的 i/o 请求状态通知给 CLR。</span><span class="sxs-lookup"><span data-stu-id="0e903-109">Notifies the CLR of the status of an I/O request that was made by using a call to the [IHostIoCompletionManager::Bind](ihostiocompletionmanager-bind-method.md) method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0e903-110">备注</span><span class="sxs-lookup"><span data-stu-id="0e903-110">Remarks</span></span>  

 <span data-ttu-id="0e903-111">宿主通过使用 [IHostIoCompletionManager](ihostiocompletionmanager-interface.md) 接口实现 i/o 完成抽象。</span><span class="sxs-lookup"><span data-stu-id="0e903-111">The host implements the I/O completion abstraction by using the [IHostIoCompletionManager](ihostiocompletionmanager-interface.md) interface.</span></span> <span data-ttu-id="0e903-112">CLR 通过此接口发出 i/o 请求，主机使用接口通知运行时此类请求的结果 `ICLRIoCompletionManager` 。</span><span class="sxs-lookup"><span data-stu-id="0e903-112">The CLR makes I/O requests through this interface, and the host notifies the runtime of the outcome of such requests by using the `ICLRIoCompletionManager` interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0e903-113">要求</span><span class="sxs-lookup"><span data-stu-id="0e903-113">Requirements</span></span>  

 <span data-ttu-id="0e903-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0e903-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0e903-115">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="0e903-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0e903-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0e903-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0e903-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0e903-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e903-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="0e903-118">See also</span></span>

- [<span data-ttu-id="0e903-119">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="0e903-119">IHostIoCompletionManager Interface</span></span>](ihostiocompletionmanager-interface.md)
- [<span data-ttu-id="0e903-120">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="0e903-120">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)
- [<span data-ttu-id="0e903-121">承载接口</span><span class="sxs-lookup"><span data-stu-id="0e903-121">Hosting Interfaces</span></span>](hosting-interfaces.md)
