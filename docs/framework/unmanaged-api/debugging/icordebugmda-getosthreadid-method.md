---
description: 了解详细信息： ICorDebugMDA：： GetOSThreadId 方法
title: ICorDebugMDA::GetOSThreadId 方法
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetOSThreadId
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetOSThreadId
helpviewer_keywords:
- ICorDebugMDA::GetOSThreadId method [.NET Framework debugging]
- GetOSThreadId method [.NET Framework debugging]
ms.assetid: 7ca7c364-ade4-4219-b434-9f6ae2359be6
topic_type:
- apiref
ms.openlocfilehash: f965585a6e6060a14f0cbc2a80b46124b2751e0e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801145"
---
# <a name="icordebugmdagetosthreadid-method"></a><span data-ttu-id="9f965-103">ICorDebugMDA::GetOSThreadId 方法</span><span class="sxs-lookup"><span data-stu-id="9f965-103">ICorDebugMDA::GetOSThreadId Method</span></span>

<span data-ttu-id="9f965-104">获取操作系统 (操作系统) 线程标识符，由 [ICorDebugMDA](icordebugmda-interface.md) 表示的托管调试助手 (MDA) 。</span><span class="sxs-lookup"><span data-stu-id="9f965-104">Gets the operating system (OS) thread identifier upon which the managed debugging assistant (MDA) represented by [ICorDebugMDA](icordebugmda-interface.md) is executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f965-105">语法</span><span class="sxs-lookup"><span data-stu-id="9f965-105">Syntax</span></span>  
  
```cpp  
HRESULT GetOSThreadId (  
    [out] DWORD    *pOsTid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9f965-106">参数</span><span class="sxs-lookup"><span data-stu-id="9f965-106">Parameters</span></span>  

 `pOsTid`  
 <span data-ttu-id="9f965-107">弄指向 OS 线程标识符的指针。</span><span class="sxs-lookup"><span data-stu-id="9f965-107">[out] A pointer to the OS thread identifier.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9f965-108">备注</span><span class="sxs-lookup"><span data-stu-id="9f965-108">Remarks</span></span>  

 <span data-ttu-id="9f965-109">使用 OS 线程而不是 ICorDebugThread 来实现以下情况：在本机线程上或在尚未输入托管代码的托管线程上触发 MDA。</span><span class="sxs-lookup"><span data-stu-id="9f965-109">The OS thread is used instead of an ICorDebugThread to allow for situations in which an MDA is fired either on a native thread or on a managed thread that has not yet entered managed code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f965-110">要求</span><span class="sxs-lookup"><span data-stu-id="9f965-110">Requirements</span></span>  

 <span data-ttu-id="9f965-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9f965-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9f965-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9f965-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9f965-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9f965-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9f965-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9f965-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f965-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="9f965-115">See also</span></span>

- [<span data-ttu-id="9f965-116">ICorDebugMDA 接口</span><span class="sxs-lookup"><span data-stu-id="9f965-116">ICorDebugMDA Interface</span></span>](icordebugmda-interface.md)
- [<span data-ttu-id="9f965-117">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="9f965-117">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
