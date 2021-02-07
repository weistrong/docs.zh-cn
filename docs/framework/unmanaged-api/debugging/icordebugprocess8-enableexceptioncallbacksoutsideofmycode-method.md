---
description: 了解详细信息： ICorDebugProcess8：： EnableExceptionCallbacksOutsideOfMyCode 方法
title: ICorDebugProcess8::EnableExceptionCallbacksOutsideOfMyCode 方法
ms.date: 03/30/2017
dev_langs:
- cpp
ms.assetid: b3af44ec-7d41-425b-aed9-0c4379e5cbe9
ms.openlocfilehash: a85c9d62e5fb62fe620f0901509afa5a03504d4e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691271"
---
# <a name="icordebugprocess8enableexceptioncallbacksoutsideofmycode-method"></a><span data-ttu-id="2a5a4-103">ICorDebugProcess8::EnableExceptionCallbacksOutsideOfMyCode 方法</span><span class="sxs-lookup"><span data-stu-id="2a5a4-103">ICorDebugProcess8::EnableExceptionCallbacksOutsideOfMyCode Method</span></span>

<span data-ttu-id="2a5a4-104">[.NET Framework 4.6 及更高版本中支持]</span><span class="sxs-lookup"><span data-stu-id="2a5a4-104">[Supported in the .NET Framework 4.6 and later versions]</span></span>  
  
 <span data-ttu-id="2a5a4-105">启用或禁用某些类型的 [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) 异常回调。</span><span class="sxs-lookup"><span data-stu-id="2a5a4-105">Enables or disables certain types of [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) exception callbacks.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a5a4-106">语法</span><span class="sxs-lookup"><span data-stu-id="2a5a4-106">Syntax</span></span>  
  
```cpp
HRESULT EnableExceptionCallbacksOutsideOfMyCode(  
   [in] BOOL enableExceptionsOutsideOfJMC  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2a5a4-107">参数</span><span class="sxs-lookup"><span data-stu-id="2a5a4-107">Parameters</span></span>  

 `enableExceptionsOutsideOfJMC`  
 <span data-ttu-id="2a5a4-108">[in]</span><span class="sxs-lookup"><span data-stu-id="2a5a4-108">[in]</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2a5a4-109">备注</span><span class="sxs-lookup"><span data-stu-id="2a5a4-109">Remarks</span></span>  

 <span data-ttu-id="2a5a4-110">如果 `enableExceptionsOutsideOfJMC` 的值是 `false`：</span><span class="sxs-lookup"><span data-stu-id="2a5a4-110">If the value of `enableExceptionsOutsideOfJMC` is `false`:</span></span>  
  
- <span data-ttu-id="2a5a4-111">DEBUG_EXCEPTION_FIRST_CHANCE 异常将不会导致回调到调试器。</span><span class="sxs-lookup"><span data-stu-id="2a5a4-111">A DEBUG_EXCEPTION_FIRST_CHANCE exception will not result in a callback to the debugger.</span></span>  
  
- <span data-ttu-id="2a5a4-112">如果异常不会转义到用户代码（即从异常源到异常处理程序的路径没有被标记为 JustMyCode 或 JMC 的方法），则 DEBUG_EXCEPTION_CATCH_HANDLER_FOUND 异常不会导致回调到调试器。</span><span class="sxs-lookup"><span data-stu-id="2a5a4-112">A DEBUG_EXCEPTION_CATCH_HANDLER_FOUND exception will not result in a callback to the debugger if the exception never escapes into user code (that is, the path from an exception origin to an exception handler has no methods marked as JustMyCode, or JMC).</span></span>  
  
 <span data-ttu-id="2a5a4-113">`enableExceptionsOutsideOfJMC` 的默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="2a5a4-113">The default value of `enableExceptionsOutsideOfJMC` is `true`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2a5a4-114">要求</span><span class="sxs-lookup"><span data-stu-id="2a5a4-114">Requirements</span></span>  

 <span data-ttu-id="2a5a4-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2a5a4-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2a5a4-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2a5a4-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2a5a4-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2a5a4-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2a5a4-118">**.NET Framework 版本：**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2a5a4-118">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a5a4-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="2a5a4-119">See also</span></span>

- [<span data-ttu-id="2a5a4-120">ICorDebugProcess8 接口</span><span class="sxs-lookup"><span data-stu-id="2a5a4-120">ICorDebugProcess8 Interface</span></span>](icordebugprocess8-interface.md)
- [<span data-ttu-id="2a5a4-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="2a5a4-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
