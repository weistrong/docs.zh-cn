---
description: 了解详细信息： ICLRValidator 接口
title: ICLRValidator 接口
ms.date: 03/30/2017
api_name:
- ICLRValidator
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRValidator
helpviewer_keywords:
- ICLRValidator interface [.NET Framework hosting]
ms.assetid: 2edd0a10-77fb-4173-91eb-f2970cc364d0
topic_type:
- apiref
ms.openlocfilehash: 72ff94915d35967b6a8a87b022789ca697f61711
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636745"
---
# <a name="iclrvalidator-interface"></a><span data-ttu-id="e3f27-103">ICLRValidator 接口</span><span class="sxs-lookup"><span data-stu-id="e3f27-103">ICLRValidator Interface</span></span>

<span data-ttu-id="e3f27-104">提供用于验证 (PE) 映像和报告验证错误的可移植可执行文件的方法。</span><span class="sxs-lookup"><span data-stu-id="e3f27-104">Provides methods for validating portable executable (PE) images and reporting validation errors.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e3f27-105">方法</span><span class="sxs-lookup"><span data-stu-id="e3f27-105">Methods</span></span>  
  
|<span data-ttu-id="e3f27-106">方法</span><span class="sxs-lookup"><span data-stu-id="e3f27-106">Method</span></span>|<span data-ttu-id="e3f27-107">说明</span><span class="sxs-lookup"><span data-stu-id="e3f27-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e3f27-108">FormatEventInfo 方法</span><span class="sxs-lookup"><span data-stu-id="e3f27-108">FormatEventInfo Method</span></span>](iclrvalidator-formateventinfo-method.md)|<span data-ttu-id="e3f27-109">获取有关指定验证错误的详细消息。</span><span class="sxs-lookup"><span data-stu-id="e3f27-109">Gets a detailed message about the specified validation error.</span></span>|  
|[<span data-ttu-id="e3f27-110">Validate 方法</span><span class="sxs-lookup"><span data-stu-id="e3f27-110">Validate Method</span></span>](iclrvalidator-validate-method.md)|<span data-ttu-id="e3f27-111">验证指定文件中的可移植可执行文件或 Microsoft 中间语言 (MSIL) 。</span><span class="sxs-lookup"><span data-stu-id="e3f27-111">Validates the portable executable or Microsoft intermediate language (MSIL) in the specified file.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e3f27-112">要求</span><span class="sxs-lookup"><span data-stu-id="e3f27-112">Requirements</span></span>  

 <span data-ttu-id="e3f27-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e3f27-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e3f27-114">**标头：** IValidator，IValidator</span><span class="sxs-lookup"><span data-stu-id="e3f27-114">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="e3f27-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e3f27-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e3f27-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e3f27-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3f27-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="e3f27-117">See also</span></span>

- [<span data-ttu-id="e3f27-118">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="e3f27-118">ICLRErrorReportingManager Interface</span></span>](iclrerrorreportingmanager-interface.md)
- [<span data-ttu-id="e3f27-119">承载接口</span><span class="sxs-lookup"><span data-stu-id="e3f27-119">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="e3f27-120">CLRRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="e3f27-120">CLRRuntimeHost Coclass</span></span>](clrruntimehost-coclass.md)
