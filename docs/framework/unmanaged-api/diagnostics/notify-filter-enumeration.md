---
description: 了解详细信息： NOTIFY_FILTER 枚举
title: NOTIFY_FILTER 枚举
ms.date: 03/30/2017
api_name:
- NOTIFY_FILTER
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- NOTIFY_FILTER
helpviewer_keywords:
- NOTIFY_FILTER enumeration [.NET Framework debugging]
ms.assetid: 4789d08f-8683-45d3-ac30-73d48c61e470
topic_type:
- apiref
ms.openlocfilehash: 0ed09af0af302b08102b7b08fa72a2d255c5b231
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761481"
---
# <a name="notify_filter-enumeration"></a><span data-ttu-id="de546-103">NOTIFY_FILTER 枚举</span><span class="sxs-lookup"><span data-stu-id="de546-103">NOTIFY_FILTER Enumeration</span></span>

<span data-ttu-id="de546-104">标识调试器函数的回调。</span><span class="sxs-lookup"><span data-stu-id="de546-104">Identifies callbacks for debugger functions.</span></span> <span data-ttu-id="de546-105">有关详细信息，请参阅 [INotifySource2：： SetNotifyFilter](inotifysource2-setnotifyfilter-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="de546-105">For more information, see the [INotifySource2::SetNotifyFilter](inotifysource2-setnotifyfilter-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de546-106">语法</span><span class="sxs-lookup"><span data-stu-id="de546-106">Syntax</span></span>  
  
```cpp  
enum tagNOTIFY_FILTER  
{  
    NOTIFY_FILTER_ONSYNCCALLOUT    = 0x1,  
    NOTIFY_FILTER_ONSYNCCALLENTER  = 0x2,  
    NOTIFY_FILTER_ONSYNCCALLEXIT   = 0x4,  
    NOTIFY_FILTER_ONSYNCCALLRETURN = 0x8,  
    NOTIFY_FILTER_ALLSYNC = NOTIFY_FILTER_ONSYNCCALLOUT | NOTIFY_FILTER_ONSYNCCALLENTER | NOTIFY_FILTER_ONSYNCCALLEXIT | NOTIFY_FILTER_ONSYNCCALLRETURN,  
    NOTIFY_FILTER_ALL              = 0xffffffff,  
    NOTIFY_FILTER_NONE             = 0  
};  
```  
  
## <a name="members"></a><span data-ttu-id="de546-107">成员</span><span class="sxs-lookup"><span data-stu-id="de546-107">Members</span></span>  
  
|<span data-ttu-id="de546-108">成员</span><span class="sxs-lookup"><span data-stu-id="de546-108">Member</span></span>|<span data-ttu-id="de546-109">说明</span><span class="sxs-lookup"><span data-stu-id="de546-109">Description</span></span>|  
|------------|-----------------|  
|`NOTIFY_FILTER_ONSYNCCALLOUT`|<span data-ttu-id="de546-110">指示应调用 [INotifySink2：： OnSyncCallOut](inotifysink2-onsynccallout-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="de546-110">Indicates that the [INotifySink2::OnSyncCallOut](inotifysink2-onsynccallout-method.md) method should be invoked.</span></span>|  
|`NOTIFY_FILTER_ONSYNCCALLENTER`|<span data-ttu-id="de546-111">指示应调用 [INotifySink2：： OnSyncCallEnter](inotifysink2-onsynccallenter-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="de546-111">Indicates that the [INotifySink2::OnSyncCallEnter](inotifysink2-onsynccallenter-method.md) method should be invoked.</span></span>|  
|`NOTIFY_FILTER_ONSYNCCALLEXIT`|<span data-ttu-id="de546-112">指示应调用 [INotifySink2：： OnSyncCallExit](inotifysink2-onsynccallexit-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="de546-112">Indicates that the [INotifySink2::OnSyncCallExit](inotifysink2-onsynccallexit-method.md) method should be invoked.</span></span>|  
|`NOTIFY_FILTER_ONSYNCCALLRETURN`|<span data-ttu-id="de546-113">指示应调用 [INotifySink2：： OnSyncCallReturn](inotifysink2-onsynccallreturn-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="de546-113">Indicates that the [INotifySink2::OnSyncCallReturn](inotifysink2-onsynccallreturn-method.md) method should be invoked.</span></span>|  
|`NOTIFY_FILTER_ALLSYNC`|<span data-ttu-id="de546-114">指示应调用所有 [INotifySink2](inotifysink2-interface.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="de546-114">Indicates that all of the [INotifySink2](inotifysink2-interface.md) methods should be invoked.</span></span>|  
|`NOTIFY_FILTER_ALL`|<span data-ttu-id="de546-115">激活所有现有和未来的通知。</span><span class="sxs-lookup"><span data-stu-id="de546-115">Activates all existing and future notifications.</span></span>|  
|`NOTIFY_FILTER_NONE`|<span data-ttu-id="de546-116">指示不应调用任何通知方法。</span><span class="sxs-lookup"><span data-stu-id="de546-116">Indicates that no notification methods should be invoked.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="de546-117">要求</span><span class="sxs-lookup"><span data-stu-id="de546-117">Requirements</span></span>  

 <span data-ttu-id="de546-118">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="de546-118">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de546-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="de546-119">See also</span></span>

- [<span data-ttu-id="de546-120">诊断符号存储区枚举</span><span class="sxs-lookup"><span data-stu-id="de546-120">Diagnostics Symbol Store Enumerations</span></span>](diagnostics-symbol-store-enumerations.md)
