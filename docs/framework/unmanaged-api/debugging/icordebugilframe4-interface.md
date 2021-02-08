---
description: 了解详细信息： ICorDebugILFrame4 接口
title: ICorDebugILFrame4 接口
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame4
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 1e739183-3e05-49e5-846f-4075256e41de
topic_type:
- apiref
ms.openlocfilehash: f2d29229f039509ed7799399f0d4d701e8cafba7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791200"
---
# <a name="icordebugilframe4-interface"></a><span data-ttu-id="2d4e2-103">ICorDebugILFrame4 接口</span><span class="sxs-lookup"><span data-stu-id="2d4e2-103">ICorDebugILFrame4 Interface</span></span>

<span data-ttu-id="2d4e2-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="2d4e2-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="2d4e2-105">提供使你能够访问中间语言 (IL) 代码的堆栈帧中的局部变量和代码的方法。</span><span class="sxs-lookup"><span data-stu-id="2d4e2-105">Provides methods that allow you to access the local variables and code in a stack frame of intermediate language (IL) code.</span></span> <span data-ttu-id="2d4e2-106">一个用于指定调试器是否可以访问在探查器 ReJIT 检测中添加的变量和代码的参数。</span><span class="sxs-lookup"><span data-stu-id="2d4e2-106">A parameter specifies whether the debugger has access to variables and code added in profiler ReJIT instrumentation.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2d4e2-107">方法</span><span class="sxs-lookup"><span data-stu-id="2d4e2-107">Methods</span></span>  
  
|<span data-ttu-id="2d4e2-108">方法</span><span class="sxs-lookup"><span data-stu-id="2d4e2-108">Method</span></span>|<span data-ttu-id="2d4e2-109">说明</span><span class="sxs-lookup"><span data-stu-id="2d4e2-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2d4e2-110">EnumerateLocalVariablesEx 方法</span><span class="sxs-lookup"><span data-stu-id="2d4e2-110">EnumerateLocalVariablesEx Method</span></span>](icordebugilframe4-enumeratelocalvariablesex-method.md)|<span data-ttu-id="2d4e2-111">返回在当前帧中可用的局部变量的列表。</span><span class="sxs-lookup"><span data-stu-id="2d4e2-111">Returns a list of the local variables available in the current frame.</span></span>|  
|[<span data-ttu-id="2d4e2-112">GetCodeEx 方法</span><span class="sxs-lookup"><span data-stu-id="2d4e2-112">GetCodeEx Method</span></span>](icordebugilframe4-getcodeex-method.md)|<span data-ttu-id="2d4e2-113">返回此堆栈帧正在运行的代码。</span><span class="sxs-lookup"><span data-stu-id="2d4e2-113">Returns the code that this stack frame is running.</span></span>|  
|[<span data-ttu-id="2d4e2-114">GetLocalVariableEx 方法</span><span class="sxs-lookup"><span data-stu-id="2d4e2-114">GetLocalVariableEx Method</span></span>](icordebugilframe4-getlocalvariableex-method.md)|<span data-ttu-id="2d4e2-115">返回 IL 帧中的局部变量的值。</span><span class="sxs-lookup"><span data-stu-id="2d4e2-115">Returns the value of a local variable in the IL frame.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2d4e2-116">备注</span><span class="sxs-lookup"><span data-stu-id="2d4e2-116">Remarks</span></span>  

 <span data-ttu-id="2d4e2-117">除了 [EnumerateLocalVariables](icordebugilframe-enumeratelocalvariables-method.md)、 [GetCode](icordebugframe-getcode-method.md)和 [GetLocalVariable](icordebugilframe-getlocalvariable-method.md) 方法提供的功能外，这些方法还提供功能。</span><span class="sxs-lookup"><span data-stu-id="2d4e2-117">These methods offer functionality in addition to that provided by the [EnumerateLocalVariables](icordebugilframe-enumeratelocalvariables-method.md), [GetCode](icordebugframe-getcode-method.md), and [GetLocalVariable](icordebugilframe-getlocalvariable-method.md) methods.</span></span> <span data-ttu-id="2d4e2-118">每个方法都包含一个 `flags` 参数，该参数可指定探查器的 ReJIT 请求定义的附加局部变量或代码是否可见。</span><span class="sxs-lookup"><span data-stu-id="2d4e2-118">Each method includes a `flags` parameter that specifies whether additional local variables or code defined by a profiler's ReJIT request are visible.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d4e2-119">要求</span><span class="sxs-lookup"><span data-stu-id="2d4e2-119">Requirements</span></span>  

 <span data-ttu-id="2d4e2-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2d4e2-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d4e2-121">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2d4e2-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2d4e2-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2d4e2-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2d4e2-123">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d4e2-123">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d4e2-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="2d4e2-124">See also</span></span>

- [<span data-ttu-id="2d4e2-125">调试接口</span><span class="sxs-lookup"><span data-stu-id="2d4e2-125">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="2d4e2-126">调试</span><span class="sxs-lookup"><span data-stu-id="2d4e2-126">Debugging</span></span>](index.md)
