---
description: 了解详细信息： CorRuntimeHost 组件类
title: CorRuntimeHost 组件类
ms.date: 03/30/2017
api_name:
- CorRuntimeHost Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorRuntimeHost
helpviewer_keywords:
- CoRuntimeHost coclass [.NET Framework hosting]
ms.assetid: 5833740b-7d67-44b4-865c-b5bf45e291e3
topic_type:
- apiref
ms.openlocfilehash: cd2d01075e5c8264337e1e989b3d9fdc6bf68962
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760631"
---
# <a name="corruntimehost-coclass"></a><span data-ttu-id="0663a-103">CorRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="0663a-103">CorRuntimeHost Coclass</span></span>

<span data-ttu-id="0663a-104">提供用于管理由公共语言运行时执行的应用程序的接口。</span><span class="sxs-lookup"><span data-stu-id="0663a-104">Provides interfaces for managing applications that are being executed by the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0663a-105">语法</span><span class="sxs-lookup"><span data-stu-id="0663a-105">Syntax</span></span>  
  
```cpp  
coclass CorRuntimeHost {  
    [default] interface ICorRuntimeHost;  
    interface IGCHost;  
    interface ICorConfiguration;  
    interface IValidator;  
    interface IDebuggerInfo;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="0663a-106">界面</span><span class="sxs-lookup"><span data-stu-id="0663a-106">Interfaces</span></span>  
  
|<span data-ttu-id="0663a-107">接口</span><span class="sxs-lookup"><span data-stu-id="0663a-107">Interface</span></span>|<span data-ttu-id="0663a-108">说明</span><span class="sxs-lookup"><span data-stu-id="0663a-108">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="0663a-109">ICorConfiguration 接口</span><span class="sxs-lookup"><span data-stu-id="0663a-109">ICorConfiguration Interface</span></span>](icorconfiguration-interface.md)|<span data-ttu-id="0663a-110">提供 (CLR) 配置公共语言运行时的方法。</span><span class="sxs-lookup"><span data-stu-id="0663a-110">Provides methods for configuring the common language runtime (CLR).</span></span>|  
|[<span data-ttu-id="0663a-111">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="0663a-111">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)|<span data-ttu-id="0663a-112">提供使宿主可以显式启动和停止公共语言运行时、创建和配置应用程序域、访问默认域和枚举进程中运行的所有域的方法。</span><span class="sxs-lookup"><span data-stu-id="0663a-112">Provides methods that enable the host to start and stop the common language runtime explicitly, to create and configure application domains, to access the default domain, and to enumerate all domains running in the process.</span></span>|  
|[<span data-ttu-id="0663a-113">IDebuggerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="0663a-113">IDebuggerInfo Interface</span></span>](idebuggerinfo-interface.md)|<span data-ttu-id="0663a-114">提供用于获取有关调试服务状态的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="0663a-114">Provides methods for obtaining information about the state of the debugging services.</span></span>|  
|[<span data-ttu-id="0663a-115">IGCHost 接口</span><span class="sxs-lookup"><span data-stu-id="0663a-115">IGCHost Interface</span></span>](igchost-interface.md)|<span data-ttu-id="0663a-116">提供一些方法，用于获取有关垃圾回收系统的信息并控制垃圾回收的某些方面。</span><span class="sxs-lookup"><span data-stu-id="0663a-116">Provides methods for obtaining information about the garbage collection system and for controlling some aspects of garbage collection.</span></span>|  
|<span data-ttu-id="0663a-117">IValidator</span><span class="sxs-lookup"><span data-stu-id="0663a-117">"IValidator"</span></span>|<span data-ttu-id="0663a-118">提供可移植可执行映像的验证和验证错误的详细报告的方法。</span><span class="sxs-lookup"><span data-stu-id="0663a-118">Provides methods for validation of portable executable images and detailed reporting of validation errors.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0663a-119">要求</span><span class="sxs-lookup"><span data-stu-id="0663a-119">Requirements</span></span>  

 <span data-ttu-id="0663a-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0663a-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0663a-121">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="0663a-121">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="0663a-122">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0663a-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0663a-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0663a-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0663a-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="0663a-124">See also</span></span>

- [<span data-ttu-id="0663a-125">承载组件类</span><span class="sxs-lookup"><span data-stu-id="0663a-125">Hosting Coclasses</span></span>](hosting-coclasses.md)
