---
description: 了解详细信息： IDebuggerThreadControl：： StartBlockingForDebugger 方法
title: IDebuggerThreadControl::StartBlockingForDebugger 方法
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.StartBlockingForDebugger
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StartBlockingForDebugger
helpviewer_keywords:
- IDebuggerThreadControl::StartBlockingForDebugger method [.NET Framework hosting]
- StartBlockingForDebugger method [.NET Framework hosting]
ms.assetid: 5c8f11b4-35d3-4c39-9bbd-58b896ba5ba6
topic_type:
- apiref
ms.openlocfilehash: 3e19817c4adbefd1dd70be047656b3fea261c389
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709667"
---
# <a name="idebuggerthreadcontrolstartblockingfordebugger-method"></a><span data-ttu-id="df6fc-103">IDebuggerThreadControl::StartBlockingForDebugger 方法</span><span class="sxs-lookup"><span data-stu-id="df6fc-103">IDebuggerThreadControl::StartBlockingForDebugger Method</span></span>

<span data-ttu-id="df6fc-104">通知宿主调试服务即将开始阻塞所有线程。</span><span class="sxs-lookup"><span data-stu-id="df6fc-104">Notifies the host that the debugging services are about to start blocking all threads.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df6fc-105">语法</span><span class="sxs-lookup"><span data-stu-id="df6fc-105">Syntax</span></span>  
  
```cpp  
HRESULT StartBlockingForDebugger (  
    [in] DWORD dwUnused  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="df6fc-106">参数</span><span class="sxs-lookup"><span data-stu-id="df6fc-106">Parameters</span></span>  

 `dwUnused`  
 <span data-ttu-id="df6fc-107">中保留供将来使用。</span><span class="sxs-lookup"><span data-stu-id="df6fc-107">[in] Reserved for future use.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="df6fc-108">备注</span><span class="sxs-lookup"><span data-stu-id="df6fc-108">Remarks</span></span>  

 <span data-ttu-id="df6fc-109">`StartBlockingForDebugger`可以在运行时线程上调用方法。</span><span class="sxs-lookup"><span data-stu-id="df6fc-109">The `StartBlockingForDebugger` method could be called on a runtime thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="df6fc-110">要求</span><span class="sxs-lookup"><span data-stu-id="df6fc-110">Requirements</span></span>  

 <span data-ttu-id="df6fc-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="df6fc-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="df6fc-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="df6fc-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="df6fc-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="df6fc-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="df6fc-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="df6fc-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df6fc-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="df6fc-115">See also</span></span>

- [<span data-ttu-id="df6fc-116">IDebuggerThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="df6fc-116">IDebuggerThreadControl Interface</span></span>](idebuggerthreadcontrol-interface.md)
