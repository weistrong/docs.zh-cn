---
description: 了解详细信息： MDAInfo 结构
title: MDAInfo 结构
ms.date: 03/30/2017
api_name:
- MDAInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- MDAInfo
helpviewer_keywords:
- MDAInfo structure [.NET Framework hosting]
ms.assetid: fb8c14f7-d461-43d1-8b47-adb6723b9b93
topic_type:
- apiref
ms.openlocfilehash: 5c42537a68d38e6cff3d70dcb796cd733ce64a1e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679740"
---
# <a name="mdainfo-structure"></a><span data-ttu-id="5f15d-103">MDAInfo 结构</span><span class="sxs-lookup"><span data-stu-id="5f15d-103">MDAInfo Structure</span></span>

<span data-ttu-id="5f15d-104">提供有关事件的详细信息 `Event_MDAFired` ，该事件会触发)  (MDA 创建托管调试助手。</span><span class="sxs-lookup"><span data-stu-id="5f15d-104">Provides details about the `Event_MDAFired` event, which triggers the creation of a managed debugging assistant (MDA).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f15d-105">语法</span><span class="sxs-lookup"><span data-stu-id="5f15d-105">Syntax</span></span>  
  
```cpp  
typedef struct _MDAInfo {  
    LPCWSTR  lpMDACaption;  
    LPCWSTR  lpMDAMessage  
} MDAInfo;  
```  
  
## <a name="members"></a><span data-ttu-id="5f15d-106">成员</span><span class="sxs-lookup"><span data-stu-id="5f15d-106">Members</span></span>  
  
|<span data-ttu-id="5f15d-107">成员</span><span class="sxs-lookup"><span data-stu-id="5f15d-107">Member</span></span>|<span data-ttu-id="5f15d-108">说明</span><span class="sxs-lookup"><span data-stu-id="5f15d-108">Description</span></span>|  
|------------|-----------------|  
|`lpMDACaption`|<span data-ttu-id="5f15d-109">当前 MDA 的标题。</span><span class="sxs-lookup"><span data-stu-id="5f15d-109">The title of the current MDA.</span></span> <span data-ttu-id="5f15d-110">标题描述触发事件的故障类型 `Event_MDAFired` 。</span><span class="sxs-lookup"><span data-stu-id="5f15d-110">The title describes the kind of failure that triggered the `Event_MDAFired` event.</span></span>|  
|`lpMDAMessage`|<span data-ttu-id="5f15d-111">当前 MDA 提供的输出消息。</span><span class="sxs-lookup"><span data-stu-id="5f15d-111">The output message provided by the current MDA.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5f15d-112">备注</span><span class="sxs-lookup"><span data-stu-id="5f15d-112">Remarks</span></span>  

 <span data-ttu-id="5f15d-113">托管调试助手 (Mda) 是调试辅助工具，可与公共语言运行时 (CLR) 来执行任务，例如，在运行时执行引擎中标识无效条件或转储有关引擎状态的附加信息。</span><span class="sxs-lookup"><span data-stu-id="5f15d-113">Managed debugging assistants (MDAs) are debugging aids that work in conjunction with the common language runtime (CLR) to perform tasks such as identifying invalid conditions in the runtime execution engine or dumping additional information about the state of the engine.</span></span> <span data-ttu-id="5f15d-114">Mda 生成的 XML 消息与其他难以捕获的事件有关。</span><span class="sxs-lookup"><span data-stu-id="5f15d-114">MDAs generate XML messages about events that are otherwise difficult to trap.</span></span> <span data-ttu-id="5f15d-115">它们对于调试托管代码和非托管代码之间的转换特别有用。</span><span class="sxs-lookup"><span data-stu-id="5f15d-115">They are especially useful for debugging transitions between managed and unmanaged code.</span></span>  
  
 <span data-ttu-id="5f15d-116">触发创建 MDA 的事件时，运行时将执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5f15d-116">The runtime takes the following steps when an event that triggers the creation of an MDA is fired:</span></span>  
  
- <span data-ttu-id="5f15d-117">如果主机尚未通过调用 ICLROnEventManager：： RegisterActionOnEvent 来注册 [IActionOnCLREvent](iactiononclrevent-interface.md) 实例，则会通过调用 [：：](iclroneventmanager-registeractiononevent-method.md) 来接收 `Event_MDAFired` 事件通知，运行时将继续默认的非托管行为。</span><span class="sxs-lookup"><span data-stu-id="5f15d-117">If the host has not registered an [IActionOnCLREvent](iactiononclrevent-interface.md) instance by calling [ICLROnEventManager::RegisterActionOnEvent](iclroneventmanager-registeractiononevent-method.md) to be notified of an `Event_MDAFired` event, the runtime proceeds with its default, non-hosted behavior.</span></span>  
  
- <span data-ttu-id="5f15d-118">如果主机注册了此事件的处理程序，则运行时将进行检查以确定调试器是否已附加到进程。</span><span class="sxs-lookup"><span data-stu-id="5f15d-118">If the host has registered a handler for this event, the runtime checks to see whether a debugger is attached to the process.</span></span> <span data-ttu-id="5f15d-119">如果为，则运行时会中断调试器。</span><span class="sxs-lookup"><span data-stu-id="5f15d-119">If it is, the runtime breaks into the debugger.</span></span> <span data-ttu-id="5f15d-120">调试器继续时，它会调入宿主。</span><span class="sxs-lookup"><span data-stu-id="5f15d-120">When the debugger continues, it calls into the host.</span></span> <span data-ttu-id="5f15d-121">如果未附加调试器，则运行时将调用 `IActionOnCLREvent::OnEvent` 并将一个指针 `MDAInfo` 作为参数传递给实例 `data` 。</span><span class="sxs-lookup"><span data-stu-id="5f15d-121">If no debugger is attached, the runtime calls `IActionOnCLREvent::OnEvent` and passes a pointer to an `MDAInfo` instance as the `data` parameter.</span></span>  
  
 <span data-ttu-id="5f15d-122">宿主可以选择激活 mda，并在激活 MDA 时获得通知。</span><span class="sxs-lookup"><span data-stu-id="5f15d-122">The host can choose to activate MDAs and to be notified when an MDA is activated.</span></span> <span data-ttu-id="5f15d-123">这使宿主有机会覆盖默认行为，并中止引发事件的托管线程，以防止其损坏进程状态。</span><span class="sxs-lookup"><span data-stu-id="5f15d-123">This gives the host an opportunity to override default behavior and to abort the managed thread that raised the event, to prevent it from corrupting the process state.</span></span> <span data-ttu-id="5f15d-124">有关使用 Mda 的详细信息，请参阅 [使用托管调试助手诊断错误](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)。</span><span class="sxs-lookup"><span data-stu-id="5f15d-124">For more information about using MDAs, see [Diagnosing Errors with Managed Debugging Assistants](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5f15d-125">要求</span><span class="sxs-lookup"><span data-stu-id="5f15d-125">Requirements</span></span>  

 <span data-ttu-id="5f15d-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5f15d-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f15d-127">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5f15d-127">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="5f15d-128">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5f15d-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5f15d-129">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f15d-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f15d-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f15d-130">See also</span></span>

- [<span data-ttu-id="5f15d-131">承载结构</span><span class="sxs-lookup"><span data-stu-id="5f15d-131">Hosting Structures</span></span>](hosting-structures.md)
- [<span data-ttu-id="5f15d-132">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="5f15d-132">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
