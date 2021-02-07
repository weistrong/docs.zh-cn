---
description: 了解详细信息： ICorDebugAppDomain 接口
title: ICorDebugAppDomain 接口
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain
api_location:
- corguids.lib
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain
helpviewer_keywords:
- ICorDebugAppDomain interface [.NET Framework debugging]
ms.assetid: be7ae711-1217-4a44-be40-166e29641b77
topic_type:
- apiref
ms.openlocfilehash: 5f1ac20a7376a741da2e34de74c810c0f45e8293
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754191"
---
# <a name="icordebugappdomain-interface"></a><span data-ttu-id="854b0-103">ICorDebugAppDomain 接口</span><span class="sxs-lookup"><span data-stu-id="854b0-103">ICorDebugAppDomain Interface</span></span>

<span data-ttu-id="854b0-104">提供用于调试应用程序域的方法。</span><span class="sxs-lookup"><span data-stu-id="854b0-104">Provides methods for debugging application domains.</span></span> <span data-ttu-id="854b0-105">此接口是 ICorDebugController 的子类。</span><span class="sxs-lookup"><span data-stu-id="854b0-105">This interface is a subclass of ICorDebugController.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="854b0-106">方法</span><span class="sxs-lookup"><span data-stu-id="854b0-106">Methods</span></span>  
  
|<span data-ttu-id="854b0-107">方法</span><span class="sxs-lookup"><span data-stu-id="854b0-107">Method</span></span>|<span data-ttu-id="854b0-108">说明</span><span class="sxs-lookup"><span data-stu-id="854b0-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="854b0-109">Attach 方法</span><span class="sxs-lookup"><span data-stu-id="854b0-109">Attach Method</span></span>](icordebugappdomain-attach-method.md)|<span data-ttu-id="854b0-110">将调试器附加到应用程序域。</span><span class="sxs-lookup"><span data-stu-id="854b0-110">Attaches the debugger to the application domain.</span></span>|  
|[<span data-ttu-id="854b0-111">EnumerateAssemblies 方法</span><span class="sxs-lookup"><span data-stu-id="854b0-111">EnumerateAssemblies Method</span></span>](icordebugappdomain-enumerateassemblies-method.md)|<span data-ttu-id="854b0-112">获取应用程序域中的程序集的枚举器。</span><span class="sxs-lookup"><span data-stu-id="854b0-112">Gets an enumerator for the assemblies in the application domain.</span></span>|  
|[<span data-ttu-id="854b0-113">EnumerateBreakpoints 方法</span><span class="sxs-lookup"><span data-stu-id="854b0-113">EnumerateBreakpoints Method</span></span>](icordebugappdomain-enumeratebreakpoints-method.md)|<span data-ttu-id="854b0-114">获取应用程序域中所有活动断点的枚举器。</span><span class="sxs-lookup"><span data-stu-id="854b0-114">Gets an enumerator for all active breakpoints in the application domain.</span></span>|  
|[<span data-ttu-id="854b0-115">EnumerateSteppers 方法</span><span class="sxs-lookup"><span data-stu-id="854b0-115">EnumerateSteppers Method</span></span>](icordebugappdomain-enumeratesteppers-method.md)|<span data-ttu-id="854b0-116">获取应用程序域中所有活动 steppers 的枚举器。</span><span class="sxs-lookup"><span data-stu-id="854b0-116">Gets an enumerator for all active steppers in the application domain.</span></span>|  
|[<span data-ttu-id="854b0-117">GetId 方法</span><span class="sxs-lookup"><span data-stu-id="854b0-117">GetId Method</span></span>](icordebugappdomain-getid-method.md)|<span data-ttu-id="854b0-118">获取应用程序域的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="854b0-118">Gets the unique ID of the application domain.</span></span>|  
|[<span data-ttu-id="854b0-119">GetModuleFromMetaDataInterface 方法</span><span class="sxs-lookup"><span data-stu-id="854b0-119">GetModuleFromMetaDataInterface Method</span></span>](icordebugappdomain-getmodulefrommetadatainterface-method.md)|<span data-ttu-id="854b0-120">获取具有给定元数据接口的 ICorDebugModule 对象。</span><span class="sxs-lookup"><span data-stu-id="854b0-120">Gets the ICorDebugModule object with the given metadata interface.</span></span>|  
|[<span data-ttu-id="854b0-121">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="854b0-121">GetName Method</span></span>](icordebugappdomain-getname-method.md)|<span data-ttu-id="854b0-122">获取应用程序域的名称。</span><span class="sxs-lookup"><span data-stu-id="854b0-122">Gets the name of the application domain.</span></span>|  
|[<span data-ttu-id="854b0-123">GetObject 方法</span><span class="sxs-lookup"><span data-stu-id="854b0-123">GetObject Method</span></span>](icordebugappdomain-getobject-method.md)|<span data-ttu-id="854b0-124">获取 (CLR) 应用程序域的公共语言运行时的接口指针。</span><span class="sxs-lookup"><span data-stu-id="854b0-124">Gets an interface pointer to the common language runtime (CLR) application domain.</span></span>|  
|[<span data-ttu-id="854b0-125">GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="854b0-125">GetProcess Method</span></span>](icordebugappdomain-getprocess-method.md)|<span data-ttu-id="854b0-126">获取包含应用程序域的进程。</span><span class="sxs-lookup"><span data-stu-id="854b0-126">Gets the process containing the application domain.</span></span>|  
|[<span data-ttu-id="854b0-127">IsAttached 方法</span><span class="sxs-lookup"><span data-stu-id="854b0-127">IsAttached Method</span></span>](icordebugappdomain-isattached-method.md)|<span data-ttu-id="854b0-128">确定调试器是否已附加到应用程序域。</span><span class="sxs-lookup"><span data-stu-id="854b0-128">Determines whether the debugger is attached to the application domain.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="854b0-129">备注</span><span class="sxs-lookup"><span data-stu-id="854b0-129">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="854b0-130">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="854b0-130">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="854b0-131">要求</span><span class="sxs-lookup"><span data-stu-id="854b0-131">Requirements</span></span>  

 <span data-ttu-id="854b0-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="854b0-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="854b0-133">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="854b0-133">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="854b0-134">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="854b0-134">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="854b0-135">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="854b0-135">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="854b0-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="854b0-136">See also</span></span>

- [<span data-ttu-id="854b0-137">调试接口</span><span class="sxs-lookup"><span data-stu-id="854b0-137">Debugging Interfaces</span></span>](debugging-interfaces.md)
