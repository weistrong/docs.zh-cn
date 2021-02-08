---
description: 了解详细信息： ICorDebugManagedCallback2：： ChangeConnection 方法
title: ICorDebugManagedCallback2::ChangeConnection 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2.ChangeConnection
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2::ChangeConnection
helpviewer_keywords:
- ICorDebugManagedCallback2::ChangeConnection method [.NET Framework debugging]
- ChangeConnection method [.NET Framework debugging]
ms.assetid: 7263f9a9-4c0b-4d82-a181-288873fb2b18
topic_type:
- apiref
ms.openlocfilehash: 854ea7f40cad9bce613b4034afe7688f4aaf4e52
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790914"
---
# <a name="icordebugmanagedcallback2changeconnection-method"></a><span data-ttu-id="2071c-103">ICorDebugManagedCallback2::ChangeConnection 方法</span><span class="sxs-lookup"><span data-stu-id="2071c-103">ICorDebugManagedCallback2::ChangeConnection Method</span></span>

<span data-ttu-id="2071c-104">通知调试器与指定连接关联的任务集已更改。</span><span class="sxs-lookup"><span data-stu-id="2071c-104">Notifies the debugger that the set of tasks associated with the specified connection has changed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2071c-105">语法</span><span class="sxs-lookup"><span data-stu-id="2071c-105">Syntax</span></span>  
  
```cpp  
HRESULT ChangeConnection (  
    [in] ICorDebugProcess     *pProcess,  
    [in] CONNID               dwConnectionId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2071c-106">参数</span><span class="sxs-lookup"><span data-stu-id="2071c-106">Parameters</span></span>  

 `pProcess`  
 <span data-ttu-id="2071c-107">中一个指向 "ICorDebugProcess" 对象的指针，该对象表示包含已更改的连接的进程。</span><span class="sxs-lookup"><span data-stu-id="2071c-107">[in] A pointer to an "ICorDebugProcess" object that represents the process containing the connection that changed.</span></span>  
  
 `dwConnectionId`  
 <span data-ttu-id="2071c-108">中已更改的连接的 ID。</span><span class="sxs-lookup"><span data-stu-id="2071c-108">[in] The ID of the connection that changed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2071c-109">备注</span><span class="sxs-lookup"><span data-stu-id="2071c-109">Remarks</span></span>  

 <span data-ttu-id="2071c-110">`ChangeConnection`在以下任一情况下，都将激发回调：</span><span class="sxs-lookup"><span data-stu-id="2071c-110">A `ChangeConnection` callback will be fired in either of the following cases:</span></span>  
  
- <span data-ttu-id="2071c-111">调试器附加到包含连接的进程时。</span><span class="sxs-lookup"><span data-stu-id="2071c-111">When a debugger attaches to a process that contains connections.</span></span> <span data-ttu-id="2071c-112">在这种情况下，运行时将为进程中的每个连接生成并调度一个 [ICorDebugManagedCallback2：： CreateConnection](icordebugmanagedcallback2-createconnection-method.md) 事件和一个 `ChangeConnection` 事件。</span><span class="sxs-lookup"><span data-stu-id="2071c-112">In this case, the runtime will generate and dispatch a [ICorDebugManagedCallback2::CreateConnection](icordebugmanagedcallback2-createconnection-method.md) event and a `ChangeConnection` event for each connection in the process.</span></span> <span data-ttu-id="2071c-113">将 `ChangeConnection` 为每个现有连接生成一个事件，而不管该连接的一组任务在创建后是否已更改。</span><span class="sxs-lookup"><span data-stu-id="2071c-113">A `ChangeConnection` event is generated for every existing connection, regardless of whether that connection’s set of tasks has been changed since its creation.</span></span>  
  
- <span data-ttu-id="2071c-114">当主机在[托管 API](../hosting/index.md)中调用[ICLRDebugManager：： SetConnectionTasks](../hosting/iclrdebugmanager-setconnectiontasks-method.md)时。</span><span class="sxs-lookup"><span data-stu-id="2071c-114">When a host calls [ICLRDebugManager::SetConnectionTasks](../hosting/iclrdebugmanager-setconnectiontasks-method.md) in the [Hosting API](../hosting/index.md).</span></span>  
  
 <span data-ttu-id="2071c-115">调试器应扫描进程中的所有线程以选取新的更改。</span><span class="sxs-lookup"><span data-stu-id="2071c-115">The debugger should scan all threads in the process to pick up the new changes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2071c-116">要求</span><span class="sxs-lookup"><span data-stu-id="2071c-116">Requirements</span></span>  

 <span data-ttu-id="2071c-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2071c-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2071c-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2071c-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2071c-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2071c-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2071c-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2071c-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2071c-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="2071c-121">See also</span></span>

- [<span data-ttu-id="2071c-122">ICorDebugManagedCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="2071c-122">ICorDebugManagedCallback2 Interface</span></span>](icordebugmanagedcallback2-interface.md)
- [<span data-ttu-id="2071c-123">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="2071c-123">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
