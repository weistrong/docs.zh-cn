---
description: 了解详细信息： ICorDebugThread：： GetHandle 方法
title: ICorDebugThread::GetHandle 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetHandle
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetHandle
helpviewer_keywords:
- GetHandle method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetHandle method [.NET Framework debugging]
ms.assetid: 172ef8c4-2ead-4cfc-bd2e-dee4fb7191cd
topic_type:
- apiref
ms.openlocfilehash: 378bb395e56f0fc287a480d67d2047e082d0796f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659096"
---
# <a name="icordebugthreadgethandle-method"></a><span data-ttu-id="55ec1-103">ICorDebugThread::GetHandle 方法</span><span class="sxs-lookup"><span data-stu-id="55ec1-103">ICorDebugThread::GetHandle Method</span></span>

<span data-ttu-id="55ec1-104">获取此 ICorDebugThread 的活动部分的当前句柄。</span><span class="sxs-lookup"><span data-stu-id="55ec1-104">Gets the current handle for the active part of this ICorDebugThread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55ec1-105">语法</span><span class="sxs-lookup"><span data-stu-id="55ec1-105">Syntax</span></span>  
  
```cpp  
HRESULT GetHandle (  
    [out] HTHREAD *phThreadHandle  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="55ec1-106">参数</span><span class="sxs-lookup"><span data-stu-id="55ec1-106">Parameters</span></span>  

 `phThreadHandle`  
 <span data-ttu-id="55ec1-107">弄指向 HTHREAD 的指针，该指针是此线程的活动部分的句柄。</span><span class="sxs-lookup"><span data-stu-id="55ec1-107">[out] A pointer to an HTHREAD that is the handle of the active part of this thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="55ec1-108">备注</span><span class="sxs-lookup"><span data-stu-id="55ec1-108">Remarks</span></span>  

 <span data-ttu-id="55ec1-109">该句柄可能在进程执行时发生更改，并且可能不同于线程的不同部分。</span><span class="sxs-lookup"><span data-stu-id="55ec1-109">The handle may change as the process executes, and may be different for different parts of the thread.</span></span>  
  
 <span data-ttu-id="55ec1-110">此句柄属于调试 API。</span><span class="sxs-lookup"><span data-stu-id="55ec1-110">This handle is owned by the debugging API.</span></span> <span data-ttu-id="55ec1-111">调试器应在使用之前进行复制。</span><span class="sxs-lookup"><span data-stu-id="55ec1-111">The debugger should duplicate it before using it.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="55ec1-112">要求</span><span class="sxs-lookup"><span data-stu-id="55ec1-112">Requirements</span></span>  

 <span data-ttu-id="55ec1-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="55ec1-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="55ec1-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="55ec1-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="55ec1-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="55ec1-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="55ec1-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="55ec1-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
