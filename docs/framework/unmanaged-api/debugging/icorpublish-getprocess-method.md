---
description: 了解详细信息： ICorPublish：： GetProcess 方法
title: ICorPublish::GetProcess 方法
ms.date: 03/30/2017
api_name:
- ICorPublish.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublish::GetProcess
helpviewer_keywords:
- ICorPublish::GetProcess method [.NET Framework debugging]
- GetProcess method, ICorPublish interface [.NET Framework debugging]
ms.assetid: c5143805-2eb7-45b8-85ed-c8fb34df1084
topic_type:
- apiref
ms.openlocfilehash: d288a772274618cc99b63a68b37e84e543957b44
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721965"
---
# <a name="icorpublishgetprocess-method"></a><span data-ttu-id="0e0ab-103">ICorPublish::GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="0e0ab-103">ICorPublish::GetProcess Method</span></span>

<span data-ttu-id="0e0ab-104">获取一个表示具有指定标识符的进程的 [ICorPublishProcess](icorpublishprocess-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="0e0ab-104">Gets an [ICorPublishProcess](icorpublishprocess-interface.md) instance that represents the process with the specified identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e0ab-105">语法</span><span class="sxs-lookup"><span data-stu-id="0e0ab-105">Syntax</span></span>  
  
```cpp  
HRESULT GetProcess(  
    [in] unsigned              pid,
    [out] ICorPublishProcess   **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0e0ab-106">参数</span><span class="sxs-lookup"><span data-stu-id="0e0ab-106">Parameters</span></span>  

 `pid`  
 <span data-ttu-id="0e0ab-107">中进程的标识符。</span><span class="sxs-lookup"><span data-stu-id="0e0ab-107">[in] The identifier of the process.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="0e0ab-108">弄一个指针，指向 `ICorPublishProcess` 表示进程的实例的地址。</span><span class="sxs-lookup"><span data-stu-id="0e0ab-108">[out] A pointer to the address of an `ICorPublishProcess` instance that represents the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0e0ab-109">备注</span><span class="sxs-lookup"><span data-stu-id="0e0ab-109">Remarks</span></span>  

 <span data-ttu-id="0e0ab-110">`GetProcess` 如果进程不存在，或者不是可由当前用户调试的托管进程，则会失败。</span><span class="sxs-lookup"><span data-stu-id="0e0ab-110">`GetProcess` fails if the process doesn't exist, or isn't a managed process that can be debugged by the current user.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0e0ab-111">要求</span><span class="sxs-lookup"><span data-stu-id="0e0ab-111">Requirements</span></span>  

 <span data-ttu-id="0e0ab-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0e0ab-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0e0ab-113">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="0e0ab-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="0e0ab-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0e0ab-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0e0ab-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0e0ab-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e0ab-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="0e0ab-116">See also</span></span>

- [<span data-ttu-id="0e0ab-117">ICorPublish 接口</span><span class="sxs-lookup"><span data-stu-id="0e0ab-117">ICorPublish Interface</span></span>](icorpublish-interface.md)
