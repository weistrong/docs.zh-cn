---
description: 了解详细信息： ICorProfilerInfo2 接口
title: ICorProfilerInfo2 接口
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2
helpviewer_keywords:
- ICorProfilerInfo2 interface [.NET Framework profiling]
ms.assetid: 91bd49b6-4d12-494f-a8f1-2f251e8c65e3
topic_type:
- apiref
ms.openlocfilehash: 07828c6f55b72068e9021991600ed17eb6ffe6ad
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647006"
---
# <a name="icorprofilerinfo2-interface"></a><span data-ttu-id="46fcf-103">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="46fcf-103">ICorProfilerInfo2 Interface</span></span>

<span data-ttu-id="46fcf-104">提供一些方法，代码探查器使用这些方法与公共语言运行时 (CLR) 进行通信，以控制事件监视和请求信息。</span><span class="sxs-lookup"><span data-stu-id="46fcf-104">Provides methods that code profilers use to communicate with the common language runtime (CLR) to control event monitoring and request information.</span></span> <span data-ttu-id="46fcf-105">`ICorProfilerInfo2`接口是[ICorProfilerInfo](icorprofilerinfo-interface.md)接口的扩展。</span><span class="sxs-lookup"><span data-stu-id="46fcf-105">The `ICorProfilerInfo2` interface is an extension of the [ICorProfilerInfo](icorprofilerinfo-interface.md) interface.</span></span> <span data-ttu-id="46fcf-106">也就是说，它提供 .NET Framework 版本2.0 及更高版本中支持的新方法。</span><span class="sxs-lookup"><span data-stu-id="46fcf-106">That is, it provides new methods supported in the .NET Framework version 2.0 and later versions.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="46fcf-107">方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-107">Methods</span></span>  
  
