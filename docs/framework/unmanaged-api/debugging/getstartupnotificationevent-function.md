---
description: 了解详细信息： GetStartupNotificationEvent 函数
title: GetStartupNotificationEvent 函数
ms.date: 03/30/2017
api_name:
- GetStartupNotificationEvent
api_location:
- dbgshim.dll
api_type:
- COM
f1_keywords:
- GetStartupNotificationEvent
helpviewer_keywords:
- GetStartupNotificationEvent function
- debugging API [Silverlight]
- Silverlight, debugging
ms.assetid: c94b1b61-045a-4695-bacd-0f18c5acc246
topic_type:
- apiref
ms.openlocfilehash: 49b0e3f9b2acec87e419bae03086a7e437f45f98
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801379"
---
# <a name="getstartupnotificationevent-function"></a><span data-ttu-id="7f0e0-103">GetStartupNotificationEvent 函数</span><span class="sxs-lookup"><span data-stu-id="7f0e0-103">GetStartupNotificationEvent Function</span></span>

<span data-ttu-id="7f0e0-104">创建或打开一个事件句柄，由在指定目标进程中加载的公共语言运行时 (CLR) 对其发出信号。</span><span class="sxs-lookup"><span data-stu-id="7f0e0-104">Creates or opens an event handle that will be signaled upon by any common language runtime (CLR) that is loading in the specified target process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f0e0-105">语法</span><span class="sxs-lookup"><span data-stu-id="7f0e0-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStartupNotificationEvent  
    (  
    [in]  DWORD     debuggeePID,  
    [out]  HANDLE*  phStartupEvent  
    );  
```  
  
## <a name="parameters"></a><span data-ttu-id="7f0e0-106">参数</span><span class="sxs-lookup"><span data-stu-id="7f0e0-106">Parameters</span></span>  

 `debuggeePID`  
 <span data-ttu-id="7f0e0-107">[in] 从其中接收 CLR 启动通知的目标进程的进程标识符。</span><span class="sxs-lookup"><span data-stu-id="7f0e0-107">[in] Process identifier of the target process from which to receive CLR startup notifications.</span></span>  
  
 `phStartupEvent`  
 <span data-ttu-id="7f0e0-108">[out] 指向在启动时由 CLR 发出信号通知的句柄的指针。</span><span class="sxs-lookup"><span data-stu-id="7f0e0-108">[out] A pointer to a handle that will be signaled by a CLR on startup.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7f0e0-109">返回值</span><span class="sxs-lookup"><span data-stu-id="7f0e0-109">Return Value</span></span>  

 <span data-ttu-id="7f0e0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f0e0-110">S_OK</span></span>  
 <span data-ttu-id="7f0e0-111">成功获取启动通知事件的句柄。</span><span class="sxs-lookup"><span data-stu-id="7f0e0-111">Successfully obtained the handle to the startup notification event.</span></span>  
  
 <span data-ttu-id="7f0e0-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7f0e0-112">E_INVALIDARG</span></span>  
 <span data-ttu-id="7f0e0-113">`phStartupEvent` 为 null 或 `debuggeePID` 不引用当前正在运行的进程。</span><span class="sxs-lookup"><span data-stu-id="7f0e0-113">`phStartupEvent` is null or `debuggeePID` does not refer to a process that is currently running.</span></span>  
  
 <span data-ttu-id="7f0e0-114">E_FAIL（或其他 E_ 返回代码）</span><span class="sxs-lookup"><span data-stu-id="7f0e0-114">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="7f0e0-115">无法获取启动通知事件的句柄。</span><span class="sxs-lookup"><span data-stu-id="7f0e0-115">Unable to obtain the handle to the startup notification event.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7f0e0-116">备注</span><span class="sxs-lookup"><span data-stu-id="7f0e0-116">Remarks</span></span>  

 <span data-ttu-id="7f0e0-117">在 Windows 操作系统上，`debuggeePID` 映射到 OS 进程标识符。</span><span class="sxs-lookup"><span data-stu-id="7f0e0-117">On the Windows operating system, `debuggeePID` maps to an OS process identifier.</span></span>  
  
 <span data-ttu-id="7f0e0-118">在发出信号通知事件的 CLR 执行任何托管代码之前，对该事件发出了信号。</span><span class="sxs-lookup"><span data-stu-id="7f0e0-118">The event is signaled before any managed code is executed by the CLR that signaled the event.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f0e0-119">要求</span><span class="sxs-lookup"><span data-stu-id="7f0e0-119">Requirements</span></span>  

 <span data-ttu-id="7f0e0-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7f0e0-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7f0e0-121">**标头：** dbgshim.dll</span><span class="sxs-lookup"><span data-stu-id="7f0e0-121">**Header:** dbgshim.h</span></span>  
  
 <span data-ttu-id="7f0e0-122">**库：** dbgshim.dll</span><span class="sxs-lookup"><span data-stu-id="7f0e0-122">**Library:** dbgshim.dll</span></span>  
  
 <span data-ttu-id="7f0e0-123">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="7f0e0-123">**.NET Framework Versions:** 3.5 SP1</span></span>
