---
description: 了解详细信息： IAppDomainBinding：： OnAppDomain 方法
title: IAppDomainBinding::OnAppDomain 方法
ms.date: 03/30/2017
api_name:
- IAppDomainBinding.OnAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- OnAppDomain
helpviewer_keywords:
- IAppDomainBinding::OnAppDomain method [.NET Framework hosting]
- OnAppDomain method [.NET Framework hosting]
ms.assetid: b419dcc9-e8aa-484b-af0d-0f40358edb99
topic_type:
- apiref
ms.openlocfilehash: de7f37152261a6fe829026607cf135f3ea0b4a84
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760597"
---
# <a name="iappdomainbindingonappdomain-method"></a><span data-ttu-id="6526e-103">IAppDomainBinding::OnAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="6526e-103">IAppDomainBinding::OnAppDomain Method</span></span>

<span data-ttu-id="6526e-104">由公共语言运行时 (CLR) 调用，以通知宿主已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="6526e-104">Called by the common language runtime (CLR) to notify the host that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6526e-105">语法</span><span class="sxs-lookup"><span data-stu-id="6526e-105">Syntax</span></span>  
  
```cpp  
HRESULT OnAppDomain (  
    [in] IUnknown* pAppdomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6526e-106">参数</span><span class="sxs-lookup"><span data-stu-id="6526e-106">Parameters</span></span>  

 `pAppdomain`  
 <span data-ttu-id="6526e-107">中指向 [IUnknown](/cpp/atl/iunknown) 接口对象的指针，该对象表示新的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="6526e-107">[in] A pointer to an [IUnknown](/cpp/atl/iunknown) interface object that represents the new application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6526e-108">要求</span><span class="sxs-lookup"><span data-stu-id="6526e-108">Requirements</span></span>  

 <span data-ttu-id="6526e-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6526e-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6526e-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="6526e-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6526e-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6526e-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6526e-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6526e-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6526e-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="6526e-113">See also</span></span>

- [<span data-ttu-id="6526e-114">IAppDomainBinding 接口</span><span class="sxs-lookup"><span data-stu-id="6526e-114">IAppDomainBinding Interface</span></span>](iappdomainbinding-interface.md)