|<span data-ttu-id="46fcf-108">方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-108">Method</span></span>|<span data-ttu-id="46fcf-109">说明</span><span class="sxs-lookup"><span data-stu-id="46fcf-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="46fcf-110">DoStackSnapshot 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-110">DoStackSnapshot Method</span></span>](icorprofilerinfo2-dostacksnapshot-method.md)|<span data-ttu-id="46fcf-111">遍历指定线程的堆栈，将托管调用帧报告给探查器。</span><span class="sxs-lookup"><span data-stu-id="46fcf-111">Walks the stack of the specified thread to report managed call frames to the profiler.</span></span>|  
|[<span data-ttu-id="46fcf-112">EnumModuleFrozenObjects 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-112">EnumModuleFrozenObjects Method</span></span>](icorprofilerinfo2-enummodulefrozenobjects-method.md)|<span data-ttu-id="46fcf-113">获取一个枚举器，该枚举数允许对指定模块中的冻结对象进行迭代。</span><span class="sxs-lookup"><span data-stu-id="46fcf-113">Gets an enumerator that allows iteration over the frozen objects in the specified module.</span></span>|  
|[<span data-ttu-id="46fcf-114">GetAppDomainStaticAddress 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-114">GetAppDomainStaticAddress Method</span></span>](icorprofilerinfo2-getappdomainstaticaddress-method.md)|<span data-ttu-id="46fcf-115">获取指定应用程序域静态字段在指定应用程序域范围内的地址。</span><span class="sxs-lookup"><span data-stu-id="46fcf-115">Gets the address of the specified application domain-static field that is in the scope of the specified application domain.</span></span>|  
|[<span data-ttu-id="46fcf-116">GetArrayObjectInfo 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-116">GetArrayObjectInfo Method</span></span>](icorprofilerinfo2-getarrayobjectinfo-method.md)|<span data-ttu-id="46fcf-117">获取有关数组对象的详细信息。</span><span class="sxs-lookup"><span data-stu-id="46fcf-117">Gets detailed information about an array object.</span></span>|  
|[<span data-ttu-id="46fcf-118">GetBoxClassLayout 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-118">GetBoxClassLayout Method</span></span>](icorprofilerinfo2-getboxclasslayout-method.md)|<span data-ttu-id="46fcf-119">获取有关已装箱的指定值类型的类布局信息。</span><span class="sxs-lookup"><span data-stu-id="46fcf-119">Gets information about the class layout for a specified value type that is boxed.</span></span>|  
|[<span data-ttu-id="46fcf-120">GetClassFromTokenAndTypeArgs 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-120">GetClassFromTokenAndTypeArgs Method</span></span>](icorprofilerinfo2-getclassfromtokenandtypeargs-method.md)|<span data-ttu-id="46fcf-121">`ClassID`使用指定的元数据标记和 `ClassID` 任何类型参数的值获取类型的。</span><span class="sxs-lookup"><span data-stu-id="46fcf-121">Gets the `ClassID` of a type by using the specified metadata token and the `ClassID` values of any type arguments.</span></span>|  
|[<span data-ttu-id="46fcf-122">GetClassIDInfo2 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-122">GetClassIDInfo2 Method</span></span>](icorprofilerinfo2-getclassidinfo2-method.md)|<span data-ttu-id="46fcf-123">获取指定的泛型类的父模块、类的元数据标记、 `ClassID` 其父类的，以及 `ClassID` 每个类型参数（如果存在）的。</span><span class="sxs-lookup"><span data-stu-id="46fcf-123">Gets the parent module of the specified generic class, the metadata token for the class, the `ClassID` of its parent class, and the `ClassID` for each type argument, if present, of the class.</span></span>|  
|[<span data-ttu-id="46fcf-124">GetClassLayout 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-124">GetClassLayout Method</span></span>](icorprofilerinfo2-getclasslayout-method.md)|<span data-ttu-id="46fcf-125">获取内存中由指定的类定义的字段的布局信息。</span><span class="sxs-lookup"><span data-stu-id="46fcf-125">Gets information about the layout, in memory, of the fields defined by the specified class.</span></span> <span data-ttu-id="46fcf-126">也就是说，此方法获取类的字段的偏移量。</span><span class="sxs-lookup"><span data-stu-id="46fcf-126">That is, this method gets the offsets of the class's fields.</span></span>|  
|[<span data-ttu-id="46fcf-127">GetCodeInfo2 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-127">GetCodeInfo2 Method</span></span>](icorprofilerinfo2-getcodeinfo2-method.md)|<span data-ttu-id="46fcf-128">获取与指定 `FunctionID` 关联的本机代码的范围。</span><span class="sxs-lookup"><span data-stu-id="46fcf-128">Gets the extents of native code associated with the specified `FunctionID`.</span></span>|  
|[<span data-ttu-id="46fcf-129">GetContextStaticAddress 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-129">GetContextStaticAddress Method</span></span>](icorprofilerinfo2-getcontextstaticaddress-method.md)|<span data-ttu-id="46fcf-130">获取指定上下文的范围内的指定上下文静态字段的地址。</span><span class="sxs-lookup"><span data-stu-id="46fcf-130">Gets the address of the specified context-static field that is in the scope of the specified context.</span></span>|  
|[<span data-ttu-id="46fcf-131">GetFunctionFromTokenAndTypeArgs 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-131">GetFunctionFromTokenAndTypeArgs Method</span></span>](icorprofilerinfo2-getfunctionfromtokenandtypeargs-method.md)|<span data-ttu-id="46fcf-132">`FunctionID`使用指定的元数据标记（包含类）和 `ClassID` 任何类型参数的值获取函数的。</span><span class="sxs-lookup"><span data-stu-id="46fcf-132">Gets the `FunctionID` of a function by using the specified metadata token, containing class, and `ClassID` values of any type arguments.</span></span>|  
|[<span data-ttu-id="46fcf-133">GetFunctionInfo2 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-133">GetFunctionInfo2 Method</span></span>](icorprofilerinfo2-getfunctioninfo2-method.md)|<span data-ttu-id="46fcf-134">获取每个类型参数或某个函数（如果存在）的父类、元数据标记和 `ClassID`。</span><span class="sxs-lookup"><span data-stu-id="46fcf-134">Gets the parent class, the metadata token, and the `ClassID` of each type argument, if present, of a function.</span></span>|  
|[<span data-ttu-id="46fcf-135">GetGenerationBounds 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-135">GetGenerationBounds Method</span></span>](icorprofilerinfo2-getgenerationbounds-method.md)|<span data-ttu-id="46fcf-136">获取组成垃圾回收堆的生成 (堆) 段的内存区域。</span><span class="sxs-lookup"><span data-stu-id="46fcf-136">Gets the memory regions (the segments of the heap) that make up the generations of the garbage-collected heap.</span></span>|  
|[<span data-ttu-id="46fcf-137">GetNotifiedExceptionClauseInfo 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-137">GetNotifiedExceptionClauseInfo Method</span></span>](icorprofilerinfo2-getnotifiedexceptionclauseinfo-method.md)|<span data-ttu-id="46fcf-138">获取 `catch` / `finally` / `filter` 要运行或刚刚运行 () 的异常子句的本机地址和帧信息。</span><span class="sxs-lookup"><span data-stu-id="46fcf-138">Gets the native address and frame information for the exception clause (`catch`/`finally`/`filter`) that is about to be run or has just been run.</span></span>|  
|[<span data-ttu-id="46fcf-139">GetObjectGeneration 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-139">GetObjectGeneration Method</span></span>](icorprofilerinfo2-getobjectgeneration-method.md)|<span data-ttu-id="46fcf-140">获取包含指定对象的堆段。</span><span class="sxs-lookup"><span data-stu-id="46fcf-140">Gets the segment of the heap that contains the specified object.</span></span>|  
|[<span data-ttu-id="46fcf-141">GetRVAStaticAddress 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-141">GetRVAStaticAddress Method</span></span>](icorprofilerinfo2-getrvastaticaddress-method.md)|<span data-ttu-id="46fcf-142">获取 (RVA) 静态字段的指定相对虚拟地址的地址。</span><span class="sxs-lookup"><span data-stu-id="46fcf-142">Gets the address of the specified relative virtual address (RVA)-static field.</span></span>|  
|[<span data-ttu-id="46fcf-143">GetStaticFieldInfo 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-143">GetStaticFieldInfo Method</span></span>](icorprofilerinfo2-getstaticfieldinfo-method.md)|<span data-ttu-id="46fcf-144">获取指定字段为静态的作用域。</span><span class="sxs-lookup"><span data-stu-id="46fcf-144">Gets the scope in which the specified field is static.</span></span>|  
|[<span data-ttu-id="46fcf-145">GetStringLayout 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-145">GetStringLayout Method</span></span>](icorprofilerinfo2-getstringlayout-method.md)|<span data-ttu-id="46fcf-146">获取有关字符串对象布局的信息。</span><span class="sxs-lookup"><span data-stu-id="46fcf-146">Gets information about the layout of a string object.</span></span>|  
|[<span data-ttu-id="46fcf-147">GetThreadAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-147">GetThreadAppDomain Method</span></span>](icorprofilerinfo2-getthreadappdomain-method.md)|<span data-ttu-id="46fcf-148">获取指定线程当前正在执行代码的应用程序域的 ID。</span><span class="sxs-lookup"><span data-stu-id="46fcf-148">Gets the ID of the application domain in which the specified thread is currently executing code.</span></span>|  
|[<span data-ttu-id="46fcf-149">GetThreadStaticAddress 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-149">GetThreadStaticAddress Method</span></span>](icorprofilerinfo2-getthreadstaticaddress-method.md)|<span data-ttu-id="46fcf-150">获取指定线程范围内的指定线程静态字段的地址。</span><span class="sxs-lookup"><span data-stu-id="46fcf-150">Gets the address of the specified thread-static field that is in the scope of the specified thread.</span></span>|  
|[<span data-ttu-id="46fcf-151">SetEnterLeaveFunctionHooks2 方法</span><span class="sxs-lookup"><span data-stu-id="46fcf-151">SetEnterLeaveFunctionHooks2 Method</span></span>](icorprofilerinfo2-setenterleavefunctionhooks2-method.md)|<span data-ttu-id="46fcf-152">指定在托管函数的 "enter"、"leave" 和 "tailcall" 挂钩上调用的探查器实现函数。</span><span class="sxs-lookup"><span data-stu-id="46fcf-152">Specifies profiler-implemented functions to be called on "enter", "leave", and "tailcall" hooks of managed functions.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="46fcf-153">备注</span><span class="sxs-lookup"><span data-stu-id="46fcf-153">Remarks</span></span>  

 <span data-ttu-id="46fcf-154">探查器调用接口中的方法 `ICorProfilerInfo2` ，以便与 CLR 通信以控制事件监视和请求信息。</span><span class="sxs-lookup"><span data-stu-id="46fcf-154">A profiler calls a method in the `ICorProfilerInfo2` interface to communicate with the CLR to control event monitoring and request information.</span></span>  
  
 <span data-ttu-id="46fcf-155">接口的方法 `ICorProfilerInfo2` 由 CLR 使用自由线程模型实现。</span><span class="sxs-lookup"><span data-stu-id="46fcf-155">The methods of the `ICorProfilerInfo2` interface are implemented by the CLR using the free-threaded model.</span></span> <span data-ttu-id="46fcf-156">每个方法均返回一个 HRESULT，指示成功或失败。</span><span class="sxs-lookup"><span data-stu-id="46fcf-156">Each method returns an HRESULT to indicate success or failure.</span></span> <span data-ttu-id="46fcf-157">有关可能的返回代码的列表，请参阅 CorError.h 文件。</span><span class="sxs-lookup"><span data-stu-id="46fcf-157">For a list of possible return codes, see the CorError.h file.</span></span>  
  
 <span data-ttu-id="46fcf-158">在 `ICorProfilerInfo2` 初始化期间，使用探查器的 [ICorProfilerCallback：： Initialize](icorprofilercallback-initialize-method.md)实现将一个接口传递到每个代码探查器。</span><span class="sxs-lookup"><span data-stu-id="46fcf-158">The CLR passes an `ICorProfilerInfo2` interface to each code profiler during initialization, using the profiler's implementation of [ICorProfilerCallback::Initialize](icorprofilercallback-initialize-method.md).</span></span> <span data-ttu-id="46fcf-159">然后，代码探查器可以调用接口的方法 `ICorProfilerInfo2` ，以获取有关在 CLR 控制下执行的托管代码的信息。</span><span class="sxs-lookup"><span data-stu-id="46fcf-159">A code profiler can then call methods of the `ICorProfilerInfo2` interface to get information about managed code being executed under the control of the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="46fcf-160">要求</span><span class="sxs-lookup"><span data-stu-id="46fcf-160">Requirements</span></span>  

 <span data-ttu-id="46fcf-161">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="46fcf-161">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46fcf-162">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="46fcf-162">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="46fcf-163">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="46fcf-163">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="46fcf-164">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46fcf-164">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46fcf-165">请参阅</span><span class="sxs-lookup"><span data-stu-id="46fcf-165">See also</span></span>

- [<span data-ttu-id="46fcf-166">分析接口</span><span class="sxs-lookup"><span data-stu-id="46fcf-166">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="46fcf-167">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="46fcf-167">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
