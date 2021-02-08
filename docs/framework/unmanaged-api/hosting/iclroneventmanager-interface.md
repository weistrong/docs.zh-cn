---
description: 了解详细信息： ICLROnEventManager 接口
title: ICLROnEventManager 接口
ms.date: 03/30/2017
api_name:
- ICLROnEventManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLROnEventManager
helpviewer_keywords:
- ICLROnEventManager interface [.NET Framework hosting]
ms.assetid: 9e15a0c1-8ab6-43d0-ae28-6ec7a4edd913
topic_type:
- apiref
ms.openlocfilehash: 7a9c0beec5083bc93f5361bb0e701da5beeedea2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789822"
---
# <a name="iclroneventmanager-interface"></a><span data-ttu-id="b2bc0-103">ICLROnEventManager 接口</span><span class="sxs-lookup"><span data-stu-id="b2bc0-103">ICLROnEventManager Interface</span></span>

<span data-ttu-id="b2bc0-104">提供一些方法，这些方法允许主机注册和注销公共语言运行时 (CLR) 事件的回调。</span><span class="sxs-lookup"><span data-stu-id="b2bc0-104">Provides methods that allow the host to register and unregister callbacks for common language runtime (CLR) events.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b2bc0-105">方法</span><span class="sxs-lookup"><span data-stu-id="b2bc0-105">Methods</span></span>  
  
|<span data-ttu-id="b2bc0-106">方法</span><span class="sxs-lookup"><span data-stu-id="b2bc0-106">Method</span></span>|<span data-ttu-id="b2bc0-107">说明</span><span class="sxs-lookup"><span data-stu-id="b2bc0-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b2bc0-108">RegisterActionOnEvent 方法</span><span class="sxs-lookup"><span data-stu-id="b2bc0-108">RegisterActionOnEvent Method</span></span>](iclroneventmanager-registeractiononevent-method.md)|<span data-ttu-id="b2bc0-109">为指定事件注册回调指针。</span><span class="sxs-lookup"><span data-stu-id="b2bc0-109">Registers a callback pointer for the specified event.</span></span>|  
|[<span data-ttu-id="b2bc0-110">UnregisterActionOnEvent 方法</span><span class="sxs-lookup"><span data-stu-id="b2bc0-110">UnregisterActionOnEvent Method</span></span>](iclroneventmanager-unregisteractiononevent-method.md)|<span data-ttu-id="b2bc0-111">为指定的事件注销先前注册的回调指针。</span><span class="sxs-lookup"><span data-stu-id="b2bc0-111">Unregisters a previously registered callback pointer for the specified event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b2bc0-112">备注</span><span class="sxs-lookup"><span data-stu-id="b2bc0-112">Remarks</span></span>  

 <span data-ttu-id="b2bc0-113">若要注册和注销事件回调，主机可 `ICLROnEventManager` 通过调用 [ICLRControl：： GetCLRManager](iclrcontrol-getclrmanager-method.md) 方法获取对的引用。</span><span class="sxs-lookup"><span data-stu-id="b2bc0-113">To register and unregister event callbacks, the host gets a reference to `ICLROnEventManager` by calling the [ICLRControl::GetCLRManager](iclrcontrol-getclrmanager-method.md) method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b2bc0-114">[EClrEvent](eclrevent-enumeration.md)描述的事件可以从不同的线程激发一次，以指示卸载或禁用 CLR。</span><span class="sxs-lookup"><span data-stu-id="b2bc0-114">The events described by [EClrEvent](eclrevent-enumeration.md) can be fired more than once and from different threads to signal an unload or the disabling of the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b2bc0-115">要求</span><span class="sxs-lookup"><span data-stu-id="b2bc0-115">Requirements</span></span>  

 <span data-ttu-id="b2bc0-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b2bc0-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b2bc0-117">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b2bc0-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b2bc0-118">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b2bc0-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b2bc0-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b2bc0-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2bc0-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="b2bc0-120">See also</span></span>

- [<span data-ttu-id="b2bc0-121">EClrEvent 枚举</span><span class="sxs-lookup"><span data-stu-id="b2bc0-121">EClrEvent Enumeration</span></span>](eclrevent-enumeration.md)
- [<span data-ttu-id="b2bc0-122">IActionOnCLREvent 接口</span><span class="sxs-lookup"><span data-stu-id="b2bc0-122">IActionOnCLREvent Interface</span></span>](iactiononclrevent-interface.md)
- [<span data-ttu-id="b2bc0-123">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="b2bc0-123">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="b2bc0-124">承载接口</span><span class="sxs-lookup"><span data-stu-id="b2bc0-124">Hosting Interfaces</span></span>](hosting-interfaces.md)
