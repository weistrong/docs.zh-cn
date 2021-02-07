---
description: 了解详细信息： IAppDomainBinding 接口
title: IAppDomainBinding 接口
ms.date: 03/30/2017
api_name:
- IAppDomainBinding
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IAppDomainBinding
helpviewer_keywords:
- IAppDomainBinding interface [.NET Framework hosting]
ms.assetid: 368881ab-c4ea-4731-bf22-c596aac7c66c
topic_type:
- apiref
ms.openlocfilehash: 3de559af023311f705f9f7dc6eb9785788216a83
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760610"
---
# <a name="iappdomainbinding-interface"></a><span data-ttu-id="d0a4d-103">IAppDomainBinding 接口</span><span class="sxs-lookup"><span data-stu-id="d0a4d-103">IAppDomainBinding Interface</span></span>

<span data-ttu-id="d0a4d-104">提供一个方法，该方法由公共语言运行时 (CLR) ，用于通知宿主应用程序已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="d0a4d-104">Provides a method that is called by the common language runtime (CLR) to notify the host application that an application domain has been created.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d0a4d-105">方法</span><span class="sxs-lookup"><span data-stu-id="d0a4d-105">Methods</span></span>  
  
|<span data-ttu-id="d0a4d-106">方法</span><span class="sxs-lookup"><span data-stu-id="d0a4d-106">Method</span></span>|<span data-ttu-id="d0a4d-107">说明</span><span class="sxs-lookup"><span data-stu-id="d0a4d-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d0a4d-108">OnAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="d0a4d-108">OnAppDomain Method</span></span>](iappdomainbinding-onappdomain-method.md)|<span data-ttu-id="d0a4d-109">由公共语言运行时 (CLR) 调用，以通知宿主已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="d0a4d-109">Called by the common language runtime (CLR) to notify the host that an application domain has been created.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d0a4d-110">要求</span><span class="sxs-lookup"><span data-stu-id="d0a4d-110">Requirements</span></span>  

 <span data-ttu-id="d0a4d-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d0a4d-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d0a4d-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="d0a4d-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d0a4d-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d0a4d-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d0a4d-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d0a4d-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0a4d-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="d0a4d-115">See also</span></span>

- [<span data-ttu-id="d0a4d-116">承载接口</span><span class="sxs-lookup"><span data-stu-id="d0a4d-116">Hosting Interfaces</span></span>](hosting-interfaces.md)
