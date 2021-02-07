---
description: 了解详细信息： IValidator 接口
title: IValidator 接口
ms.date: 03/30/2017
api_name:
- IValidator
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IValidator
helpviewer_keywords:
- IValidator interface [.NET Framework hosting]
ms.assetid: b297e3b0-20f9-478f-b707-5e2eecb2b5b2
topic_type:
- apiref
ms.openlocfilehash: bc18b68d0e9a0e978789ab92afaed28751925870
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99680091"
---
# <a name="ivalidator-interface"></a><span data-ttu-id="5292a-103">IValidator 接口</span><span class="sxs-lookup"><span data-stu-id="5292a-103">IValidator Interface</span></span>

<span data-ttu-id="5292a-104">提供用于验证 (PE) 映像和报告验证错误的可移植可执行文件的方法。</span><span class="sxs-lookup"><span data-stu-id="5292a-104">Provides methods for validating portable executable (PE) images and reporting validation errors.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5292a-105">方法</span><span class="sxs-lookup"><span data-stu-id="5292a-105">Methods</span></span>  
  
|<span data-ttu-id="5292a-106">方法</span><span class="sxs-lookup"><span data-stu-id="5292a-106">Method</span></span>|<span data-ttu-id="5292a-107">说明</span><span class="sxs-lookup"><span data-stu-id="5292a-107">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="5292a-108">验证</span><span class="sxs-lookup"><span data-stu-id="5292a-108">Validate</span></span>|<span data-ttu-id="5292a-109">验证指定的 PE 或 Microsoft 中间语言 (MSIL) 文件。</span><span class="sxs-lookup"><span data-stu-id="5292a-109">Validates the specified PE or Microsoft intermediate language (MSIL) file.</span></span>|  
|<span data-ttu-id="5292a-110">FormatEventInfo</span><span class="sxs-lookup"><span data-stu-id="5292a-110">FormatEventInfo</span></span>|<span data-ttu-id="5292a-111">获取与指定的验证错误相对应的错误消息。</span><span class="sxs-lookup"><span data-stu-id="5292a-111">Gets the error message corresponding to the specified validation error.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5292a-112">要求</span><span class="sxs-lookup"><span data-stu-id="5292a-112">Requirements</span></span>  

 <span data-ttu-id="5292a-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5292a-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5292a-114">**标头：** IValidator，IValidator</span><span class="sxs-lookup"><span data-stu-id="5292a-114">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="5292a-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5292a-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5292a-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5292a-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5292a-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="5292a-117">See also</span></span>

- [<span data-ttu-id="5292a-118">承载接口</span><span class="sxs-lookup"><span data-stu-id="5292a-118">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="5292a-119">CorRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="5292a-119">CorRuntimeHost Coclass</span></span>](corruntimehost-coclass.md)
