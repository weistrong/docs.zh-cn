---
description: 了解详细信息： INotifySink2 接口
title: INotifySink2 接口
ms.date: 03/30/2017
api_name:
- INotifySink2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySink2
helpviewer_keywords:
- INotifySink2 interface [.NET Framework debugging]
ms.assetid: c1018789-4206-455d-aacc-2d876fc0d0bb
topic_type:
- apiref
ms.openlocfilehash: 4d046c5566d9cb1641426f6a990f39449c33bc4d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800287"
---
# <a name="inotifysink2-interface"></a><span data-ttu-id="221c5-103">INotifySink2 接口</span><span class="sxs-lookup"><span data-stu-id="221c5-103">INotifySink2 Interface</span></span>

<span data-ttu-id="221c5-104">声明接收器通知的方法。</span><span class="sxs-lookup"><span data-stu-id="221c5-104">Declares methods for sink notification.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="221c5-105">方法</span><span class="sxs-lookup"><span data-stu-id="221c5-105">Methods</span></span>  
  
|<span data-ttu-id="221c5-106">方法</span><span class="sxs-lookup"><span data-stu-id="221c5-106">Method</span></span>|<span data-ttu-id="221c5-107">说明</span><span class="sxs-lookup"><span data-stu-id="221c5-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="221c5-108">OnSyncCallEnter 方法</span><span class="sxs-lookup"><span data-stu-id="221c5-108">OnSyncCallEnter Method</span></span>](inotifysink2-onsynccallenter-method.md)|<span data-ttu-id="221c5-109">在输入调用时调用。</span><span class="sxs-lookup"><span data-stu-id="221c5-109">Gets invoked when entering a call.</span></span>|  
|[<span data-ttu-id="221c5-110">OnSyncCallExit 方法</span><span class="sxs-lookup"><span data-stu-id="221c5-110">OnSyncCallExit Method</span></span>](inotifysink2-onsynccallexit-method.md)|<span data-ttu-id="221c5-111">在退出调用时调用。</span><span class="sxs-lookup"><span data-stu-id="221c5-111">Gets invoked when exiting a call.</span></span>|  
|[<span data-ttu-id="221c5-112">OnSyncCallOut 方法</span><span class="sxs-lookup"><span data-stu-id="221c5-112">OnSyncCallOut Method</span></span>](inotifysink2-onsynccallout-method.md)|<span data-ttu-id="221c5-113">在调用时调用。</span><span class="sxs-lookup"><span data-stu-id="221c5-113">Gets invoked when a call is out.</span></span>|  
|[<span data-ttu-id="221c5-114">OnSyncCallReturn 方法</span><span class="sxs-lookup"><span data-stu-id="221c5-114">OnSyncCallReturn Method</span></span>](inotifysink2-onsynccallreturn-method.md)|<span data-ttu-id="221c5-115">当调用返回时调用。</span><span class="sxs-lookup"><span data-stu-id="221c5-115">Gets invoked when a call returns.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="221c5-116">要求</span><span class="sxs-lookup"><span data-stu-id="221c5-116">Requirements</span></span>  

 <span data-ttu-id="221c5-117">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="221c5-117">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="221c5-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="221c5-118">See also</span></span>

- [<span data-ttu-id="221c5-119">INotifyConnection2 接口</span><span class="sxs-lookup"><span data-stu-id="221c5-119">INotifyConnection2 Interface</span></span>](inotifyconnection2-interface.md)
- [<span data-ttu-id="221c5-120">INotifySource2 接口</span><span class="sxs-lookup"><span data-stu-id="221c5-120">INotifySource2 Interface</span></span>](inotifysource2-interface.md)
- [<span data-ttu-id="221c5-121">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="221c5-121">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
