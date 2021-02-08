---
description: 了解详细信息： ETaskType 枚举
title: ETaskType 枚举
ms.date: 03/30/2017
api_name:
- ETaskType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ETaskType
helpviewer_keywords:
- ETaskType enumeration [.NET Framework hosting]
ms.assetid: aa527b31-89d4-41f2-ad6f-63b76950b7df
topic_type:
- apiref
ms.openlocfilehash: 7cb241765b2ff3b4a3402221c6b3e2b7ff6305c1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785397"
---
# <a name="etasktype-enumeration"></a><span data-ttu-id="c5835-103">ETaskType 枚举</span><span class="sxs-lookup"><span data-stu-id="c5835-103">ETaskType Enumeration</span></span>

<span data-ttu-id="c5835-104">包含一些值，这些值指示由 [ICLRTask](iclrtask-interface.md) 或 [IHostTask](ihosttask-interface.md) 接口表示的任务的类型。</span><span class="sxs-lookup"><span data-stu-id="c5835-104">Contains values that indicate the type of task that is represented by either an [ICLRTask](iclrtask-interface.md) or an [IHostTask](ihosttask-interface.md) interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c5835-105">语法</span><span class="sxs-lookup"><span data-stu-id="c5835-105">Syntax</span></span>  
  
```cpp  
typedef enum ETaskType {  
    TT_DEBUGGERHELPER           = 0x1,  
    TT_GC                       = 0x2,  
    TT_FINALIZER                = 0x4,  
    TT_THREADPOOL_TIMER         = 0x8,  
    TT_THREADPOOL_GATE          = 0x10,  
    TT_THREADPOOL_WORKER        = 0x20,  
    TT_THREADPOOL_IOCOMPLETION  = 0x40,  
    TT_ADUNLOAD                 = 0x80,  
    TT_USER                     = 0x100,  
    TT_THREADPOOL_WAIT          = 0x200,  
    TT_UNKNOWN                  = 0x80000000  
} ETaskType;  
```  
  
## <a name="members"></a><span data-ttu-id="c5835-106">成员</span><span class="sxs-lookup"><span data-stu-id="c5835-106">Members</span></span>  
  
|<span data-ttu-id="c5835-107">成员</span><span class="sxs-lookup"><span data-stu-id="c5835-107">Member</span></span>|<span data-ttu-id="c5835-108">说明</span><span class="sxs-lookup"><span data-stu-id="c5835-108">Description</span></span>|  
|------------|-----------------|  
|`TT_ADUNLOAD`|<span data-ttu-id="c5835-109">接口表示应用程序域卸载任务。</span><span class="sxs-lookup"><span data-stu-id="c5835-109">The interface represents an application domain unloading task.</span></span>|  
|`TT_DEBUGGERHELPER`|<span data-ttu-id="c5835-110">接口表示调试器帮助器任务。</span><span class="sxs-lookup"><span data-stu-id="c5835-110">The interface represents a debugger helper task.</span></span>|  
|`TT_FINALIZER`|<span data-ttu-id="c5835-111">接口表示终结器任务。</span><span class="sxs-lookup"><span data-stu-id="c5835-111">The interface represents a finalizer task.</span></span>|  
|`TT_GC`|<span data-ttu-id="c5835-112">接口表示垃圾回收任务。</span><span class="sxs-lookup"><span data-stu-id="c5835-112">The interface represents a garbage collection task.</span></span>|  
|`TT_THREADPOOL_GATE`|<span data-ttu-id="c5835-113">接口表示一个 "入口线程" 任务。</span><span class="sxs-lookup"><span data-stu-id="c5835-113">The interface represents a gate thread task.</span></span>|  
|`TT_THREADPOOL_IOCOMPLETION`|<span data-ttu-id="c5835-114">接口表示 i/o 线程任务或完成端口线程任务。</span><span class="sxs-lookup"><span data-stu-id="c5835-114">The interface represents an I/O thread task or a completion port thread task.</span></span>|  
|`TT_THREADPOOL_TIMER`|<span data-ttu-id="c5835-115">接口表示计时器线程任务。</span><span class="sxs-lookup"><span data-stu-id="c5835-115">The interface represents a timer thread task.</span></span>|  
|`TT_THREADPOOL_WAIT`|<span data-ttu-id="c5835-116">接口表示等待线程任务。</span><span class="sxs-lookup"><span data-stu-id="c5835-116">The interface represents a wait thread task.</span></span>|  
|`TT_THREADPOOL_WORKER`|<span data-ttu-id="c5835-117">接口表示工作线程任务。</span><span class="sxs-lookup"><span data-stu-id="c5835-117">The interface represents a worker thread task.</span></span>|  
|`TT_UNKNOWN`|<span data-ttu-id="c5835-118">任务未知。</span><span class="sxs-lookup"><span data-stu-id="c5835-118">The task is unknown.</span></span>|  
|`TT_USER`|<span data-ttu-id="c5835-119">接口表示用户任务。</span><span class="sxs-lookup"><span data-stu-id="c5835-119">The interface represents a user task.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c5835-120">要求</span><span class="sxs-lookup"><span data-stu-id="c5835-120">Requirements</span></span>  

 <span data-ttu-id="c5835-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c5835-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c5835-122">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c5835-122">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c5835-123">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c5835-123">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c5835-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c5835-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5835-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="c5835-125">See also</span></span>

- [<span data-ttu-id="c5835-126">承载枚举</span><span class="sxs-lookup"><span data-stu-id="c5835-126">Hosting Enumerations</span></span>](hosting-enumerations.md)
