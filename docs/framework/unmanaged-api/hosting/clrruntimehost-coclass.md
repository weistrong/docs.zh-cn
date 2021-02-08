---
description: 了解详细信息： CLRRuntimeHost 组件类
title: CLRRuntimeHost 组件类
ms.date: 03/30/2017
api_name:
- CLRRuntimeHost Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CLRRuntimeHost
helpviewer_keywords:
- CLRRuntimeHost coclass [.NET Framework hosting]
ms.assetid: 2ac9cbf5-8a2d-4e4f-8831-0dad8ef0a897
topic_type:
- apiref
ms.openlocfilehash: a371b9b7263f8bb58b5c513de6647320f000beed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799884"
---
# <a name="clrruntimehost-coclass"></a><span data-ttu-id="85932-103">CLRRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="85932-103">CLRRuntimeHost Coclass</span></span>

<span data-ttu-id="85932-104">提供用于管理运行时执行的代码的接口。</span><span class="sxs-lookup"><span data-stu-id="85932-104">Provides interfaces for managing code execution by the runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="85932-105">语法</span><span class="sxs-lookup"><span data-stu-id="85932-105">Syntax</span></span>  
  
```cpp  
coclass CLRRuntimeHost {  
    [default] interface  ICLRRuntimeHost;  
    interface            ICLRValidator;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="85932-106">界面</span><span class="sxs-lookup"><span data-stu-id="85932-106">Interfaces</span></span>  
  
|<span data-ttu-id="85932-107">接口</span><span class="sxs-lookup"><span data-stu-id="85932-107">Interface</span></span>|<span data-ttu-id="85932-108">说明</span><span class="sxs-lookup"><span data-stu-id="85932-108">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="85932-109">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="85932-109">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)|<span data-ttu-id="85932-110">提供通过运行时控制应用程序执行的方法。</span><span class="sxs-lookup"><span data-stu-id="85932-110">Provides methods for controlling the execution of applications by the runtime.</span></span>|  
|[<span data-ttu-id="85932-111">ICLRValidator 接口</span><span class="sxs-lookup"><span data-stu-id="85932-111">ICLRValidator Interface</span></span>](iclrvalidator-interface.md)|<span data-ttu-id="85932-112">提供可移植可执行映像的验证方法，并提供验证错误的详细报告。</span><span class="sxs-lookup"><span data-stu-id="85932-112">Provides methods for validation of portable executable images and for detailed reporting of validation errors.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="85932-113">要求</span><span class="sxs-lookup"><span data-stu-id="85932-113">Requirements</span></span>  

 <span data-ttu-id="85932-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="85932-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="85932-115">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="85932-115">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="85932-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="85932-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="85932-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="85932-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="85932-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="85932-118">See also</span></span>

- [<span data-ttu-id="85932-119">承载组件类</span><span class="sxs-lookup"><span data-stu-id="85932-119">Hosting Coclasses</span></span>](hosting-coclasses.md)
