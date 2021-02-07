---
description: 了解详细信息： WAIT_OPTION 枚举
title: WAIT_OPTION 枚举
ms.date: 03/30/2017
api_name:
- WAIT_OPTION
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- WAIT_OPTION
helpviewer_keywords:
- WAIT_OPTION enumeration [.NET Framework hosting]
ms.assetid: 962fc293-8ded-4b3b-90ce-2c21a4f1b244
topic_type:
- apiref
ms.openlocfilehash: 1d651909e0f62f2db7478a6e0b37139d1f953196
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679129"
---
# <a name="wait_option-enumeration"></a><span data-ttu-id="38dd8-103">WAIT_OPTION 枚举</span><span class="sxs-lookup"><span data-stu-id="38dd8-103">WAIT_OPTION Enumeration</span></span>

<span data-ttu-id="38dd8-104">包含一些值，这些值指示当公共语言运行时 (CLR) 块发出请求的操作时，主机应执行的操作。</span><span class="sxs-lookup"><span data-stu-id="38dd8-104">Contains values that indicate the action a host should take if an operation requested by the common language runtime (CLR) blocks.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38dd8-105">语法</span><span class="sxs-lookup"><span data-stu-id="38dd8-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    WAIT_MSGPUMP       = 0x1,  
    WAIT_ALERTABLE     = 0x2,  
    WAIT_NOTINDEADLOCK = 0x4,  
} WAIT_OPTION;  
```  
  
## <a name="members"></a><span data-ttu-id="38dd8-106">成员</span><span class="sxs-lookup"><span data-stu-id="38dd8-106">Members</span></span>  
  
|<span data-ttu-id="38dd8-107">成员</span><span class="sxs-lookup"><span data-stu-id="38dd8-107">Member</span></span>|<span data-ttu-id="38dd8-108">说明</span><span class="sxs-lookup"><span data-stu-id="38dd8-108">Description</span></span>|  
|------------|-----------------|  
|`WAIT_ALERTABLE`|<span data-ttu-id="38dd8-109">如果 CLR 调用 [IHostTask：： Alert](ihosttask-alert-method.md) 方法，则通知宿主应唤醒任务。</span><span class="sxs-lookup"><span data-stu-id="38dd8-109">Notifies the host that the task should be awakened if the CLR calls the [IHostTask::Alert](ihosttask-alert-method.md) method.</span></span>|  
|`WAIT_MSGPUMP`|<span data-ttu-id="38dd8-110">当线程被阻止时，通知宿主必须在当前 OS 线程上抽取消息。</span><span class="sxs-lookup"><span data-stu-id="38dd8-110">Notifies the host that it must pump messages on the current OS thread if the thread becomes blocked.</span></span> <span data-ttu-id="38dd8-111">运行时仅在线程上指定此值 <xref:System.Threading.ApartmentState.STA> 。</span><span class="sxs-lookup"><span data-stu-id="38dd8-111">The runtime specifies this value only on an <xref:System.Threading.ApartmentState.STA> thread.</span></span>|  
|`WAIT_NOTINDEADLOCK`|<span data-ttu-id="38dd8-112">向宿主通知指定的同步请求无法被宿主中断。</span><span class="sxs-lookup"><span data-stu-id="38dd8-112">Notifies the host that the specified synchronization request cannot be broken by a host.</span></span> <span data-ttu-id="38dd8-113">也就是说，主机无法返回 `HOST_E_DEADLOCK` 。</span><span class="sxs-lookup"><span data-stu-id="38dd8-113">That is, the host cannot return `HOST_E_DEADLOCK`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="38dd8-114">备注</span><span class="sxs-lookup"><span data-stu-id="38dd8-114">Remarks</span></span>  

 <span data-ttu-id="38dd8-115">[IHostTaskManager：： Sleep](ihosttaskmanager-sleep-method.md)和[IHostTaskManager：： SwitchToTask](ihosttaskmanager-switchtotask-method.md)方法都采用此类型的参数。</span><span class="sxs-lookup"><span data-stu-id="38dd8-115">The [IHostTaskManager::Sleep](ihosttaskmanager-sleep-method.md) and [IHostTaskManager::SwitchToTask](ihosttaskmanager-switchtotask-method.md) methods both take a parameter of this type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="38dd8-116">要求</span><span class="sxs-lookup"><span data-stu-id="38dd8-116">Requirements</span></span>  

 <span data-ttu-id="38dd8-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="38dd8-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="38dd8-118">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="38dd8-118">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="38dd8-119">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="38dd8-119">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="38dd8-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="38dd8-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38dd8-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="38dd8-121">See also</span></span>

- [<span data-ttu-id="38dd8-122">承载枚举</span><span class="sxs-lookup"><span data-stu-id="38dd8-122">Hosting Enumerations</span></span>](hosting-enumerations.md)
