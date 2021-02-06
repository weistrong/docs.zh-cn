---
description: 了解详细信息： ICorDebugThread：： GetID 方法
title: ICorDebugThread::GetID 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetID
helpviewer_keywords:
- ICorDebugThread::GetID method [.NET Framework debugging]
- GetID method, ICorDebugThread interface [.NET Framework debugging]
ms.assetid: f1de4584-92df-42f3-9da4-fca03a1c6821
topic_type:
- apiref
ms.openlocfilehash: d089201527da67299b64cdf074bdd331f22375a1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659070"
---
# <a name="icordebugthreadgetid-method"></a><span data-ttu-id="b994f-103">ICorDebugThread::GetID 方法</span><span class="sxs-lookup"><span data-stu-id="b994f-103">ICorDebugThread::GetID Method</span></span>

<span data-ttu-id="b994f-104">获取此 ICorDebugThread 的活动部分的当前操作系统标识符。</span><span class="sxs-lookup"><span data-stu-id="b994f-104">Gets the current operating system identifier of the active part of this ICorDebugThread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b994f-105">语法</span><span class="sxs-lookup"><span data-stu-id="b994f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetID (  
    [out] DWORD *pdwThreadId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b994f-106">参数</span><span class="sxs-lookup"><span data-stu-id="b994f-106">Parameters</span></span>  

 `pdwThreadId`  
 <span data-ttu-id="b994f-107">弄线程的标识符。</span><span class="sxs-lookup"><span data-stu-id="b994f-107">[out] The identifier of the thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b994f-108">备注</span><span class="sxs-lookup"><span data-stu-id="b994f-108">Remarks</span></span>  

 <span data-ttu-id="b994f-109">操作系统标识符在进程执行期间可能会发生更改，并且可以是线程的不同部分的不同值。</span><span class="sxs-lookup"><span data-stu-id="b994f-109">The operating system identifier can potentially change during execution of a process, and can be a different value for different parts of the thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b994f-110">要求</span><span class="sxs-lookup"><span data-stu-id="b994f-110">Requirements</span></span>  

 <span data-ttu-id="b994f-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b994f-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b994f-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b994f-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b994f-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b994f-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b994f-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b994f-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
