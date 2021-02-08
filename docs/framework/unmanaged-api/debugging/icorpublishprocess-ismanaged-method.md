---
description: 了解详细信息： ICorPublishProcess：： IsManaged 方法
title: ICorPublishProcess::IsManaged 方法
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.IsManaged
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::IsManaged
helpviewer_keywords:
- IsManaged method, ICorPublishProcess interface [.NET Framework debugging]
- ICorPublishProcess::IsManaged method [.NET Framework debugging]
ms.assetid: 06b1f7cc-acdf-47a6-9d53-d9dec2424152
topic_type:
- apiref
ms.openlocfilehash: 55f620a896efd87c2f154ac68ef2db1a1b0a1ebc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790498"
---
# <a name="icorpublishprocessismanaged-method"></a><span data-ttu-id="18b0f-103">ICorPublishProcess::IsManaged 方法</span><span class="sxs-lookup"><span data-stu-id="18b0f-103">ICorPublishProcess::IsManaged Method</span></span>

<span data-ttu-id="18b0f-104">获取一个值，该值指示此 [ICorPublishProcess](icorpublishprocess-interface.md) 引用的进程是否已知具有托管代码。</span><span class="sxs-lookup"><span data-stu-id="18b0f-104">Gets a value that indicates whether the process referenced by this [ICorPublishProcess](icorpublishprocess-interface.md) is known to have managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="18b0f-105">语法</span><span class="sxs-lookup"><span data-stu-id="18b0f-105">Syntax</span></span>  
  
```cpp  
HRESULT IsManaged (  
    [out] BOOL   *pbManaged  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="18b0f-106">参数</span><span class="sxs-lookup"><span data-stu-id="18b0f-106">Parameters</span></span>  

 `pbManaged`  
 <span data-ttu-id="18b0f-107">弄一个指向布尔值的指针，该布尔值指示进程是否具有托管代码。</span><span class="sxs-lookup"><span data-stu-id="18b0f-107">[out] A pointer to a Boolean value that indicates whether the process has managed code.</span></span> <span data-ttu-id="18b0f-108">`true`如果进程具有托管代码，则该值为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="18b0f-108">The value is `true` if the process has managed code; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="18b0f-109">备注</span><span class="sxs-lookup"><span data-stu-id="18b0f-109">Remarks</span></span>  

 <span data-ttu-id="18b0f-110">由于的当前版本 `ICorPublishProcess` 只允许访问具有托管代码的进程，因此 `IsManaged` 总是返回 `true` 。</span><span class="sxs-lookup"><span data-stu-id="18b0f-110">Since the current version of `ICorPublishProcess` allows access only to processes that have managed code, `IsManaged` always returns `true`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="18b0f-111">要求</span><span class="sxs-lookup"><span data-stu-id="18b0f-111">Requirements</span></span>  

 <span data-ttu-id="18b0f-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="18b0f-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="18b0f-113">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="18b0f-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="18b0f-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="18b0f-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="18b0f-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="18b0f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="18b0f-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="18b0f-116">See also</span></span>

- [<span data-ttu-id="18b0f-117">ICorPublishProcess 接口</span><span class="sxs-lookup"><span data-stu-id="18b0f-117">ICorPublishProcess Interface</span></span>](icorpublishprocess-interface.md)
