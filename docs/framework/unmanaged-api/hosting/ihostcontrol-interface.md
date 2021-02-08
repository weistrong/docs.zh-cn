---
description: 了解详细信息： IHostControl 接口
title: IHostControl 接口
ms.date: 03/30/2017
api_name:
- IHostControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostControl
helpviewer_keywords:
- IHostControl interface [.NET Framework hosting]
ms.assetid: a4ae0d1f-ade9-4b0a-a122-93ed11a5e6b3
topic_type:
- apiref
ms.openlocfilehash: e7a242ed0fdaa734425bec9b48f01fe45cba5182
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789458"
---
# <a name="ihostcontrol-interface"></a><span data-ttu-id="2b380-103">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="2b380-103">IHostControl Interface</span></span>

<span data-ttu-id="2b380-104">提供用于配置程序集加载和确定宿主支持哪些宿主接口的方法。</span><span class="sxs-lookup"><span data-stu-id="2b380-104">Provides methods for configuring the loading of assemblies, and for determining which hosting interfaces the host supports.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2b380-105">方法</span><span class="sxs-lookup"><span data-stu-id="2b380-105">Methods</span></span>  
  
|<span data-ttu-id="2b380-106">方法</span><span class="sxs-lookup"><span data-stu-id="2b380-106">Method</span></span>|<span data-ttu-id="2b380-107">说明</span><span class="sxs-lookup"><span data-stu-id="2b380-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2b380-108">GetHostManager 方法</span><span class="sxs-lookup"><span data-stu-id="2b380-108">GetHostManager Method</span></span>](ihostcontrol-gethostmanager-method.md)|<span data-ttu-id="2b380-109">获取一个接口指针，该指针指向具有指定的接口的主机实现 `IID` 。</span><span class="sxs-lookup"><span data-stu-id="2b380-109">Gets an interface pointer to the host's implementation of the interface with the specified `IID`.</span></span>|  
|[<span data-ttu-id="2b380-110">SetAppDomainManager 方法</span><span class="sxs-lookup"><span data-stu-id="2b380-110">SetAppDomainManager Method</span></span>](ihostcontrol-setappdomainmanager-method.md)|<span data-ttu-id="2b380-111">通知宿主已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="2b380-111">Notifies the host that an application domain has been created.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="2b380-112">要求</span><span class="sxs-lookup"><span data-stu-id="2b380-112">Requirements</span></span>  

 <span data-ttu-id="2b380-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2b380-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2b380-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="2b380-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2b380-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2b380-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2b380-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2b380-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b380-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="2b380-117">See also</span></span>

- <xref:System.AppDomainManager>
- [<span data-ttu-id="2b380-118">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="2b380-118">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)
- [<span data-ttu-id="2b380-119">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="2b380-119">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="2b380-120">承载接口</span><span class="sxs-lookup"><span data-stu-id="2b380-120">Hosting Interfaces</span></span>](hosting-interfaces.md)
