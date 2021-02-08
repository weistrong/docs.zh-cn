---
description: 了解详细信息： ICorDebugILFrame 接口
title: ICorDebugILFrame 接口
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame
helpviewer_keywords:
- ICorDebugILFrame interface [.NET Framework debugging]
ms.assetid: d5cf5056-da4d-4629-914d-afe42a5393df
topic_type:
- apiref
ms.openlocfilehash: 251fa18151ff286bee3e1bcf7707bf5f7145b4f1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791343"
---
# <a name="icordebugilframe-interface"></a><span data-ttu-id="66b16-103">ICorDebugILFrame 接口</span><span class="sxs-lookup"><span data-stu-id="66b16-103">ICorDebugILFrame Interface</span></span>

<span data-ttu-id="66b16-104">表示 Microsoft 中间语言 (MSIL) 代码的堆栈帧。</span><span class="sxs-lookup"><span data-stu-id="66b16-104">Represents a stack frame of Microsoft intermediate language (MSIL) code.</span></span> <span data-ttu-id="66b16-105">此接口是 ICorDebugFrame 接口的子类。</span><span class="sxs-lookup"><span data-stu-id="66b16-105">This interface is a subclass of the ICorDebugFrame interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="66b16-106">方法</span><span class="sxs-lookup"><span data-stu-id="66b16-106">Methods</span></span>  
  
|<span data-ttu-id="66b16-107">方法</span><span class="sxs-lookup"><span data-stu-id="66b16-107">Method</span></span>|<span data-ttu-id="66b16-108">说明</span><span class="sxs-lookup"><span data-stu-id="66b16-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="66b16-109">CanSetIP 方法</span><span class="sxs-lookup"><span data-stu-id="66b16-109">CanSetIP Method</span></span>](icordebugilframe-cansetip-method.md)|<span data-ttu-id="66b16-110">获取一个值，该值指示是否可以安全地将指令指针设置为指定的偏移位置。</span><span class="sxs-lookup"><span data-stu-id="66b16-110">Gets a value that indicates whether it is safe to set the instruction pointer to the specified offset location.</span></span>|  
|[<span data-ttu-id="66b16-111">EnumerateArguments 方法</span><span class="sxs-lookup"><span data-stu-id="66b16-111">EnumerateArguments Method</span></span>](icordebugilframe-enumeratearguments-method.md)|<span data-ttu-id="66b16-112">获取此帧中的参数的枚举数。</span><span class="sxs-lookup"><span data-stu-id="66b16-112">Gets an enumerator for the arguments in this frame.</span></span>|  
|[<span data-ttu-id="66b16-113">EnumerateLocalVariables 方法</span><span class="sxs-lookup"><span data-stu-id="66b16-113">EnumerateLocalVariables Method</span></span>](icordebugilframe-enumeratelocalvariables-method.md)|<span data-ttu-id="66b16-114">获取此帧中局部变量的枚举数。</span><span class="sxs-lookup"><span data-stu-id="66b16-114">Gets an enumerator for the local variables in this frame.</span></span>|  
|[<span data-ttu-id="66b16-115">GetArgument 方法</span><span class="sxs-lookup"><span data-stu-id="66b16-115">GetArgument Method</span></span>](icordebugilframe-getargument-method.md)|<span data-ttu-id="66b16-116">获取此 MSIL 堆栈帧中的指定参数的值。</span><span class="sxs-lookup"><span data-stu-id="66b16-116">Gets the value of the specified argument in this MSIL stack frame.</span></span>|  
|[<span data-ttu-id="66b16-117">GetIP 方法</span><span class="sxs-lookup"><span data-stu-id="66b16-117">GetIP Method</span></span>](icordebugilframe-getip-method.md)|<span data-ttu-id="66b16-118">获取指令指针的值和按位组合值，它描述如何获取指令指针的值。</span><span class="sxs-lookup"><span data-stu-id="66b16-118">Gets the value of the instruction pointer and a bitwise combination value that describes how the value of the instruction pointer was obtained.</span></span>|  
|[<span data-ttu-id="66b16-119">GetLocalVariable 方法</span><span class="sxs-lookup"><span data-stu-id="66b16-119">GetLocalVariable Method</span></span>](icordebugilframe-getlocalvariable-method.md)|<span data-ttu-id="66b16-120">获取此 MSIL 堆栈帧中的指定局部变量的值。</span><span class="sxs-lookup"><span data-stu-id="66b16-120">Gets the value of the specified local variable in this MSIL stack frame.</span></span>|  
|[<span data-ttu-id="66b16-121">GetStackDepth 方法</span><span class="sxs-lookup"><span data-stu-id="66b16-121">GetStackDepth Method</span></span>](icordebugilframe-getstackdepth-method.md)|<span data-ttu-id="66b16-122">未实现。</span><span class="sxs-lookup"><span data-stu-id="66b16-122">Not implemented.</span></span>|  
|[<span data-ttu-id="66b16-123">GetStackValue 方法</span><span class="sxs-lookup"><span data-stu-id="66b16-123">GetStackValue Method</span></span>](icordebugilframe-getstackvalue-method.md)|<span data-ttu-id="66b16-124">未实现。</span><span class="sxs-lookup"><span data-stu-id="66b16-124">Not implemented.</span></span>|  
|[<span data-ttu-id="66b16-125">SetIP 方法</span><span class="sxs-lookup"><span data-stu-id="66b16-125">SetIP Method</span></span>](icordebugilframe-setip-method.md)|<span data-ttu-id="66b16-126">将指令指针设置为指向 MSIL 代码中的指定偏移位置。</span><span class="sxs-lookup"><span data-stu-id="66b16-126">Sets the instruction pointer to the specified offset location in the MSIL code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="66b16-127">备注</span><span class="sxs-lookup"><span data-stu-id="66b16-127">Remarks</span></span>  

 <span data-ttu-id="66b16-128">`ICorDebugILFrame`接口是专用的 ICorDebugFrame 接口。</span><span class="sxs-lookup"><span data-stu-id="66b16-128">The `ICorDebugILFrame` interface is a specialized ICorDebugFrame interface.</span></span> <span data-ttu-id="66b16-129">它可用于 MSIL 代码帧或实时 (JIT) 编译的帧。</span><span class="sxs-lookup"><span data-stu-id="66b16-129">It is used either for MSIL code frames or for just-in-time (JIT) compiled frames.</span></span> <span data-ttu-id="66b16-130">JIT 编译的帧实现 `ICorDebugILFrame` 接口和 ICorDebugNativeFrame 接口。</span><span class="sxs-lookup"><span data-stu-id="66b16-130">The JIT-compiled frames implement both the `ICorDebugILFrame` interface and the ICorDebugNativeFrame interface.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="66b16-131">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="66b16-131">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="66b16-132">要求</span><span class="sxs-lookup"><span data-stu-id="66b16-132">Requirements</span></span>  

 <span data-ttu-id="66b16-133">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="66b16-133">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="66b16-134">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="66b16-134">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="66b16-135">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="66b16-135">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="66b16-136">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="66b16-136">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66b16-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="66b16-137">See also</span></span>

- [<span data-ttu-id="66b16-138">调试接口</span><span class="sxs-lookup"><span data-stu-id="66b16-138">Debugging Interfaces</span></span>](debugging-interfaces.md)
