---
description: 了解详细信息： ICorDebugProcess5 接口
title: ICorDebugProcess5 接口
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5
helpviewer_keywords:
- ICorDebugProcess5 interface [.NET Framework debugging]
ms.assetid: 30a39d79-1f10-4328-9c5d-094ed824e2ba
topic_type:
- apiref
ms.openlocfilehash: 880c305c1d9786f87d9727836a973696aa686ecf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649762"
---
# <a name="icordebugprocess5-interface"></a><span data-ttu-id="e257b-103">ICorDebugProcess5 接口</span><span class="sxs-lookup"><span data-stu-id="e257b-103">ICorDebugProcess5 Interface</span></span>

<span data-ttu-id="e257b-104">扩展 ICorDebugProcess 接口以支持对托管堆的访问，以提供有关托管对象的垃圾回收的信息，以及确定调试器是否从应用程序本地本机映像缓存中加载图像。</span><span class="sxs-lookup"><span data-stu-id="e257b-104">Extends the ICorDebugProcess interface to support access to the managed heap, to provide information about garbage collection of managed objects, and to determine whether a debugger loads images from the application local native image cache.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e257b-105">方法</span><span class="sxs-lookup"><span data-stu-id="e257b-105">Methods</span></span>  
  
|<span data-ttu-id="e257b-106">方法</span><span class="sxs-lookup"><span data-stu-id="e257b-106">Method</span></span>|<span data-ttu-id="e257b-107">说明</span><span class="sxs-lookup"><span data-stu-id="e257b-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e257b-108">EnableNGenPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="e257b-108">EnableNGenPolicy Method</span></span>](icordebugprocess5-enablengenpolicy-method.md)|<span data-ttu-id="e257b-109">设置一个值，该值确定应用程序在托管调试器下运行时如何加载本机映像。</span><span class="sxs-lookup"><span data-stu-id="e257b-109">Sets a value that determines how an application loads native images while running under a managed debugger.</span></span>|  
|[<span data-ttu-id="e257b-110">EnumerateGCReferences 方法</span><span class="sxs-lookup"><span data-stu-id="e257b-110">EnumerateGCReferences Method</span></span>](icordebugprocess5-enumerategcreferences-method.md)|<span data-ttu-id="e257b-111">获取一个枚举器，该枚举器用于进程中要进行垃圾回收的所有对象。</span><span class="sxs-lookup"><span data-stu-id="e257b-111">Gets an enumerator for all objects that are to be garbage-collected in a process.</span></span>|  
|[<span data-ttu-id="e257b-112">EnumerateHandles 方法</span><span class="sxs-lookup"><span data-stu-id="e257b-112">EnumerateHandles Method</span></span>](icordebugprocess5-enumeratehandles-method.md)|<span data-ttu-id="e257b-113">获取进程中的对象句柄的枚举器。</span><span class="sxs-lookup"><span data-stu-id="e257b-113">Gets an enumerator for object handles in a process.</span></span>|  
|[<span data-ttu-id="e257b-114">EnumerateHeap 方法</span><span class="sxs-lookup"><span data-stu-id="e257b-114">EnumerateHeap Method</span></span>](icordebugprocess5-enumerateheap-method.md)|<span data-ttu-id="e257b-115">获取托管堆上的对象的枚举器。</span><span class="sxs-lookup"><span data-stu-id="e257b-115">Gets an enumerator for objects on the managed heap.</span></span>|  
|[<span data-ttu-id="e257b-116">EnumerateHeapRegions 方法</span><span class="sxs-lookup"><span data-stu-id="e257b-116">EnumerateHeapRegions Method</span></span>](icordebugprocess5-enumerateheapregions-method.md)|<span data-ttu-id="e257b-117">获取托管堆区域的枚举器。</span><span class="sxs-lookup"><span data-stu-id="e257b-117">Gets an enumerator for regions of the managed heap.</span></span>|  
|[<span data-ttu-id="e257b-118">GetArrayLayout 方法</span><span class="sxs-lookup"><span data-stu-id="e257b-118">GetArrayLayout Method</span></span>](icordebugprocess5-getarraylayout-method.md)|<span data-ttu-id="e257b-119">获取有关内存中数组的布局的信息。</span><span class="sxs-lookup"><span data-stu-id="e257b-119">Gets information about the layout of an array in memory.</span></span>|  
|[<span data-ttu-id="e257b-120">GetGCHeapInformation 方法</span><span class="sxs-lookup"><span data-stu-id="e257b-120">GetGCHeapInformation Method</span></span>](icordebugprocess5-getgcheapinformation-method.md)|<span data-ttu-id="e257b-121">获取一个指向 [COR_HEAPINFO](cor-heapinfo-structure.md) 结构的指针，该结构包含有关要在托管堆上进行垃圾回收的对象的信息。</span><span class="sxs-lookup"><span data-stu-id="e257b-121">Gets a pointer to a [COR_HEAPINFO](cor-heapinfo-structure.md) structure that contains information about objects that are to be garbage-collected on the managed heap.</span></span>|  
|[<span data-ttu-id="e257b-122">GetObject 方法</span><span class="sxs-lookup"><span data-stu-id="e257b-122">GetObject Method</span></span>](icordebugprocess5-getobject-method.md)|<span data-ttu-id="e257b-123">获取指向托管堆上的对象的指针。</span><span class="sxs-lookup"><span data-stu-id="e257b-123">Gets a pointer to an object on the managed heap.</span></span>|  
|[<span data-ttu-id="e257b-124">GetTypeFields 方法</span><span class="sxs-lookup"><span data-stu-id="e257b-124">GetTypeFields Method</span></span>](icordebugprocess5-gettypefields-method.md)|<span data-ttu-id="e257b-125">获取一个指针，该指针指向一个数组，该数组包含基于类型标识符的类型的字段信息。</span><span class="sxs-lookup"><span data-stu-id="e257b-125">Gets a pointer to an array that contains field information for a type based on its type identifier.</span></span>|  
|[<span data-ttu-id="e257b-126">GetTypeForTypeID 方法</span><span class="sxs-lookup"><span data-stu-id="e257b-126">GetTypeForTypeID Method</span></span>](icordebugprocess5-gettypefortypeid-method.md)|<span data-ttu-id="e257b-127">获取一个类型对象，该对象基于其类型标识符提供有关对象的信息。</span><span class="sxs-lookup"><span data-stu-id="e257b-127">Gets a type object that provides information about an object based on its type identifiers.</span></span>|  
|[<span data-ttu-id="e257b-128">GetTypeID 方法</span><span class="sxs-lookup"><span data-stu-id="e257b-128">GetTypeID Method</span></span>](icordebugprocess5-gettypeid-method.md)|<span data-ttu-id="e257b-129">获取指定地址处的对象的类型标识符。</span><span class="sxs-lookup"><span data-stu-id="e257b-129">Gets the type identifier for the object at a specified address.</span></span>|  
|[<span data-ttu-id="e257b-130">GetTypeLayout 方法</span><span class="sxs-lookup"><span data-stu-id="e257b-130">GetTypeLayout Method</span></span>](icordebugprocess5-gettypelayout-method.md)|<span data-ttu-id="e257b-131">根据对象的类型标识符获取有关该对象在内存中的布局的信息。</span><span class="sxs-lookup"><span data-stu-id="e257b-131">Gets information about the layout of an object in memory based on its type identifier.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e257b-132">备注</span><span class="sxs-lookup"><span data-stu-id="e257b-132">Remarks</span></span>  

 <span data-ttu-id="e257b-133">此接口以逻辑方式扩展了 ICorDebugProcess、ICorDebugProcess2 和 [ICorDebugProcess3](icordebugprocess3-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="e257b-133">This interface logically extends the ICorDebugProcess, ICorDebugProcess2, and [ICorDebugProcess3](icordebugprocess3-interface.md) interfaces.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="e257b-134">此接口不支持从另一台计算机或从其他进程进行远程调用。</span><span class="sxs-lookup"><span data-stu-id="e257b-134">This interface does not support being called remotely, either from another machine or from another process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e257b-135">要求</span><span class="sxs-lookup"><span data-stu-id="e257b-135">Requirements</span></span>  

 <span data-ttu-id="e257b-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e257b-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e257b-137">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e257b-137">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e257b-138">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e257b-138">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e257b-139">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e257b-139">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e257b-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="e257b-140">See also</span></span>

- [<span data-ttu-id="e257b-141">调试接口</span><span class="sxs-lookup"><span data-stu-id="e257b-141">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="e257b-142">调试</span><span class="sxs-lookup"><span data-stu-id="e257b-142">Debugging</span></span>](index.md)
