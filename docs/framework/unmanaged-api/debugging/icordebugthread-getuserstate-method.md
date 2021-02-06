---
description: 了解详细信息： ICorDebugThread：： GetUserState 方法
title: ICorDebugThread::GetUserState 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetUserState
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetUserState
helpviewer_keywords:
- GetUserState method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetUserState method [.NET Framework debugging]
ms.assetid: ae0cfd73-8ead-4d36-9310-dccaac9db0bd
topic_type:
- apiref
ms.openlocfilehash: b63b474525534f9e934954ebe660691db90b8b67
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658862"
---
# <a name="icordebugthreadgetuserstate-method"></a><span data-ttu-id="b78e4-103">ICorDebugThread::GetUserState 方法</span><span class="sxs-lookup"><span data-stu-id="b78e4-103">ICorDebugThread::GetUserState Method</span></span>

<span data-ttu-id="b78e4-104">获取此 ICorDebugThread 的当前用户状态。</span><span class="sxs-lookup"><span data-stu-id="b78e4-104">Gets the current user state of this ICorDebugThread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b78e4-105">语法</span><span class="sxs-lookup"><span data-stu-id="b78e4-105">Syntax</span></span>  
  
```cpp  
HRESULT GetUserState (  
    [out] CorDebugUserState   *pState  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b78e4-106">参数</span><span class="sxs-lookup"><span data-stu-id="b78e4-106">Parameters</span></span>  

 `pState`  
 <span data-ttu-id="b78e4-107">弄一个指针，指向用于描述此线程当前用户状态的 CorDebugUserState 枚举值的按位组合。</span><span class="sxs-lookup"><span data-stu-id="b78e4-107">[out] A pointer to a bitwise combination of CorDebugUserState enumeration values that describe the current user state of this thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b78e4-108">备注</span><span class="sxs-lookup"><span data-stu-id="b78e4-108">Remarks</span></span>  

 <span data-ttu-id="b78e4-109">线程的用户状态是由正在调试的程序检查的线程的状态。</span><span class="sxs-lookup"><span data-stu-id="b78e4-109">The user state of the thread is the state of the thread when it is examined by the program that is being debugged.</span></span> <span data-ttu-id="b78e4-110">线程可能会设置多个状态位。</span><span class="sxs-lookup"><span data-stu-id="b78e4-110">A thread may have multiple state bits set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b78e4-111">要求</span><span class="sxs-lookup"><span data-stu-id="b78e4-111">Requirements</span></span>  

 <span data-ttu-id="b78e4-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b78e4-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b78e4-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b78e4-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b78e4-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b78e4-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b78e4-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b78e4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
