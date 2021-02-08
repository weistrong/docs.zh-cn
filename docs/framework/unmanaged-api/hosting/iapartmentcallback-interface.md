---
description: 了解详细信息： IApartmentCallback 接口
title: IApartmentCallback 接口
ms.date: 03/30/2017
api_name:
- IApartmentCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IApartmentCallback
helpviewer_keywords:
- IApartmentCallback interface [.NET Framework hosting]
ms.assetid: 57c33c58-bf0b-4533-b569-e6a682d02cba
topic_type:
- apiref
ms.openlocfilehash: ddf99b1d926bd2d9765b936143785a975ea378a7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785118"
---
# <a name="iapartmentcallback-interface"></a><span data-ttu-id="a4260-103">IApartmentCallback 接口</span><span class="sxs-lookup"><span data-stu-id="a4260-103">IApartmentCallback Interface</span></span>

<span data-ttu-id="a4260-104">提供用于在单元中进行回调的方法。</span><span class="sxs-lookup"><span data-stu-id="a4260-104">Provides methods for making callbacks within an apartment.</span></span> <span data-ttu-id="a4260-105">*单元* 是进程内共享相同线程访问要求的对象的逻辑容器。</span><span class="sxs-lookup"><span data-stu-id="a4260-105">An *apartment* is a logical container within a process for objects that share the same thread access requirements.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a4260-106">方法</span><span class="sxs-lookup"><span data-stu-id="a4260-106">Methods</span></span>  
  
|<span data-ttu-id="a4260-107">方法</span><span class="sxs-lookup"><span data-stu-id="a4260-107">Method</span></span>|<span data-ttu-id="a4260-108">说明</span><span class="sxs-lookup"><span data-stu-id="a4260-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a4260-109">DoCallback 方法</span><span class="sxs-lookup"><span data-stu-id="a4260-109">DoCallback Method</span></span>](iapartmentcallback-docallback-method.md)|<span data-ttu-id="a4260-110">在单元内执行指定的函数。</span><span class="sxs-lookup"><span data-stu-id="a4260-110">Executes the specified function within an apartment.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a4260-111">要求</span><span class="sxs-lookup"><span data-stu-id="a4260-111">Requirements</span></span>  

 <span data-ttu-id="a4260-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a4260-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a4260-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a4260-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a4260-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a4260-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a4260-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a4260-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a4260-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="a4260-116">See also</span></span>

- [<span data-ttu-id="a4260-117">承载接口</span><span class="sxs-lookup"><span data-stu-id="a4260-117">Hosting Interfaces</span></span>](hosting-interfaces.md)
