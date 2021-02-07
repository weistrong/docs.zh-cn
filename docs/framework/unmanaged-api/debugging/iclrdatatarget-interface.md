---
description: 了解详细信息： ICLRDataTarget 接口
title: ICLRDataTarget 接口
ms.date: 03/30/2017
api_name:
- ICLRDataTarget
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget
helpviewer_keywords:
- ICLRDataTarget interface [.NET Framework debugging]
ms.assetid: e2f05155-9bef-4e11-b703-7f05890665ca
topic_type:
- apiref
ms.openlocfilehash: f24760f638705a1bde7e055069cbc3a18a0896fd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738216"
---
# <a name="iclrdatatarget-interface"></a><span data-ttu-id="b27b7-103">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="b27b7-103">ICLRDataTarget Interface</span></span>

<span data-ttu-id="b27b7-104">提供与公共语言运行时的目标项 (CLR) 交互的方法。</span><span class="sxs-lookup"><span data-stu-id="b27b7-104">Provides methods for interaction with a target item of the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b27b7-105">方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-105">Methods</span></span>  
  
|<span data-ttu-id="b27b7-106">方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-106">Method</span></span>|<span data-ttu-id="b27b7-107">说明</span><span class="sxs-lookup"><span data-stu-id="b27b7-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b27b7-108">GetCurrentThreadID 方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-108">GetCurrentThreadID Method</span></span>](iclrdatatarget-getcurrentthreadid-method.md)|<span data-ttu-id="b27b7-109">获取当前线程的操作系统标识符。</span><span class="sxs-lookup"><span data-stu-id="b27b7-109">Gets the operating system identifier for the current thread.</span></span>|  
|[<span data-ttu-id="b27b7-110">GetImageBase 方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-110">GetImageBase Method</span></span>](iclrdatatarget-getimagebase-method.md)|<span data-ttu-id="b27b7-111">获取指定的图像的基本内存地址。</span><span class="sxs-lookup"><span data-stu-id="b27b7-111">Gets the base memory address for the specified image.</span></span>|  
|[<span data-ttu-id="b27b7-112">GetMachineType 方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-112">GetMachineType Method</span></span>](iclrdatatarget-getmachinetype-method.md)|<span data-ttu-id="b27b7-113">获取目标进程正在使用的指令集类型的标识符。</span><span class="sxs-lookup"><span data-stu-id="b27b7-113">Gets an identifier for the kind of instruction set that the target process is using.</span></span>|  
|[<span data-ttu-id="b27b7-114">GetPointerSize 方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-114">GetPointerSize Method</span></span>](iclrdatatarget-getpointersize-method.md)|<span data-ttu-id="b27b7-115">获取指向当前目标的指针的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="b27b7-115">Gets the size, in bytes, of a pointer to the current target.</span></span>|  
|[<span data-ttu-id="b27b7-116">GetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-116">GetThreadContext Method</span></span>](iclrdatatarget-getthreadcontext-method.md)|<span data-ttu-id="b27b7-117">获取一个指针，该指针指向具有指定标识符的线程的上下文。</span><span class="sxs-lookup"><span data-stu-id="b27b7-117">Gets a pointer to the context of the thread with the specified identifier.</span></span>|  
|[<span data-ttu-id="b27b7-118">GetTLSValue 方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-118">GetTLSValue Method</span></span>](iclrdatatarget-gettlsvalue-method.md)|<span data-ttu-id="b27b7-119">在线程本地存储区中获取指定线程 (TLS) 中的值。</span><span class="sxs-lookup"><span data-stu-id="b27b7-119">Gets a value in thread local storage (TLS) at the specified index for the specified thread.</span></span>|  
|[<span data-ttu-id="b27b7-120">ReadVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-120">ReadVirtual Method</span></span>](iclrdatatarget-readvirtual-method.md)|<span data-ttu-id="b27b7-121">将数据从指定的虚拟内存地址读入指定的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="b27b7-121">Reads data from the specified virtual memory address into the specified buffer.</span></span>|  
|[<span data-ttu-id="b27b7-122">Request 方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-122">Request Method</span></span>](iclrdatatarget-request-method.md)|<span data-ttu-id="b27b7-123">由公共语言运行时调用 (CLR) 数据访问服务请求操作，如实现所定义。</span><span class="sxs-lookup"><span data-stu-id="b27b7-123">Called by the common language runtime (CLR) data access services to request an operation, as defined by the implementation.</span></span>|  
|[<span data-ttu-id="b27b7-124">SetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-124">SetThreadContext Method</span></span>](iclrdatatarget-setthreadcontext-method.md)|<span data-ttu-id="b27b7-125">设置目标进程中指定线程的当前上下文。</span><span class="sxs-lookup"><span data-stu-id="b27b7-125">Sets the current context of the specified thread in the target process.</span></span>|  
|[<span data-ttu-id="b27b7-126">SetTLSValue 方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-126">SetTLSValue Method</span></span>](iclrdatatarget-settlsvalue-method.md)|<span data-ttu-id="b27b7-127">在目标进程中指定线程 (TLS) 中设置一个值。</span><span class="sxs-lookup"><span data-stu-id="b27b7-127">Sets a value in the thread local storage (TLS) of the specified thread in the target process.</span></span>|  
|[<span data-ttu-id="b27b7-128">WriteVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="b27b7-128">WriteVirtual Method</span></span>](iclrdatatarget-writevirtual-method.md)|<span data-ttu-id="b27b7-129">将数据从指定的缓冲区写入指定的虚拟内存地址。</span><span class="sxs-lookup"><span data-stu-id="b27b7-129">Writes data from the specified buffer to the specified virtual memory address.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b27b7-130">备注</span><span class="sxs-lookup"><span data-stu-id="b27b7-130">Remarks</span></span>  

 <span data-ttu-id="b27b7-131">API 客户端 (即，调试器) 必须根据特定目标项实现此接口。</span><span class="sxs-lookup"><span data-stu-id="b27b7-131">The API client (that is, the debugger) must implement this interface as appropriate for the particular target item.</span></span> <span data-ttu-id="b27b7-132">例如，活动进程的实现将不同于内存转储的。</span><span class="sxs-lookup"><span data-stu-id="b27b7-132">For example, a live process would have an implementation different from that of a memory dump.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b27b7-133">要求</span><span class="sxs-lookup"><span data-stu-id="b27b7-133">Requirements</span></span>  

 <span data-ttu-id="b27b7-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b27b7-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b27b7-135">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="b27b7-135">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="b27b7-136">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b27b7-136">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b27b7-137">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b27b7-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b27b7-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="b27b7-138">See also</span></span>

- [<span data-ttu-id="b27b7-139">ICLRDataTarget2 接口</span><span class="sxs-lookup"><span data-stu-id="b27b7-139">ICLRDataTarget2 Interface</span></span>](iclrdatatarget2-interface.md)
- [<span data-ttu-id="b27b7-140">调试接口</span><span class="sxs-lookup"><span data-stu-id="b27b7-140">Debugging Interfaces</span></span>](debugging-interfaces.md)
