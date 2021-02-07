---
description: 了解详细信息： ICLRErrorReportingManager 接口
title: ICLRErrorReportingManager 接口
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager
helpviewer_keywords:
- ICLRErrorReportingManager interface [.NET Framework hosting]
ms.assetid: ea8af0d5-4133-4472-8a1f-50570d7e85fa
topic_type:
- apiref
ms.openlocfilehash: 094fe52858983fd0e1e5826e823932cb150b6087
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689269"
---
# <a name="iclrerrorreportingmanager-interface"></a><span data-ttu-id="9b3b9-103">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="9b3b9-103">ICLRErrorReportingManager Interface</span></span>

<span data-ttu-id="9b3b9-104">提供允许主机配置自定义堆栈转储以用于错误报告的方法。</span><span class="sxs-lookup"><span data-stu-id="9b3b9-104">Provides methods that allow the host to configure custom stack dumps for error reporting.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9b3b9-105">方法</span><span class="sxs-lookup"><span data-stu-id="9b3b9-105">Methods</span></span>  
  
|<span data-ttu-id="9b3b9-106">方法</span><span class="sxs-lookup"><span data-stu-id="9b3b9-106">Method</span></span>|<span data-ttu-id="9b3b9-107">说明</span><span class="sxs-lookup"><span data-stu-id="9b3b9-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9b3b9-108">BeginCustomDump 方法</span><span class="sxs-lookup"><span data-stu-id="9b3b9-108">BeginCustomDump Method</span></span>](iclrerrorreportingmanager-begincustomdump-method.md)|<span data-ttu-id="9b3b9-109">指定用于错误报告的自定义堆栈转储配置。</span><span class="sxs-lookup"><span data-stu-id="9b3b9-109">Specifies the configuration of custom stack dumps for error reporting.</span></span>|  
|[<span data-ttu-id="9b3b9-110">EndCustomDump 方法</span><span class="sxs-lookup"><span data-stu-id="9b3b9-110">EndCustomDump Method</span></span>](iclrerrorreportingmanager-endcustomdump-method.md)|<span data-ttu-id="9b3b9-111">清除由先前对的调用设置的自定义堆栈转储配置 `BeginCustomDump` 。</span><span class="sxs-lookup"><span data-stu-id="9b3b9-111">Clears the custom stack dump configuration that was set by an earlier call to `BeginCustomDump`.</span></span>|  
|[<span data-ttu-id="9b3b9-112">GetBucketParametersForCurrentException 方法</span><span class="sxs-lookup"><span data-stu-id="9b3b9-112">GetBucketParametersForCurrentException Method</span></span>](iclrerrorreportingmanager-getbucketparametersforcurrentexception-method.md)|<span data-ttu-id="9b3b9-113">获取调用线程上的当前异常的 Watson 存储桶。</span><span class="sxs-lookup"><span data-stu-id="9b3b9-113">Gets the Watson bucket for the current exception on the calling thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9b3b9-114">备注</span><span class="sxs-lookup"><span data-stu-id="9b3b9-114">Remarks</span></span>  

 <span data-ttu-id="9b3b9-115">`BeginCustomDump`方法设置自定义堆栈转储配置。</span><span class="sxs-lookup"><span data-stu-id="9b3b9-115">The `BeginCustomDump` method sets custom stack dump configuration.</span></span> <span data-ttu-id="9b3b9-116">`EndCustomDump`方法清除自定义堆栈转储配置并释放任何关联的状态。</span><span class="sxs-lookup"><span data-stu-id="9b3b9-116">The `EndCustomDump` method clears the custom stack dump configuration and frees any associated state.</span></span> <span data-ttu-id="9b3b9-117">应在自定义转储完成后调用它。</span><span class="sxs-lookup"><span data-stu-id="9b3b9-117">It should be called after the custom dump is complete.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="9b3b9-118">调用失败 `EndCustomDump` 会导致内存泄露。</span><span class="sxs-lookup"><span data-stu-id="9b3b9-118">Failure to call `EndCustomDump` causes memory to leak.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9b3b9-119">要求</span><span class="sxs-lookup"><span data-stu-id="9b3b9-119">Requirements</span></span>  

 <span data-ttu-id="9b3b9-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9b3b9-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9b3b9-121">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9b3b9-121">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9b3b9-122">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9b3b9-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9b3b9-123">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9b3b9-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b3b9-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="9b3b9-124">See also</span></span>

- [<span data-ttu-id="9b3b9-125">ECustomDumpItemKind 枚举</span><span class="sxs-lookup"><span data-stu-id="9b3b9-125">ECustomDumpItemKind Enumeration</span></span>](ecustomdumpitemkind-enumeration.md)
- [<span data-ttu-id="9b3b9-126">承载接口</span><span class="sxs-lookup"><span data-stu-id="9b3b9-126">Hosting Interfaces</span></span>](hosting-interfaces.md)
