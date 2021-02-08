---
description: 了解详细信息： ICorDebugManagedCallback2：： CreateConnection 方法
title: ICorDebugManagedCallback2::CreateConnection 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2.CreateConnection
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2::CreateConnection
helpviewer_keywords:
- CreateConnection method [.NET Framework debugging]
- ICorDebugManagedCallback2::CreateConnection method [.NET Framework debugging]
ms.assetid: 49e647be-9d63-4250-9d11-704e2a400d1b
topic_type:
- apiref
ms.openlocfilehash: c7ac91217d43531505dc27a20da9cf4534366119
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790901"
---
# <a name="icordebugmanagedcallback2createconnection-method"></a><span data-ttu-id="48c1e-103">ICorDebugManagedCallback2::CreateConnection 方法</span><span class="sxs-lookup"><span data-stu-id="48c1e-103">ICorDebugManagedCallback2::CreateConnection Method</span></span>

<span data-ttu-id="48c1e-104">通知调试器已创建新连接。</span><span class="sxs-lookup"><span data-stu-id="48c1e-104">Notifies the debugger that a new connection has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="48c1e-105">语法</span><span class="sxs-lookup"><span data-stu-id="48c1e-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateConnection (  
    [in] ICorDebugProcess     *pProcess,  
    [in] CONNID               dwConnectionId,  
    [in] WCHAR                *pConnName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="48c1e-106">参数</span><span class="sxs-lookup"><span data-stu-id="48c1e-106">Parameters</span></span>  

 `pProcess`  
 <span data-ttu-id="48c1e-107">中一个指向 "ICorDebugProcess" 对象的指针，该对象表示在其中创建连接的进程</span><span class="sxs-lookup"><span data-stu-id="48c1e-107">[in] A pointer to an "ICorDebugProcess" object that represents the process in which the connection was created</span></span>  
  
 `dwConnectionId`  
 <span data-ttu-id="48c1e-108">中新连接的 ID。</span><span class="sxs-lookup"><span data-stu-id="48c1e-108">[in] The ID of the new connection.</span></span>  
  
 `pConnName`  
 <span data-ttu-id="48c1e-109">中指向新连接名称的指针。</span><span class="sxs-lookup"><span data-stu-id="48c1e-109">[in] A pointer to the name of the new connection.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="48c1e-110">备注</span><span class="sxs-lookup"><span data-stu-id="48c1e-110">Remarks</span></span>  

 <span data-ttu-id="48c1e-111">`CreateConnection`在以下任一情况下，都将激发回调：</span><span class="sxs-lookup"><span data-stu-id="48c1e-111">A `CreateConnection` callback will be fired in either of the following cases:</span></span>  
  
- <span data-ttu-id="48c1e-112">调试器附加到包含连接的进程时。</span><span class="sxs-lookup"><span data-stu-id="48c1e-112">When a debugger attaches to a process that contains connections.</span></span> <span data-ttu-id="48c1e-113">在这种情况下，运行时将 `CreateConnection` 为进程中的每个连接生成并调度一个事件和一个 [ICorDebugManagedCallback2：： ChangeConnection](icordebugmanagedcallback2-changeconnection-method.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="48c1e-113">In this case, the runtime will generate and dispatch a `CreateConnection` event and a [ICorDebugManagedCallback2::ChangeConnection](icordebugmanagedcallback2-changeconnection-method.md) event for each connection in the process.</span></span>  
  
- <span data-ttu-id="48c1e-114">当主机在[托管 API](../hosting/index.md)中调用[ICLRDebugManager：： BeginConnection](../hosting/iclrdebugmanager-beginconnection-method.md)时。</span><span class="sxs-lookup"><span data-stu-id="48c1e-114">When a host calls [ICLRDebugManager::BeginConnection](../hosting/iclrdebugmanager-beginconnection-method.md) in the [Hosting API](../hosting/index.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="48c1e-115">要求</span><span class="sxs-lookup"><span data-stu-id="48c1e-115">Requirements</span></span>  

 <span data-ttu-id="48c1e-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="48c1e-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="48c1e-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="48c1e-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="48c1e-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="48c1e-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="48c1e-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="48c1e-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48c1e-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="48c1e-120">See also</span></span>

- [<span data-ttu-id="48c1e-121">ICorDebugManagedCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="48c1e-121">ICorDebugManagedCallback2 Interface</span></span>](icordebugmanagedcallback2-interface.md)
- [<span data-ttu-id="48c1e-122">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="48c1e-122">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
