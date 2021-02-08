---
description: 了解详细信息： INotifySource2：： SetNotifyFilter 方法
title: INotifySource2::SetNotifyFilter 方法
ms.date: 03/30/2017
api_name:
- INotifySource2.SetNotifyFilter
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySource2::SetNotifyFilter
helpviewer_keywords:
- INotifySource2::SetNotifyFilter method [.NET Framework debugging]
- SetNotifyFilter method [.NET Framework debugging]
ms.assetid: 6351fc92-b126-4af6-9bf3-0a8ce92845fc
topic_type:
- apiref
ms.openlocfilehash: 2aaf2a5253f8a9acb67c4b538f109a7a62559d12
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800222"
---
# <a name="inotifysource2setnotifyfilter-method"></a><span data-ttu-id="1f214-103">INotifySource2::SetNotifyFilter 方法</span><span class="sxs-lookup"><span data-stu-id="1f214-103">INotifySource2::SetNotifyFilter Method</span></span>

<span data-ttu-id="1f214-104">分配用于此源的通知筛选器。</span><span class="sxs-lookup"><span data-stu-id="1f214-104">Assigns a notification filter for use with this source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1f214-105">语法</span><span class="sxs-lookup"><span data-stu-id="1f214-105">Syntax</span></span>  
  
```cpp  
HRESULT SetNotifyFilter  
(  
    [in]  NOTIFY_FILTER   in_NotifyFilter,  
    [in]  USER_THREAD*    in_pUserThreadFilter  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1f214-106">参数</span><span class="sxs-lookup"><span data-stu-id="1f214-106">Parameters</span></span>  

 `in_NotifyFilter`  
 <span data-ttu-id="1f214-107">中 [NOTIFY_FILTER](notify-filter-enumeration.md) 枚举值的按位组合，这些值用于标识调试器 API 的回调。</span><span class="sxs-lookup"><span data-stu-id="1f214-107">[in] A bitwise combination of the [NOTIFY_FILTER](notify-filter-enumeration.md) enumeration values that identify callbacks for the debugger API.</span></span>  
  
 `in_pUserThreadFilter`  
 <span data-ttu-id="1f214-108">中一个指针，指向用于标识调试器 API 的线程的 [USER_THREAD](user-thread-structure.md) 结构。</span><span class="sxs-lookup"><span data-stu-id="1f214-108">[in] A pointer to a [USER_THREAD](user-thread-structure.md) structure that identifies threads for the debugger API.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1f214-109">返回值</span><span class="sxs-lookup"><span data-stu-id="1f214-109">Return Value</span></span>  

 <span data-ttu-id="1f214-110">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="1f214-110">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1f214-111">要求</span><span class="sxs-lookup"><span data-stu-id="1f214-111">Requirements</span></span>  

 <span data-ttu-id="1f214-112">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="1f214-112">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1f214-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="1f214-113">See also</span></span>

- [<span data-ttu-id="1f214-114">INotifySource2 接口</span><span class="sxs-lookup"><span data-stu-id="1f214-114">INotifySource2 Interface</span></span>](inotifysource2-interface.md)
- [<span data-ttu-id="1f214-115">INotifyConnection2 接口</span><span class="sxs-lookup"><span data-stu-id="1f214-115">INotifyConnection2 Interface</span></span>](inotifyconnection2-interface.md)
- [<span data-ttu-id="1f214-116">INotifySink2 接口</span><span class="sxs-lookup"><span data-stu-id="1f214-116">INotifySink2 Interface</span></span>](inotifysink2-interface.md)
