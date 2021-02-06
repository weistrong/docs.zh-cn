---
description: 了解详细信息： ICorDebugModule 接口
title: ICorDebugModule 接口
ms.date: 03/30/2017
api_name:
- ICorDebugModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule
helpviewer_keywords:
- ICorDebugModule interface [.NET Framework debugging]
ms.assetid: 32e4d6fa-e5a3-413e-9166-d5e2871d3114
topic_type:
- apiref
ms.openlocfilehash: f78023fe9975b609309c1c511380a3a394426283
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660110"
---
# <a name="icordebugmodule-interface"></a><span data-ttu-id="a5c43-103">ICorDebugModule 接口</span><span class="sxs-lookup"><span data-stu-id="a5c43-103">ICorDebugModule Interface</span></span>

<span data-ttu-id="a5c43-104">表示公共语言运行时 (CLR) 模块，该模块可以是可执行文件或动态链接库 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="a5c43-104">Represents a common language runtime (CLR) module, which is either an executable file or a dynamic-link library (DLL).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a5c43-105">方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-105">Methods</span></span>  
  
|<span data-ttu-id="a5c43-106">方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-106">Method</span></span>|<span data-ttu-id="a5c43-107">说明</span><span class="sxs-lookup"><span data-stu-id="a5c43-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a5c43-108">CreateBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-108">CreateBreakpoint Method</span></span>](icordebugmodule-createbreakpoint-method.md)|<span data-ttu-id="a5c43-109">未实现。</span><span class="sxs-lookup"><span data-stu-id="a5c43-109">Not implemented.</span></span>|  
|[<span data-ttu-id="a5c43-110">EnableClassLoadCallbacks 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-110">EnableClassLoadCallbacks Method</span></span>](icordebugmodule-enableclassloadcallbacks-method.md)|<span data-ttu-id="a5c43-111">确定是否为此模块调用 [ICorDebugManagedCallback：： LoadClass](icordebugmanagedcallback-loadclass-method.md) 和 [ICorDebugManagedCallback：： UnloadClass](icordebugmanagedcallback-unloadclass-method.md) 回调。</span><span class="sxs-lookup"><span data-stu-id="a5c43-111">Determines whether the [ICorDebugManagedCallback::LoadClass](icordebugmanagedcallback-loadclass-method.md) and [ICorDebugManagedCallback::UnloadClass](icordebugmanagedcallback-unloadclass-method.md) callbacks are called for this module.</span></span>|  
|[<span data-ttu-id="a5c43-112">EnableJITDebugging 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-112">EnableJITDebugging Method</span></span>](icordebugmodule-enablejitdebugging-method.md)|<span data-ttu-id="a5c43-113">确定实时 (JIT) 编译器是否保留此模块内方法的调试信息。</span><span class="sxs-lookup"><span data-stu-id="a5c43-113">Determines whether the just-in-time (JIT) compiler preserves debugging information for methods within this module.</span></span>|  
|[<span data-ttu-id="a5c43-114">GetAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-114">GetAssembly Method</span></span>](icordebugmodule-getassembly-method.md)|<span data-ttu-id="a5c43-115">获取包含此模块的程序集。</span><span class="sxs-lookup"><span data-stu-id="a5c43-115">Gets the containing assembly for this module.</span></span>|  
|[<span data-ttu-id="a5c43-116">GetBaseAddress 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-116">GetBaseAddress Method</span></span>](icordebugmodule-getbaseaddress-method.md)|<span data-ttu-id="a5c43-117">获取模块的基址。</span><span class="sxs-lookup"><span data-stu-id="a5c43-117">Gets the base address of the module.</span></span>|  
|[<span data-ttu-id="a5c43-118">GetClassFromToken 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-118">GetClassFromToken Method</span></span>](icordebugmodule-getclassfromtoken-method.md)|<span data-ttu-id="a5c43-119">从元数据中获取 ICorDebugClass。</span><span class="sxs-lookup"><span data-stu-id="a5c43-119">Gets the ICorDebugClass from the metadata.</span></span>|  
|[<span data-ttu-id="a5c43-120">GetEditAndContinueSnapshot 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-120">GetEditAndContinueSnapshot Method</span></span>](icordebugmodule-geteditandcontinuesnapshot-method.md)|<span data-ttu-id="a5c43-121">已弃用。</span><span class="sxs-lookup"><span data-stu-id="a5c43-121">Deprecated.</span></span>|  
|[<span data-ttu-id="a5c43-122">GetFunctionFromRVA 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-122">GetFunctionFromRVA Method</span></span>](icordebugmodule-getfunctionfromrva-method.md)|<span data-ttu-id="a5c43-123">未实现。</span><span class="sxs-lookup"><span data-stu-id="a5c43-123">Not implemented.</span></span>|  
|[<span data-ttu-id="a5c43-124">GetFunctionFromToken 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-124">GetFunctionFromToken Method</span></span>](icordebugmodule-getfunctionfromtoken-method.md)|<span data-ttu-id="a5c43-125">获取元数据标记指定的函数。</span><span class="sxs-lookup"><span data-stu-id="a5c43-125">Gets the function that is specified by the metadata token.</span></span>|  
|[<span data-ttu-id="a5c43-126">GetGlobalVariableValue 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-126">GetGlobalVariableValue Method</span></span>](icordebugmodule-getglobalvariablevalue-method.md)|<span data-ttu-id="a5c43-127">获取指定全局变量的值对象。</span><span class="sxs-lookup"><span data-stu-id="a5c43-127">Gets a value object for the specified global variable.</span></span>|  
|[<span data-ttu-id="a5c43-128">GetMetaDataInterface 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-128">GetMetaDataInterface Method</span></span>](icordebugmodule-getmetadatainterface-method.md)|<span data-ttu-id="a5c43-129">获取可用于检查模块的元数据的元数据接口指针。</span><span class="sxs-lookup"><span data-stu-id="a5c43-129">Gets a metadata interface pointer that can be used to examine the metadata for the module.</span></span>|  
|[<span data-ttu-id="a5c43-130">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-130">GetName Method</span></span>](icordebugmodule-getname-method.md)|<span data-ttu-id="a5c43-131">获取模块的文件名。</span><span class="sxs-lookup"><span data-stu-id="a5c43-131">Gets the file name of the module.</span></span>|  
|[<span data-ttu-id="a5c43-132">GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-132">GetProcess Method</span></span>](icordebugmodule-getprocess-method.md)|<span data-ttu-id="a5c43-133">获取此模块的包含进程。</span><span class="sxs-lookup"><span data-stu-id="a5c43-133">Gets the containing process for this module.</span></span>|  
|[<span data-ttu-id="a5c43-134">GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-134">GetSize Method</span></span>](icordebugmodule-getsize-method.md)|<span data-ttu-id="a5c43-135">获取模块的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="a5c43-135">Gets the size of the module in bytes.</span></span>|  
|[<span data-ttu-id="a5c43-136">GetToken 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-136">GetToken Method</span></span>](icordebugmodule-gettoken-method.md)|<span data-ttu-id="a5c43-137">获取此模块的表项的标记。</span><span class="sxs-lookup"><span data-stu-id="a5c43-137">Gets the token for the table entry for this module.</span></span>|  
|[<span data-ttu-id="a5c43-138">IsDynamic 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-138">IsDynamic Method</span></span>](icordebugmodule-isdynamic-method.md)|<span data-ttu-id="a5c43-139">指示模块是否为动态模块。</span><span class="sxs-lookup"><span data-stu-id="a5c43-139">Indicates whether the module is dynamic.</span></span>|  
|[<span data-ttu-id="a5c43-140">IsInMemory 方法</span><span class="sxs-lookup"><span data-stu-id="a5c43-140">IsInMemory Method</span></span>](icordebugmodule-isinmemory-method.md)|<span data-ttu-id="a5c43-141">指示此模块是否仅存在于内存中。</span><span class="sxs-lookup"><span data-stu-id="a5c43-141">Indicates whether this module exists only in memory.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a5c43-142">备注</span><span class="sxs-lookup"><span data-stu-id="a5c43-142">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="a5c43-143">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="a5c43-143">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a5c43-144">要求</span><span class="sxs-lookup"><span data-stu-id="a5c43-144">Requirements</span></span>  

 <span data-ttu-id="a5c43-145">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a5c43-145">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a5c43-146">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a5c43-146">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a5c43-147">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a5c43-147">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a5c43-148">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a5c43-148">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a5c43-149">请参阅</span><span class="sxs-lookup"><span data-stu-id="a5c43-149">See also</span></span>

- [<span data-ttu-id="a5c43-150">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="a5c43-150">ICorDebug Interface</span></span>](icordebug-interface.md)
- [<span data-ttu-id="a5c43-151">调试接口</span><span class="sxs-lookup"><span data-stu-id="a5c43-151">Debugging Interfaces</span></span>](debugging-interfaces.md)
