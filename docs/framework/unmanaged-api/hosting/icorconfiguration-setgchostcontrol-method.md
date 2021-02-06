---
description: 了解详细信息： ICorConfiguration：： SetGCHostControl 方法
title: ICorConfiguration::SetGCHostControl 方法
ms.date: 03/30/2017
api_name:
- ICorConfiguration.SetGCHostControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetGCHostControl
helpviewer_keywords:
- ICorConfiguration::SetGCHostControl method [.NET Framework hosting]
- SetGCHostControl method [.NET Framework hosting]
ms.assetid: bca6bd79-e288-475a-aa46-6bf81541d966
topic_type:
- apiref
ms.openlocfilehash: 4d3d6e5e5275adf02f9d693234a5c8e77714fd03
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636639"
---
# <a name="icorconfigurationsetgchostcontrol-method"></a><span data-ttu-id="9808f-103">ICorConfiguration::SetGCHostControl 方法</span><span class="sxs-lookup"><span data-stu-id="9808f-103">ICorConfiguration::SetGCHostControl Method</span></span>

<span data-ttu-id="9808f-104">设置垃圾回收器用于请求主机更改虚拟内存限制的回调接口。</span><span class="sxs-lookup"><span data-stu-id="9808f-104">Sets the callback interface to be used by the garbage collector to request the host to change the limits of virtual memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9808f-105">语法</span><span class="sxs-lookup"><span data-stu-id="9808f-105">Syntax</span></span>  
  
```cpp  
HRESULT SetGCHostControl (  
    [in] IGCHostControl* pGCHostControl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9808f-106">参数</span><span class="sxs-lookup"><span data-stu-id="9808f-106">Parameters</span></span>  

 `pGCHostControl`  
 <span data-ttu-id="9808f-107">中指向 [IGCHostControl](igchostcontrol-interface.md) 对象的指针，该对象允许垃圾回收器请求主机更改虚拟内存的限制。</span><span class="sxs-lookup"><span data-stu-id="9808f-107">[in] A pointer to an [IGCHostControl](igchostcontrol-interface.md) object that allows the garbage collector to request the host to change the limits of virtual memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9808f-108">要求</span><span class="sxs-lookup"><span data-stu-id="9808f-108">Requirements</span></span>  

 <span data-ttu-id="9808f-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9808f-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9808f-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9808f-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9808f-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9808f-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9808f-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9808f-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9808f-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="9808f-113">See also</span></span>

- [<span data-ttu-id="9808f-114">ICorConfiguration 接口</span><span class="sxs-lookup"><span data-stu-id="9808f-114">ICorConfiguration Interface</span></span>](icorconfiguration-interface.md)
