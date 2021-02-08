---
description: 了解详细信息： ICorDebugManagedCallback2：:D estroyConnection 方法
title: ICorDebugManagedCallback2::DestroyConnection 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2.DestroyConnection
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2::DestroyConnection
helpviewer_keywords:
- DestroyConnection method [.NET Framework debugging]
- ICorDebugManagedCallback2::DestroyConnection method [.NET Framework debugging]
ms.assetid: cf7940e9-4558-4319-925c-09f6c98c8fcd
topic_type:
- apiref
ms.openlocfilehash: f17def5599dc02ed6b7b49d7f8ed4db02eb40181
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790884"
---
# <a name="icordebugmanagedcallback2destroyconnection-method"></a><span data-ttu-id="dc421-103">ICorDebugManagedCallback2::DestroyConnection 方法</span><span class="sxs-lookup"><span data-stu-id="dc421-103">ICorDebugManagedCallback2::DestroyConnection Method</span></span>

<span data-ttu-id="dc421-104">通知调试器指定的连接已终止。</span><span class="sxs-lookup"><span data-stu-id="dc421-104">Notifies the debugger that the specified connection has been terminated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc421-105">语法</span><span class="sxs-lookup"><span data-stu-id="dc421-105">Syntax</span></span>  
  
```cpp  
HRESULT DestroyConnection (  
    [in] ICorDebugProcess     *pProcess,  
    [in] CONNID               dwConnectionId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dc421-106">参数</span><span class="sxs-lookup"><span data-stu-id="dc421-106">Parameters</span></span>  

 `pProcess`  
 <span data-ttu-id="dc421-107">中指向 ICorDebugProcess 对象的指针，该对象表示包含已销毁的连接的进程。</span><span class="sxs-lookup"><span data-stu-id="dc421-107">[in] A pointer to an ICorDebugProcess object that represents the process containing the connection that was destroyed.</span></span>  
  
 `dwConnectionId`  
 <span data-ttu-id="dc421-108">中已销毁的连接的 ID。</span><span class="sxs-lookup"><span data-stu-id="dc421-108">[in] The ID of the connection that was destroyed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dc421-109">备注</span><span class="sxs-lookup"><span data-stu-id="dc421-109">Remarks</span></span>  

 <span data-ttu-id="dc421-110">`DestroyConnection`当主机在[宿主 API](../hosting/index.md)中调用[ICLRDebugManager：： EndConnection](../hosting/iclrdebugmanager-endconnection-method.md)时，将触发回调。</span><span class="sxs-lookup"><span data-stu-id="dc421-110">A `DestroyConnection` callback will be fired when a host calls [ICLRDebugManager::EndConnection](../hosting/iclrdebugmanager-endconnection-method.md) in the [Hosting API](../hosting/index.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dc421-111">要求</span><span class="sxs-lookup"><span data-stu-id="dc421-111">Requirements</span></span>  

 <span data-ttu-id="dc421-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dc421-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dc421-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="dc421-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="dc421-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dc421-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dc421-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dc421-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc421-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="dc421-116">See also</span></span>

- [<span data-ttu-id="dc421-117">ICorDebugManagedCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="dc421-117">ICorDebugManagedCallback2 Interface</span></span>](icordebugmanagedcallback2-interface.md)
- [<span data-ttu-id="dc421-118">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="dc421-118">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
