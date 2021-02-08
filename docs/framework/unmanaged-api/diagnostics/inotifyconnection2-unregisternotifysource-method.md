---
description: 了解详细信息： INotifyConnection2：： UnregisterNotifySource 方法
title: INotifyConnection2::UnregisterNotifySource 方法
ms.date: 03/30/2017
api_name:
- INotifyConnection2.UnregisterNotifySource
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifyConnection2::UnregisterNotifySource
helpviewer_keywords:
- INotifyConnection2::UnregisterNotifySource method [.NET Framework debugging]
- UnregisterNotifySource method [.NET Framework debugging]
ms.assetid: 2fc6c715-646f-41fd-9c12-c59b40575269
topic_type:
- apiref
ms.openlocfilehash: d3b82665375f54d33b6a5581241788d828060a83
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800300"
---
# <a name="inotifyconnection2unregisternotifysource-method"></a><span data-ttu-id="6bdd3-103">INotifyConnection2::UnregisterNotifySource 方法</span><span class="sxs-lookup"><span data-stu-id="6bdd3-103">INotifyConnection2::UnregisterNotifySource Method</span></span>

<span data-ttu-id="6bdd3-104">从连接中删除指定的通知源对象。</span><span class="sxs-lookup"><span data-stu-id="6bdd3-104">Removes a specified notification source object from the connection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6bdd3-105">语法</span><span class="sxs-lookup"><span data-stu-id="6bdd3-105">Syntax</span></span>  
  
```cpp  
HRESULT UnregisterNotifySource  
(  
    [in]  INotifySource2*  in_pNotifySource  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6bdd3-106">参数</span><span class="sxs-lookup"><span data-stu-id="6bdd3-106">Parameters</span></span>  

 `in_pNotifySource`  
 <span data-ttu-id="6bdd3-107">中要注销的通知对象。</span><span class="sxs-lookup"><span data-stu-id="6bdd3-107">[in] Notification object to be unregistered.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6bdd3-108">返回值</span><span class="sxs-lookup"><span data-stu-id="6bdd3-108">Return Value</span></span>  

 <span data-ttu-id="6bdd3-109">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="6bdd3-109">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6bdd3-110">要求</span><span class="sxs-lookup"><span data-stu-id="6bdd3-110">Requirements</span></span>  

 <span data-ttu-id="6bdd3-111">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="6bdd3-111">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6bdd3-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="6bdd3-112">See also</span></span>

- [<span data-ttu-id="6bdd3-113">INotifyConnection2 接口</span><span class="sxs-lookup"><span data-stu-id="6bdd3-113">INotifyConnection2 Interface</span></span>](inotifyconnection2-interface.md)
- [<span data-ttu-id="6bdd3-114">INotifySource2 接口</span><span class="sxs-lookup"><span data-stu-id="6bdd3-114">INotifySource2 Interface</span></span>](inotifysource2-interface.md)
- [<span data-ttu-id="6bdd3-115">INotifySink2 接口</span><span class="sxs-lookup"><span data-stu-id="6bdd3-115">INotifySink2 Interface</span></span>](inotifysink2-interface.md)
- [<span data-ttu-id="6bdd3-116">RegisterNotifySource 方法</span><span class="sxs-lookup"><span data-stu-id="6bdd3-116">RegisterNotifySource Method</span></span>](inotifyconnection2-registernotifysource-method.md)
