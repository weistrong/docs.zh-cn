---
description: 了解详细信息： ICorDebugController：： Terminate 方法
title: ICorDebugController::Terminate 方法
ms.date: 03/30/2017
api_name:
- ICorDebugController.Terminate
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Terminate
helpviewer_keywords:
- Terminate method, ICorDebugController interface [.NET Framework debugging]
- ICorDebugController::Terminate method [.NET Framework debugging]
ms.assetid: 4275af0c-b5a7-4e4c-97c9-7e41f36b2dd8
topic_type:
- apiref
ms.openlocfilehash: 15cc832205ebfe86e521d4a45124808e0f3fe128
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710707"
---
# <a name="icordebugcontrollerterminate-method"></a><span data-ttu-id="ae790-103">ICorDebugController::Terminate 方法</span><span class="sxs-lookup"><span data-stu-id="ae790-103">ICorDebugController::Terminate Method</span></span>

<span data-ttu-id="ae790-104">用指定的退出代码终止进程。</span><span class="sxs-lookup"><span data-stu-id="ae790-104">Terminates the process with the specified exit code.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ae790-105">此方法是 Win32 函数的包装器 `TerminateProcess` 。</span><span class="sxs-lookup"><span data-stu-id="ae790-105">This method is a wrapper for the Win32 `TerminateProcess` function.</span></span> <span data-ttu-id="ae790-106">因此， `Terminate` 使用退出代码的方式与 Win32 函数使用的方式相同 `TerminateProcess` 。</span><span class="sxs-lookup"><span data-stu-id="ae790-106">Thus, `Terminate` uses the exit code in the same way that the Win32 `TerminateProcess` function uses it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae790-107">语法</span><span class="sxs-lookup"><span data-stu-id="ae790-107">Syntax</span></span>  
  
```cpp  
HRESULT Terminate (  
    [in] UINT exitCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ae790-108">参数</span><span class="sxs-lookup"><span data-stu-id="ae790-108">Parameters</span></span>  

 `exitCode`  
 <span data-ttu-id="ae790-109">中一个表示退出代码的数字值。</span><span class="sxs-lookup"><span data-stu-id="ae790-109">[in] A numeric value that is the exit code.</span></span> <span data-ttu-id="ae790-110">有效的数值是在 Winbase.h 中定义的。</span><span class="sxs-lookup"><span data-stu-id="ae790-110">The valid numeric values are defined in Winbase.h.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ae790-111">备注</span><span class="sxs-lookup"><span data-stu-id="ae790-111">Remarks</span></span>  

 <span data-ttu-id="ae790-112">如果在调用时停止该进程 `Terminate` ，则应使用 [ICorDebugController：： Continue](icordebugcontroller-continue-method.md) 方法继续此过程，以便调试器通过 [ICorDebugManagedCallback：： ExitProcess](icordebugmanagedcallback-exitprocess-method.md) 或 [ICorDebugManagedCallback：： ExitAppDomain](icordebugmanagedcallback-exitappdomain-method.md) 回调接收终止确认。</span><span class="sxs-lookup"><span data-stu-id="ae790-112">If the process is stopped when `Terminate` is called, the process should be continued by using the [ICorDebugController::Continue](icordebugcontroller-continue-method.md) method so that the debugger receives confirmation of the termination through the [ICorDebugManagedCallback::ExitProcess](icordebugmanagedcallback-exitprocess-method.md) or [ICorDebugManagedCallback::ExitAppDomain](icordebugmanagedcallback-exitappdomain-method.md) callback.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ae790-113">此方法不是由应用程序域实现的。</span><span class="sxs-lookup"><span data-stu-id="ae790-113">This method is not implemented by an application domain.</span></span> <span data-ttu-id="ae790-114">也就是说，它不是在级别实现的 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="ae790-114">That is, it is not implemented at the <xref:System.AppDomain> level.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae790-115">要求</span><span class="sxs-lookup"><span data-stu-id="ae790-115">Requirements</span></span>  

 <span data-ttu-id="ae790-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ae790-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae790-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ae790-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ae790-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ae790-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ae790-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae790-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae790-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="ae790-120">See also</span></span>
