---
description: 了解详细信息： CoInitializeEE 函数
title: CoInitializeEE 函数
ms.date: 03/30/2017
api_name:
- CoInitializeEE
api_location:
- mscoree.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CoInitializeEE
helpviewer_keywords:
- CoInitializeEE function [.NET Framework hosting]
ms.assetid: 7e42a928-5068-4ba6-b8c3-806551a01fa8
topic_type:
- apiref
ms.openlocfilehash: 9664324c569ed4de73262491cf8eda8296b3c3a1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799819"
---
# <a name="coinitializeee-function"></a><span data-ttu-id="ad705-103">CoInitializeEE 函数</span><span class="sxs-lookup"><span data-stu-id="ad705-103">CoInitializeEE Function</span></span>

<span data-ttu-id="ad705-104">确保将公共语言运行时执行引擎加载到进程中。</span><span class="sxs-lookup"><span data-stu-id="ad705-104">Ensures that the common language runtime execution engine is loaded into a process.</span></span> <span data-ttu-id="ad705-105">此函数在 .NET Framework 4 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="ad705-105">This function is deprecated in the .NET Framework 4.</span></span> <span data-ttu-id="ad705-106">改为使用 [ICLRRuntimeHost：： Start](iclrruntimehost-start-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ad705-106">Use the [ICLRRuntimeHost::Start](iclrruntimehost-start-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad705-107">语法</span><span class="sxs-lookup"><span data-stu-id="ad705-107">Syntax</span></span>  
  
```cpp  
HRESULT CoInitializeEE (  
   [in] DWORD fFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ad705-108">参数</span><span class="sxs-lookup"><span data-stu-id="ad705-108">Parameters</span></span>  

 `fFlags`  
 <span data-ttu-id="ad705-109">中 [COINITIEE](../metadata/coinitiee-enumeration.md) 枚举常量之一。</span><span class="sxs-lookup"><span data-stu-id="ad705-109">[in] One of the [COINITIEE](../metadata/coinitiee-enumeration.md) enumeration constants.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ad705-110">返回值</span><span class="sxs-lookup"><span data-stu-id="ad705-110">Return Value</span></span>  

 <span data-ttu-id="ad705-111">此方法返回 Winerror.h 中定义的标准 COM 错误代码，以及下表中的值。</span><span class="sxs-lookup"><span data-stu-id="ad705-111">This method returns standard COM error codes as defined in Winerror.h, and the values in the following table.</span></span>  
  
|<span data-ttu-id="ad705-112">返回代码</span><span class="sxs-lookup"><span data-stu-id="ad705-112">Return code</span></span>|<span data-ttu-id="ad705-113">说明</span><span class="sxs-lookup"><span data-stu-id="ad705-113">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="ad705-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad705-114">S_OK</span></span>|<span data-ttu-id="ad705-115">已成功加载执行引擎。</span><span class="sxs-lookup"><span data-stu-id="ad705-115">The execution engine was loaded successfully.</span></span>|  
|<span data-ttu-id="ad705-116">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ad705-116">S_FALSE</span></span>|<span data-ttu-id="ad705-117">已经加载了执行引擎。</span><span class="sxs-lookup"><span data-stu-id="ad705-117">The execution engine is already loaded.</span></span>|  
|<span data-ttu-id="ad705-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ad705-118">E_FAIL</span></span>|<span data-ttu-id="ad705-119">未能加载执行引擎。</span><span class="sxs-lookup"><span data-stu-id="ad705-119">The execution engine could not be loaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ad705-120">备注</span><span class="sxs-lookup"><span data-stu-id="ad705-120">Remarks</span></span>  

 <span data-ttu-id="ad705-121">此方法加载尚未加载的执行引擎。</span><span class="sxs-lookup"><span data-stu-id="ad705-121">This method loads the execution engine if it has not been previously loaded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ad705-122">要求</span><span class="sxs-lookup"><span data-stu-id="ad705-122">Requirements</span></span>  

 <span data-ttu-id="ad705-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ad705-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ad705-124">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="ad705-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ad705-125">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ad705-125">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ad705-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ad705-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad705-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="ad705-127">See also</span></span>

- [<span data-ttu-id="ad705-128">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="ad705-128">Metadata Global Static Functions</span></span>](../metadata/metadata-global-static-functions.md)
