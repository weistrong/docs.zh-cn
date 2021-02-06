---
description: 了解详细信息： ICorDebugModule2 接口
title: ICorDebugModule2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugModule2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2
helpviewer_keywords:
- ICorDebugModule2 interface [.NET Framework debugging]
ms.assetid: 0847e64f-fdbe-4c96-8168-da20fdc84d80
topic_type:
- apiref
ms.openlocfilehash: 28de1f0d3411218ac92991d4fceda0612c8199bf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659928"
---
# <a name="icordebugmodule2-interface"></a><span data-ttu-id="4caaf-103">ICorDebugModule2 接口</span><span class="sxs-lookup"><span data-stu-id="4caaf-103">ICorDebugModule2 Interface</span></span>

<span data-ttu-id="4caaf-104">用作 ICorDebugModule 接口的逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="4caaf-104">Serves as a logical extension to the ICorDebugModule interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4caaf-105">方法</span><span class="sxs-lookup"><span data-stu-id="4caaf-105">Methods</span></span>  
  
|<span data-ttu-id="4caaf-106">方法</span><span class="sxs-lookup"><span data-stu-id="4caaf-106">Method</span></span>|<span data-ttu-id="4caaf-107">说明</span><span class="sxs-lookup"><span data-stu-id="4caaf-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4caaf-108">ApplyChanges 方法</span><span class="sxs-lookup"><span data-stu-id="4caaf-108">ApplyChanges Method</span></span>](icordebugmodule2-applychanges-method.md)|<span data-ttu-id="4caaf-109">将元数据中的更改和 Microsoft 中间语言 (MSIL) 代码中的更改应用到正在运行的进程。</span><span class="sxs-lookup"><span data-stu-id="4caaf-109">Applies the changes in the metadata and the changes in the Microsoft intermediate language (MSIL) code to the running process.</span></span>|  
|[<span data-ttu-id="4caaf-110">GetJITCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="4caaf-110">GetJITCompilerFlags Method</span></span>](icordebugmodule2-getjitcompilerflags-method.md)|<span data-ttu-id="4caaf-111">获取用于控制此的实时 (JIT) 编译的标志 `ICorDebugModule2` 。</span><span class="sxs-lookup"><span data-stu-id="4caaf-111">Gets the flags that control the just-in-time (JIT) compilation for this `ICorDebugModule2`.</span></span>|  
|[<span data-ttu-id="4caaf-112">ResolveAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="4caaf-112">ResolveAssembly Method</span></span>](icordebugmodule2-resolveassembly-method.md)|<span data-ttu-id="4caaf-113">解析指定的元数据标记所引用的程序集。</span><span class="sxs-lookup"><span data-stu-id="4caaf-113">Resolves the assembly referenced by the specified metadata token.</span></span>|  
|[<span data-ttu-id="4caaf-114">SetJITCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="4caaf-114">SetJITCompilerFlags Method</span></span>](icordebugmodule2-setjitcompilerflags-method.md)|<span data-ttu-id="4caaf-115">设置控制此的 JIT 编译的标志 `ICorDebugModule2` 。</span><span class="sxs-lookup"><span data-stu-id="4caaf-115">Sets the flags that control the JIT compilation for this `ICorDebugModule2`.</span></span>|  
|[<span data-ttu-id="4caaf-116">SetJMCStatus 方法</span><span class="sxs-lookup"><span data-stu-id="4caaf-116">SetJMCStatus Method</span></span>](icordebugmodule2-setjmcstatus-method.md)|<span data-ttu-id="4caaf-117">将此仅我的代码 (的所有类的所有方法的) 状态设置 `ICorDebugModule2` 为指定的值（数组中的所有方法 `pTokens` ，将其设置为相反的值）。</span><span class="sxs-lookup"><span data-stu-id="4caaf-117">Sets the Just My Code (JMC) status of all methods of all the classes in this `ICorDebugModule2` to the specified value, except those in the `pTokens` array, which it sets to the opposite value.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4caaf-118">备注</span><span class="sxs-lookup"><span data-stu-id="4caaf-118">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="4caaf-119">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="4caaf-119">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4caaf-120">要求</span><span class="sxs-lookup"><span data-stu-id="4caaf-120">Requirements</span></span>  

 <span data-ttu-id="4caaf-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4caaf-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4caaf-122">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4caaf-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4caaf-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4caaf-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4caaf-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4caaf-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4caaf-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="4caaf-125">See also</span></span>

- [<span data-ttu-id="4caaf-126">调试接口</span><span class="sxs-lookup"><span data-stu-id="4caaf-126">Debugging Interfaces</span></span>](debugging-interfaces.md)
