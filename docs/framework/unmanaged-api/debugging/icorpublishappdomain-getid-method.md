---
description: 了解详细信息： ICorPublishAppDomain：： GetID 方法
title: ICorPublishAppDomain::GetID 方法
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomain.GetID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomain::GetID
helpviewer_keywords:
- GetID method, ICorPublishAppDomain interface [.NET Framework debugging]
- ICorPublishAppDomain::GetID method [.NET Framework debugging]
ms.assetid: 229437e3-1465-4bd8-8846-9804b2488133
topic_type:
- apiref
ms.openlocfilehash: b3de19c053b5fcce2af5e0036ee6174b01700aac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721835"
---
# <a name="icorpublishappdomaingetid-method"></a><span data-ttu-id="e1ba0-103">ICorPublishAppDomain::GetID 方法</span><span class="sxs-lookup"><span data-stu-id="e1ba0-103">ICorPublishAppDomain::GetID Method</span></span>

<span data-ttu-id="e1ba0-104">获取此 [ICorPublishAppDomain](icorpublishappdomain-interface.md)的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="e1ba0-104">Gets the unique identifier for this [ICorPublishAppDomain](icorpublishappdomain-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e1ba0-105">语法</span><span class="sxs-lookup"><span data-stu-id="e1ba0-105">Syntax</span></span>  
  
```cpp  
HRESULT GetID (  
    [out] ULONG32   *puId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e1ba0-106">参数</span><span class="sxs-lookup"><span data-stu-id="e1ba0-106">Parameters</span></span>  

 `puId`  
 <span data-ttu-id="e1ba0-107">弄指向应用程序域的标识符的指针。</span><span class="sxs-lookup"><span data-stu-id="e1ba0-107">[out] A pointer to the identifier of the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e1ba0-108">备注</span><span class="sxs-lookup"><span data-stu-id="e1ba0-108">Remarks</span></span>  

 <span data-ttu-id="e1ba0-109">标识符仅在包含进程的范围内是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e1ba0-109">The identifier is unique only in the scope of the containing process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e1ba0-110">要求</span><span class="sxs-lookup"><span data-stu-id="e1ba0-110">Requirements</span></span>  

 <span data-ttu-id="e1ba0-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e1ba0-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e1ba0-112">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="e1ba0-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="e1ba0-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e1ba0-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e1ba0-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e1ba0-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1ba0-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="e1ba0-115">See also</span></span>

- [<span data-ttu-id="e1ba0-116">ICorPublishAppDomain 接口</span><span class="sxs-lookup"><span data-stu-id="e1ba0-116">ICorPublishAppDomain Interface</span></span>](icorpublishappdomain-interface.md)
