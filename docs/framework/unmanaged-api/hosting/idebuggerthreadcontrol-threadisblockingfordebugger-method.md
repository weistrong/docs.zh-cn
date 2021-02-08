---
description: 了解详细信息： IDebuggerThreadControl：： ThreadIsBlockingForDebugger 方法
title: IDebuggerThreadControl::ThreadIsBlockingForDebugger 方法
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.ThreadIsBlockingForDebugger
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ThreadIsBlockingForDebugger
helpviewer_keywords:
- ThreadIsBlockingForDebugger method [.NET Framework hosting]
- IDebuggerThreadControl::ThreadIsBlockingForDebugger method [.NET Framework hosting]
ms.assetid: d4d7cb2d-69da-48b3-879a-1a8a68c9bfa8
topic_type:
- apiref
ms.openlocfilehash: 0fa96b2e36ea6653e1698dd32fa1e73d223afb94
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789510"
---
# <a name="idebuggerthreadcontrolthreadisblockingfordebugger-method"></a><span data-ttu-id="6bfe7-103">IDebuggerThreadControl::ThreadIsBlockingForDebugger 方法</span><span class="sxs-lookup"><span data-stu-id="6bfe7-103">IDebuggerThreadControl::ThreadIsBlockingForDebugger Method</span></span>

<span data-ttu-id="6bfe7-104">向宿主通知发送此回调的线程即将在调试服务中阻止。</span><span class="sxs-lookup"><span data-stu-id="6bfe7-104">Notifies the host that the thread that is sending this callback is about to block within the debugging services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6bfe7-105">语法</span><span class="sxs-lookup"><span data-stu-id="6bfe7-105">Syntax</span></span>  
  
```cpp  
HRESULT ThreadIsBlockingForDebugger ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="6bfe7-106">备注</span><span class="sxs-lookup"><span data-stu-id="6bfe7-106">Remarks</span></span>  

 <span data-ttu-id="6bfe7-107">在 `ThreadIsBlockingForDebugger` 运行时线程上将始终调用方法。</span><span class="sxs-lookup"><span data-stu-id="6bfe7-107">The `ThreadIsBlockingForDebugger` method will always be called on a runtime thread.</span></span>  
  
 <span data-ttu-id="6bfe7-108">`ThreadIsBlockingForDebugger`方法使宿主有机会在线程阻塞时执行另一个操作。</span><span class="sxs-lookup"><span data-stu-id="6bfe7-108">The `ThreadIsBlockingForDebugger` method gives the host an opportunity to perform another action while the thread blocks.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6bfe7-109">要求</span><span class="sxs-lookup"><span data-stu-id="6bfe7-109">Requirements</span></span>  

 <span data-ttu-id="6bfe7-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6bfe7-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6bfe7-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="6bfe7-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6bfe7-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6bfe7-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6bfe7-113">**NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6bfe7-113">**NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6bfe7-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="6bfe7-114">See also</span></span>

- [<span data-ttu-id="6bfe7-115">IDebuggerThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="6bfe7-115">IDebuggerThreadControl Interface</span></span>](idebuggerthreadcontrol-interface.md)
