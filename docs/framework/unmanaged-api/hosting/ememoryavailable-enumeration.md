---
description: 了解详细信息： EMemoryAvailable 枚举
title: EMemoryAvailable 枚举
ms.date: 03/30/2017
api_name:
- EMemoryAvailable
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EMemoryAvailable
helpviewer_keywords:
- EMemoryAvailable enumeration [.NET Framework hosting]
ms.assetid: 38e72a06-dbed-473b-a59b-7e0b3ea4f2af
topic_type:
- apiref
ms.openlocfilehash: fdb33b45c354d39b1a52fd815a44041b659181ec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785440"
---
# <a name="ememoryavailable-enumeration"></a><span data-ttu-id="473d2-103">EMemoryAvailable 枚举</span><span class="sxs-lookup"><span data-stu-id="473d2-103">EMemoryAvailable Enumeration</span></span>

<span data-ttu-id="473d2-104">包含指示计算机上的可用物理内存量的值。</span><span class="sxs-lookup"><span data-stu-id="473d2-104">Contains values that indicate the amount of free physical memory on the computer.</span></span> <span data-ttu-id="473d2-105">这些值从逻辑上映射到 Windows API 中从函数返回的高和低内存的事件 `CreateMemoryResourceNotification` 。</span><span class="sxs-lookup"><span data-stu-id="473d2-105">These values logically map to the events for high and low memory returned from the `CreateMemoryResourceNotification` function in the Windows API.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="473d2-106">语法</span><span class="sxs-lookup"><span data-stu-id="473d2-106">Syntax</span></span>  
  
```cpp  
typedef enum {  
    eMemoryAvailableLow     = 1,  
    eMemoryAvailableNeutral = 2,  
    eMemoryAvailableHigh    = 3
} EMemoryAvailable;  
```  
  
## <a name="members"></a><span data-ttu-id="473d2-107">成员</span><span class="sxs-lookup"><span data-stu-id="473d2-107">Members</span></span>  
  
|<span data-ttu-id="473d2-108">成员</span><span class="sxs-lookup"><span data-stu-id="473d2-108">Member</span></span>|<span data-ttu-id="473d2-109">说明</span><span class="sxs-lookup"><span data-stu-id="473d2-109">Description</span></span>|  
|------------|-----------------|  
|`eMemoryAvailableHigh`|<span data-ttu-id="473d2-110">有大量物理内存可用。</span><span class="sxs-lookup"><span data-stu-id="473d2-110">Plenty of physical memory is available.</span></span>|  
|`eMemoryAvailableLow`|<span data-ttu-id="473d2-111">物理内存非常少。</span><span class="sxs-lookup"><span data-stu-id="473d2-111">Very little physical memory is available.</span></span>|  
|`eMemoryAvailableNeutral`|<span data-ttu-id="473d2-112">可用物理内存为中性。</span><span class="sxs-lookup"><span data-stu-id="473d2-112">The available physical memory is neutral.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="473d2-113">备注</span><span class="sxs-lookup"><span data-stu-id="473d2-113">Remarks</span></span>  

 <span data-ttu-id="473d2-114">使用 [ICLRMemoryNotificationCallback：： OnMemoryNotification](iclrmemorynotificationcallback-onmemorynotification-method.md) 方法调用，此值由主机传递到公共语言运行时 (CLR) 。</span><span class="sxs-lookup"><span data-stu-id="473d2-114">This value is passed by the host to the common language runtime (CLR) by using a call to the [ICLRMemoryNotificationCallback::OnMemoryNotification](iclrmemorynotificationcallback-onmemorynotification-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="473d2-115">要求</span><span class="sxs-lookup"><span data-stu-id="473d2-115">Requirements</span></span>  

 <span data-ttu-id="473d2-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="473d2-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="473d2-117">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="473d2-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="473d2-118">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="473d2-118">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="473d2-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="473d2-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="473d2-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="473d2-120">See also</span></span>

- [<span data-ttu-id="473d2-121">承载枚举</span><span class="sxs-lookup"><span data-stu-id="473d2-121">Hosting Enumerations</span></span>](hosting-enumerations.md)
