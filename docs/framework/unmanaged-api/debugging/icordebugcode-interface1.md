---
description: 了解详细信息： ICorDebugCode 接口
title: ICorDebugCode 接口
ms.date: 03/30/2017
api_name:
- ICorDebugCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode
helpviewer_keywords:
- ICorDebugCode interface [.NET Framework debugging]
ms.assetid: 7bd14fb6-8b54-4484-a891-e3c21859c019
topic_type:
- apiref
ms.openlocfilehash: ce67c48501783bbe00152f0ba2c224e6e7dde6d7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711136"
---
# <a name="icordebugcode-interface"></a><span data-ttu-id="27521-103">ICorDebugCode 接口</span><span class="sxs-lookup"><span data-stu-id="27521-103">ICorDebugCode Interface</span></span>

<span data-ttu-id="27521-104">表示 Microsoft 中间语言 (MSIL) 代码段或本机代码段。</span><span class="sxs-lookup"><span data-stu-id="27521-104">Represents a segment of either Microsoft intermediate language (MSIL) code or native code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="27521-105">方法</span><span class="sxs-lookup"><span data-stu-id="27521-105">Methods</span></span>  
  
|<span data-ttu-id="27521-106">方法</span><span class="sxs-lookup"><span data-stu-id="27521-106">Method</span></span>|<span data-ttu-id="27521-107">说明</span><span class="sxs-lookup"><span data-stu-id="27521-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="27521-108">CreateBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="27521-108">CreateBreakpoint Method</span></span>](icordebugcode-createbreakpoint-method.md)|<span data-ttu-id="27521-109">按指定的偏移量创建断点。</span><span class="sxs-lookup"><span data-stu-id="27521-109">Creates a breakpoint at the specified offset.</span></span>|  
|[<span data-ttu-id="27521-110">GetAddress 方法</span><span class="sxs-lookup"><span data-stu-id="27521-110">GetAddress Method</span></span>](icordebugcode-getaddress-method.md)|<span data-ttu-id="27521-111">获取此表示的代码段 (RVA) 的相对虚拟地址 `ICorDebugCode` 。</span><span class="sxs-lookup"><span data-stu-id="27521-111">Gets the relative virtual address (RVA) of the code segment that this `ICorDebugCode` represents.</span></span>|  
|[<span data-ttu-id="27521-112">GetCode 方法</span><span class="sxs-lookup"><span data-stu-id="27521-112">GetCode Method</span></span>](icordebugcode-getcode-method.md)|<span data-ttu-id="27521-113">获取用于反汇编的指定函数的所有代码。</span><span class="sxs-lookup"><span data-stu-id="27521-113">Gets all the code for the specified function, formatted for disassembly.</span></span> <span data-ttu-id="27521-114">此方法已弃用;改 [为使用 ICorDebugCode2：： GetCodeChunks](icordebugcode2-getcodechunks-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="27521-114">This method has been deprecated; use [ICorDebugCode2::GetCodeChunks](icordebugcode2-getcodechunks-method.md) instead.</span></span>|  
|[<span data-ttu-id="27521-115">GetEnCRemapSequencePoints 方法</span><span class="sxs-lookup"><span data-stu-id="27521-115">GetEnCRemapSequencePoints Method</span></span>](icordebugcode-getencremapsequencepoints-method.md)|<span data-ttu-id="27521-116">未实现。</span><span class="sxs-lookup"><span data-stu-id="27521-116">Not implemented.</span></span>|  
|[<span data-ttu-id="27521-117">GetFunction 方法</span><span class="sxs-lookup"><span data-stu-id="27521-117">GetFunction Method</span></span>](icordebugcode-getfunction-method.md)|<span data-ttu-id="27521-118">获取与此关联的 "ICorDebugFunction" `ICorDebugCode` 。</span><span class="sxs-lookup"><span data-stu-id="27521-118">Gets the "ICorDebugFunction" associated with this `ICorDebugCode`.</span></span>|  
|[<span data-ttu-id="27521-119">GetILToNativeMapping 方法</span><span class="sxs-lookup"><span data-stu-id="27521-119">GetILToNativeMapping Method</span></span>](icordebugcode-getiltonativemapping-method.md)|<span data-ttu-id="27521-120">获取 "COR_DEBUG_IL_TO_NATIVE_MAP" 实例的数组，这些实例表示从 MSIL 偏移量到本机偏移量的映射。</span><span class="sxs-lookup"><span data-stu-id="27521-120">Gets an array of "COR_DEBUG_IL_TO_NATIVE_MAP" instances that represent mappings from MSIL offsets to native offsets.</span></span>|  
|[<span data-ttu-id="27521-121">GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="27521-121">GetSize Method</span></span>](icordebugcode-getsize-method.md)|<span data-ttu-id="27521-122">获取此表示的二进制代码的大小（以字节为单位） `ICorDebugCode` 。</span><span class="sxs-lookup"><span data-stu-id="27521-122">Gets the size, in bytes, of the binary code represented by this `ICorDebugCode`.</span></span>|  
|[<span data-ttu-id="27521-123">GetVersionNumber 方法</span><span class="sxs-lookup"><span data-stu-id="27521-123">GetVersionNumber Method</span></span>](icordebugcode-getversionnumber-method.md)|<span data-ttu-id="27521-124">获取一个从1开始的数字，该数字标识此表示的代码的版本 `ICorDebugCode` 。</span><span class="sxs-lookup"><span data-stu-id="27521-124">Gets the one-based number that identifies the version of the code that this `ICorDebugCode` represents.</span></span>|  
|[<span data-ttu-id="27521-125">IsIL 方法</span><span class="sxs-lookup"><span data-stu-id="27521-125">IsIL Method</span></span>](icordebugcode-isil-method.md)|<span data-ttu-id="27521-126">获取一个值，该值指示是否 `ICorDebugCode` 在 MSIL 中编译此。</span><span class="sxs-lookup"><span data-stu-id="27521-126">Gets a value that indicates whether this `ICorDebugCode` is compiled in MSIL.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="27521-127">备注</span><span class="sxs-lookup"><span data-stu-id="27521-127">Remarks</span></span>  

 <span data-ttu-id="27521-128">`ICorDebugCode` 可以表示 MSIL 或本机代码。</span><span class="sxs-lookup"><span data-stu-id="27521-128">`ICorDebugCode` can represent either MSIL or native code.</span></span> <span data-ttu-id="27521-129">表示 MSIL 代码的 "ICorDebugFunction" 对象可以有零个或一个 `ICorDebugCode` 关联的对象。</span><span class="sxs-lookup"><span data-stu-id="27521-129">An "ICorDebugFunction" object that represents MSIL code can have either zero or one `ICorDebugCode` objects associated with it.</span></span> <span data-ttu-id="27521-130">表示本机代码的 "ICorDebugFunction" 对象可以有任意数量的 `ICorDebugCode` 关联对象。</span><span class="sxs-lookup"><span data-stu-id="27521-130">An "ICorDebugFunction" object that represents native code can have any number of `ICorDebugCode` objects associated with it.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="27521-131">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="27521-131">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="27521-132">要求</span><span class="sxs-lookup"><span data-stu-id="27521-132">Requirements</span></span>  

 <span data-ttu-id="27521-133">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="27521-133">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="27521-134">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="27521-134">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="27521-135">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="27521-135">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="27521-136">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="27521-136">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27521-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="27521-137">See also</span></span>

- [<span data-ttu-id="27521-138">ICorDebugCode3 接口</span><span class="sxs-lookup"><span data-stu-id="27521-138">ICorDebugCode3 Interface</span></span>](icordebugcode3-interface.md)
- [<span data-ttu-id="27521-139">调试接口</span><span class="sxs-lookup"><span data-stu-id="27521-139">Debugging Interfaces</span></span>](debugging-interfaces.md)
