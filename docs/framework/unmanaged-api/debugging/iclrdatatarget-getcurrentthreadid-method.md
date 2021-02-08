---
description: 了解详细信息： ICLRDataTarget：： GetCurrentThreadID 方法
title: ICLRDataTarget::GetCurrentThreadID 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.GetCurrentThreadID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::GetCurrentThreadID
helpviewer_keywords:
- GetCurrentThreadID method, ICLRDataTarget interface [.NET Framework debugging]
- ICLRDataTarget::GetCurrentThreadID method [.NET Framework debugging]
ms.assetid: dc9a0a6c-d592-4fb7-86ed-62684da3b0e1
topic_type:
- apiref
ms.openlocfilehash: ae1ef00fd6afbecf741d1e4ed215c816dcf6af8f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801353"
---
# <a name="iclrdatatargetgetcurrentthreadid-method"></a><span data-ttu-id="5397e-103">ICLRDataTarget::GetCurrentThreadID 方法</span><span class="sxs-lookup"><span data-stu-id="5397e-103">ICLRDataTarget::GetCurrentThreadID Method</span></span>

<span data-ttu-id="5397e-104">获取当前线程的操作系统标识符。</span><span class="sxs-lookup"><span data-stu-id="5397e-104">Gets the operating system identifier for the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5397e-105">语法</span><span class="sxs-lookup"><span data-stu-id="5397e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentThreadID (  
    [out] ULONG32    *threadID  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5397e-106">参数</span><span class="sxs-lookup"><span data-stu-id="5397e-106">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="5397e-107">弄指向目标进程的当前线程的操作系统标识符的指针。</span><span class="sxs-lookup"><span data-stu-id="5397e-107">[out] A pointer to the operating system identifier of the current thread for the target process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5397e-108">备注</span><span class="sxs-lookup"><span data-stu-id="5397e-108">Remarks</span></span>  

 <span data-ttu-id="5397e-109">如果目标进程没有当前线程，则该 `GetCurrentThreadID` 方法可能失败。</span><span class="sxs-lookup"><span data-stu-id="5397e-109">If there is no current thread for the target process, the `GetCurrentThreadID` method may fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5397e-110">要求</span><span class="sxs-lookup"><span data-stu-id="5397e-110">Requirements</span></span>  

 <span data-ttu-id="5397e-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5397e-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5397e-112">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="5397e-112">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="5397e-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5397e-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5397e-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5397e-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5397e-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="5397e-115">See also</span></span>

- [<span data-ttu-id="5397e-116">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="5397e-116">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
