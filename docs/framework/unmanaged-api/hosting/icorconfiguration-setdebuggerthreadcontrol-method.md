---
description: 了解详细信息： ICorConfiguration：： SetDebuggerThreadControl 方法
title: ICorConfiguration::SetDebuggerThreadControl 方法
ms.date: 03/30/2017
api_name:
- ICorConfiguration.SetDebuggerThreadControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetDebuggerThreadControl
helpviewer_keywords:
- SetDebuggerThreadControl method [.NET Framework hosting]
- ICorConfiguration::SetDebuggerThreadControl method [.NET Framework hosting]
ms.assetid: 1ded7639-dacb-4db1-961c-d1ceaec01959
topic_type:
- apiref
ms.openlocfilehash: 9bf024f3feb6df44a94f8a5f1a626bb6e0c91d31
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636658"
---
# <a name="icorconfigurationsetdebuggerthreadcontrol-method"></a><span data-ttu-id="8de16-103">ICorConfiguration::SetDebuggerThreadControl 方法</span><span class="sxs-lookup"><span data-stu-id="8de16-103">ICorConfiguration::SetDebuggerThreadControl Method</span></span>

<span data-ttu-id="8de16-104">设置回调接口，调试服务将调用该接口作为公共语言运行时 (CLR) 线程被阻止和取消阻止以进行调试。</span><span class="sxs-lookup"><span data-stu-id="8de16-104">Sets the callback interface that the debugging services will call as common language runtime (CLR) threads are blocked and unblocked for debugging.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8de16-105">语法</span><span class="sxs-lookup"><span data-stu-id="8de16-105">Syntax</span></span>  
  
```cpp  
HRESULT SetDebuggerThreadControl (  
    [in] IDebuggerThreadControl* pDebuggerThreadControl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8de16-106">参数</span><span class="sxs-lookup"><span data-stu-id="8de16-106">Parameters</span></span>  

 `pDebuggerThreadControl`  
 <span data-ttu-id="8de16-107">中指向 [IDebuggerThreadControl](idebuggerthreadcontrol-interface.md) 对象的指针，该对象通知宿主调试服务阻止和取消阻止线程。</span><span class="sxs-lookup"><span data-stu-id="8de16-107">[in] A pointer to an [IDebuggerThreadControl](idebuggerthreadcontrol-interface.md) object that notifies the host about the blocking and unblocking of threads by the debugging services.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8de16-108">要求</span><span class="sxs-lookup"><span data-stu-id="8de16-108">Requirements</span></span>  

 <span data-ttu-id="8de16-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8de16-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8de16-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="8de16-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8de16-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8de16-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8de16-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8de16-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8de16-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="8de16-113">See also</span></span>

- [<span data-ttu-id="8de16-114">ICorConfiguration 接口</span><span class="sxs-lookup"><span data-stu-id="8de16-114">ICorConfiguration Interface</span></span>](icorconfiguration-interface.md)
