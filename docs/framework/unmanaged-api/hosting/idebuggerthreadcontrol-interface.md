---
description: 了解详细信息： IDebuggerThreadControl 接口
title: IDebuggerThreadControl 接口
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IDebuggerThreadControl
helpviewer_keywords:
- IDebuggerThreadControl interface [.NET Framework hosting]
ms.assetid: 0a270c42-a7d1-45f1-a64d-fa3e84d14532
topic_type:
- apiref
ms.openlocfilehash: 293a120d44b9b04d7e367546c477fb273f535310
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709734"
---
# <a name="idebuggerthreadcontrol-interface"></a><span data-ttu-id="165e3-103">IDebuggerThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="165e3-103">IDebuggerThreadControl Interface</span></span>

<span data-ttu-id="165e3-104">提供一些方法，用于通知宿主调试服务阻止和取消阻止线程。</span><span class="sxs-lookup"><span data-stu-id="165e3-104">Provides methods for notifying the host about the blocking and unblocking of threads by the debugging services.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="165e3-105">方法</span><span class="sxs-lookup"><span data-stu-id="165e3-105">Methods</span></span>  
  
|<span data-ttu-id="165e3-106">方法</span><span class="sxs-lookup"><span data-stu-id="165e3-106">Method</span></span>|<span data-ttu-id="165e3-107">说明</span><span class="sxs-lookup"><span data-stu-id="165e3-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="165e3-108">ThreadIsBlockingForDebugger 方法</span><span class="sxs-lookup"><span data-stu-id="165e3-108">ThreadIsBlockingForDebugger Method</span></span>](idebuggerthreadcontrol-threadisblockingfordebugger-method.md)|<span data-ttu-id="165e3-109">向宿主通知发送此回调的线程即将在调试服务中阻止。</span><span class="sxs-lookup"><span data-stu-id="165e3-109">Notifies the host that the thread that is sending this callback is about to block within the debugging services.</span></span>|  
|[<span data-ttu-id="165e3-110">ReleaseAllRuntimeThreads 方法</span><span class="sxs-lookup"><span data-stu-id="165e3-110">ReleaseAllRuntimeThreads Method</span></span>](idebuggerthreadcontrol-releaseallruntimethreads-method.md)|<span data-ttu-id="165e3-111">向宿主通知调试服务将要释放被阻止的所有线程。</span><span class="sxs-lookup"><span data-stu-id="165e3-111">Notifies the host that the debugging services are about to release all threads that are blocked.</span></span>|  
|[<span data-ttu-id="165e3-112">StartBlockingForDebugger 方法</span><span class="sxs-lookup"><span data-stu-id="165e3-112">StartBlockingForDebugger Method</span></span>](idebuggerthreadcontrol-startblockingfordebugger-method.md)|<span data-ttu-id="165e3-113">通知宿主调试服务即将开始阻塞所有线程。</span><span class="sxs-lookup"><span data-stu-id="165e3-113">Notifies the host that the debugging services are about to start blocking all threads.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="165e3-114">要求</span><span class="sxs-lookup"><span data-stu-id="165e3-114">Requirements</span></span>  

 <span data-ttu-id="165e3-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="165e3-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="165e3-116">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="165e3-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="165e3-117">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="165e3-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="165e3-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="165e3-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="165e3-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="165e3-119">See also</span></span>

- [<span data-ttu-id="165e3-120">承载接口</span><span class="sxs-lookup"><span data-stu-id="165e3-120">Hosting Interfaces</span></span>](hosting-interfaces.md)
