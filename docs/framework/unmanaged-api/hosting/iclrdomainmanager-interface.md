---
description: 了解详细信息： ICLRDomainManager 接口
title: ICLRDomainManager 接口
ms.date: 03/30/2017
api_name:
- ICLRDomainManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDomainManager
helpviewer_keywords:
- ICLRDomainManager interface [.NET Framework hosting]
ms.assetid: f08b2390-d872-4521-a815-e9c237c4c45d
ms.openlocfilehash: d719e89d81e8c7abb1f238ce50b4e236de17ac72
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790004"
---
# <a name="iclrdomainmanager-interface"></a><span data-ttu-id="74d47-103">ICLRDomainManager 接口</span><span class="sxs-lookup"><span data-stu-id="74d47-103">ICLRDomainManager Interface</span></span>

<span data-ttu-id="74d47-104">使宿主能够指定将用于初始化默认应用程序域的应用程序域管理器，并指定初始化属性。</span><span class="sxs-lookup"><span data-stu-id="74d47-104">Enables the host to specify the application domain manager that will be used to initialize the default application domain, and to specify initialization properties.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="74d47-105">方法</span><span class="sxs-lookup"><span data-stu-id="74d47-105">Methods</span></span>  
  
|<span data-ttu-id="74d47-106">方法</span><span class="sxs-lookup"><span data-stu-id="74d47-106">Method</span></span>|<span data-ttu-id="74d47-107">说明</span><span class="sxs-lookup"><span data-stu-id="74d47-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="74d47-108">SetAppDomainManagerType 方法</span><span class="sxs-lookup"><span data-stu-id="74d47-108">SetAppDomainManagerType Method</span></span>](iclrdomainmanager-setappdomainmanagertype-method.md)|<span data-ttu-id="74d47-109">指定从类派生的、 <xref:System.AppDomainManager?displayProperty=nameWithType> 将用于初始化默认应用程序域的应用程序域管理器的类型。</span><span class="sxs-lookup"><span data-stu-id="74d47-109">Specifies the type, derived from the <xref:System.AppDomainManager?displayProperty=nameWithType> class, of the application domain manager that will be used to initialize the default application domain.</span></span>|  
|[<span data-ttu-id="74d47-110">SetPropertiesForDefaultAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="74d47-110">SetPropertiesForDefaultAppDomain Method</span></span>](iclrdomainmanager-setpropertiesfordefaultappdomain-method.md)|<span data-ttu-id="74d47-111">设置将用于初始化默认应用程序域的属性。</span><span class="sxs-lookup"><span data-stu-id="74d47-111">Sets properties that will be used to initialize the default application domain.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="74d47-112">备注</span><span class="sxs-lookup"><span data-stu-id="74d47-112">Remarks</span></span>  

 <span data-ttu-id="74d47-113">若要获取此接口的实例，请使用管理器类型 IID 调用 [ICLRControl：： GetCLRManager](iclrcontrol-getclrmanager-method.md) 方法 `IID_ICLRDomainManager` 。</span><span class="sxs-lookup"><span data-stu-id="74d47-113">To get an instance of this interface, call the [ICLRControl::GetCLRManager](iclrcontrol-getclrmanager-method.md) method with the manager type IID `IID_ICLRDomainManager`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="74d47-114">要求</span><span class="sxs-lookup"><span data-stu-id="74d47-114">Requirements</span></span>  

 <span data-ttu-id="74d47-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="74d47-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="74d47-116">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="74d47-116">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="74d47-117">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="74d47-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="74d47-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="74d47-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74d47-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="74d47-119">See also</span></span>

- [<span data-ttu-id="74d47-120">承载接口</span><span class="sxs-lookup"><span data-stu-id="74d47-120">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="74d47-121">承载</span><span class="sxs-lookup"><span data-stu-id="74d47-121">Hosting</span></span>](index.md)
