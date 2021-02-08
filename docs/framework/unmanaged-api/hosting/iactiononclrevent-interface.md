---
description: 了解详细信息： IActionOnCLREvent 接口
title: IActionOnCLREvent 接口
ms.date: 03/30/2017
api_name:
- IActionOnCLREvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IActionOnCLREvent
helpviewer_keywords:
- IActionOnCLREvent interface [.NET Framework hosting]
ms.assetid: b5f9b41e-7301-429c-911f-21d5422292b3
topic_type:
- apiref
ms.openlocfilehash: 9d762635247f897663f4c6f2badf67edf98bd5d0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785167"
---
# <a name="iactiononclrevent-interface"></a><span data-ttu-id="1891b-103">IActionOnCLREvent 接口</span><span class="sxs-lookup"><span data-stu-id="1891b-103">IActionOnCLREvent Interface</span></span>

<span data-ttu-id="1891b-104">提供了 [IActionOnCLREvent：： OnEvent](iactiononclrevent-onevent-method.md) 方法，该方法对已通过调用 [ICLROnEventManager：： RegisterActionOnEvent](iclroneventmanager-registeractiononevent-method.md) 方法注册的事件执行回调。</span><span class="sxs-lookup"><span data-stu-id="1891b-104">Provides the [IActionOnCLREvent::OnEvent](iactiononclrevent-onevent-method.md) method, which performs callbacks on events that have been registered by using a call to the [ICLROnEventManager::RegisterActionOnEvent](iclroneventmanager-registeractiononevent-method.md) method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1891b-105">方法</span><span class="sxs-lookup"><span data-stu-id="1891b-105">Methods</span></span>  
  
|<span data-ttu-id="1891b-106">方法</span><span class="sxs-lookup"><span data-stu-id="1891b-106">Method</span></span>|<span data-ttu-id="1891b-107">说明</span><span class="sxs-lookup"><span data-stu-id="1891b-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1891b-108">OnEvent 方法</span><span class="sxs-lookup"><span data-stu-id="1891b-108">OnEvent Method</span></span>](iactiononclrevent-onevent-method.md)|<span data-ttu-id="1891b-109">对已注册的事件执行回调。</span><span class="sxs-lookup"><span data-stu-id="1891b-109">Performs a callback for a registered event.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1891b-110">要求</span><span class="sxs-lookup"><span data-stu-id="1891b-110">Requirements</span></span>  

 <span data-ttu-id="1891b-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1891b-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1891b-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="1891b-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1891b-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1891b-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1891b-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1891b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1891b-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="1891b-115">See also</span></span>

- [<span data-ttu-id="1891b-116">EClrEvent 枚举</span><span class="sxs-lookup"><span data-stu-id="1891b-116">EClrEvent Enumeration</span></span>](eclrevent-enumeration.md)
- [<span data-ttu-id="1891b-117">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="1891b-117">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="1891b-118">ICLROnEventManager 接口</span><span class="sxs-lookup"><span data-stu-id="1891b-118">ICLROnEventManager Interface</span></span>](iclroneventmanager-interface.md)
- [<span data-ttu-id="1891b-119">承载接口</span><span class="sxs-lookup"><span data-stu-id="1891b-119">Hosting Interfaces</span></span>](hosting-interfaces.md)
