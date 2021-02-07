---
description: 了解详细信息： IHostSecurityContext 接口
title: IHostSecurityContext 接口
ms.date: 03/30/2017
api_name:
- IHostSecurityContext
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityContext
helpviewer_keywords:
- IHostSecurityContext interface [.NET Framework hosting]
ms.assetid: 88e2eac0-8ccb-404f-abbc-287d55159842
topic_type:
- apiref
ms.openlocfilehash: c4c1be00a8b1c9df58797a0f2fc7e60abcab9673
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671615"
---
# <a name="ihostsecuritycontext-interface"></a><span data-ttu-id="c764c-103">IHostSecurityContext 接口</span><span class="sxs-lookup"><span data-stu-id="c764c-103">IHostSecurityContext Interface</span></span>

<span data-ttu-id="c764c-104">允许公共语言运行时 (CLR) 维护宿主实现的安全上下文信息。</span><span class="sxs-lookup"><span data-stu-id="c764c-104">Allows the common language runtime (CLR) to maintain security context information implemented by the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c764c-105">方法</span><span class="sxs-lookup"><span data-stu-id="c764c-105">Methods</span></span>  
  
|<span data-ttu-id="c764c-106">方法</span><span class="sxs-lookup"><span data-stu-id="c764c-106">Method</span></span>|<span data-ttu-id="c764c-107">说明</span><span class="sxs-lookup"><span data-stu-id="c764c-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c764c-108">Capture 方法</span><span class="sxs-lookup"><span data-stu-id="c764c-108">Capture Method</span></span>](ihostsecuritycontext-capture-method.md)|<span data-ttu-id="c764c-109">获取 `IHostSecurityContext` 从对 [IHostSecurityManager：： GetSecurityContext](ihostsecuritymanager-getsecuritycontext-method.md)的调用返回的实例的克隆。</span><span class="sxs-lookup"><span data-stu-id="c764c-109">Gets a clone of the `IHostSecurityContext` instance returned from a call to [IHostSecurityManager::GetSecurityContext](ihostsecuritymanager-getsecuritycontext-method.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c764c-110">备注</span><span class="sxs-lookup"><span data-stu-id="c764c-110">Remarks</span></span>  

 <span data-ttu-id="c764c-111">宿主可以通过 CLR 和用户代码控制对线程标记的所有代码访问。</span><span class="sxs-lookup"><span data-stu-id="c764c-111">A host can control all code access to thread tokens by both the CLR and user code.</span></span> <span data-ttu-id="c764c-112">它还可以确保在异步操作或代码点之间跨受限制的代码访问传递完整的安全上下文信息。</span><span class="sxs-lookup"><span data-stu-id="c764c-112">It can also ensure that complete security context information is passed across asynchronous operations or code points with restricted code access.</span></span> <span data-ttu-id="c764c-113">`IHostSecurityContext` 封装此安全上下文信息，这对于运行时是不透明的。</span><span class="sxs-lookup"><span data-stu-id="c764c-113">`IHostSecurityContext` encapsulates this security context information, which is opaque to the runtime.</span></span> <span data-ttu-id="c764c-114">运行时使用捕获此信息 `Capture` ，并将其移动到线程池辅助角色项调度、终结器执行和模块和类构造函数中。</span><span class="sxs-lookup"><span data-stu-id="c764c-114">The runtime captures this information using `Capture`, and moves it across thread pool worker item dispatch, finalizer execution, and module and class constructors.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c764c-115">要求</span><span class="sxs-lookup"><span data-stu-id="c764c-115">Requirements</span></span>  

 <span data-ttu-id="c764c-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c764c-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c764c-117">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c764c-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c764c-118">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c764c-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c764c-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c764c-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c764c-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="c764c-120">See also</span></span>

- [<span data-ttu-id="c764c-121">ICLRHostProtectionManager 接口</span><span class="sxs-lookup"><span data-stu-id="c764c-121">ICLRHostProtectionManager Interface</span></span>](iclrhostprotectionmanager-interface.md)
- [<span data-ttu-id="c764c-122">IHostSecurityManager 接口</span><span class="sxs-lookup"><span data-stu-id="c764c-122">IHostSecurityManager Interface</span></span>](ihostsecuritymanager-interface.md)
- [<span data-ttu-id="c764c-123">承载接口</span><span class="sxs-lookup"><span data-stu-id="c764c-123">Hosting Interfaces</span></span>](hosting-interfaces.md)
