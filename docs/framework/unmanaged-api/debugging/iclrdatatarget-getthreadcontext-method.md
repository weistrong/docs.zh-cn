---
description: 了解详细信息： ICLRDataTarget：： GetThreadContext 方法
title: ICLRDataTarget::GetThreadContext 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.GetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::GetThreadContext
helpviewer_keywords:
- ICLRDataTarget::GetThreadContext method [.NET Framework debugging]
- GetThreadContext method, ICLRDataTarget interface [.NET Framework debugging]
ms.assetid: b9d8c3b5-3a2e-4225-95d4-dd052c4532c3
topic_type:
- apiref
ms.openlocfilehash: 210f4294aed31307557db419a0fb567cc71d4354
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785679"
---
# <a name="iclrdatatargetgetthreadcontext-method"></a><span data-ttu-id="a6df4-103">ICLRDataTarget::GetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="a6df4-103">ICLRDataTarget::GetThreadContext Method</span></span>

<span data-ttu-id="a6df4-104">获取目标进程中给定线程的当前执行上下文。</span><span class="sxs-lookup"><span data-stu-id="a6df4-104">Gets the current execution context for the given thread in the target process.</span></span> <span data-ttu-id="a6df4-105">此方法由公共语言运行时数据访问服务调用。</span><span class="sxs-lookup"><span data-stu-id="a6df4-105">This method is called by the common language runtime data access services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6df4-106">语法</span><span class="sxs-lookup"><span data-stu-id="a6df4-106">Syntax</span></span>  
  
```cpp  
HRESULT GetThreadContext (  
    [in] ULONG32            threadID,  
    [in] ULONG32            contextFlags,  
    [in] ULONG32            contextSize,  
    [out, size_is(contextSize)]
        BYTE                *context  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a6df4-107">参数</span><span class="sxs-lookup"><span data-stu-id="a6df4-107">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="a6df4-108">中目标进程中的线程的操作系统标识符。</span><span class="sxs-lookup"><span data-stu-id="a6df4-108">[in] The operating system identifier of a thread in the target process.</span></span>  
  
 `contextFlags`  
 <span data-ttu-id="a6df4-109">中指定要返回的上下文部分的标志。</span><span class="sxs-lookup"><span data-stu-id="a6df4-109">[in] Flags that specify which parts of the context to return.</span></span> <span data-ttu-id="a6df4-110">该实现将返回至少上下文的这些部分。</span><span class="sxs-lookup"><span data-stu-id="a6df4-110">The implementation will return at least these parts of the context.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="a6df4-111">中上下文的大小。</span><span class="sxs-lookup"><span data-stu-id="a6df4-111">[in] The size of the context.</span></span>  
  
 `context`  
 <span data-ttu-id="a6df4-112">弄指向要在其中放置上下文的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="a6df4-112">[out] Pointer to a buffer in which to place the context.</span></span>  
  
 <span data-ttu-id="a6df4-113">缓冲区中的数据 `context` 必须采用 Win32 结构的格式 `CONTEXT` 。</span><span class="sxs-lookup"><span data-stu-id="a6df4-113">The data in the `context` buffer must be in the format of the Win32 `CONTEXT` structure.</span></span> <span data-ttu-id="a6df4-114">上下文指定处理器特定的寄存器数据，因此 Win32 结构的定义 `CONTEXT` 取决于处理器的体系结构。</span><span class="sxs-lookup"><span data-stu-id="a6df4-114">The context specifies processor-specific register data, so the definition of the Win32 `CONTEXT` structure depends on the processor's architecture.</span></span> <span data-ttu-id="a6df4-115">有关 Win32 结构的定义，请参阅 WinNT. .h 头文件 `CONTEXT` 。</span><span class="sxs-lookup"><span data-stu-id="a6df4-115">Refer to the WinNT.h header file for the definition of the Win32 `CONTEXT` structure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a6df4-116">备注</span><span class="sxs-lookup"><span data-stu-id="a6df4-116">Remarks</span></span>  

 <span data-ttu-id="a6df4-117">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="a6df4-117">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a6df4-118">要求</span><span class="sxs-lookup"><span data-stu-id="a6df4-118">Requirements</span></span>  

 <span data-ttu-id="a6df4-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a6df4-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a6df4-120">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="a6df4-120">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="a6df4-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a6df4-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a6df4-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a6df4-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6df4-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="a6df4-123">See also</span></span>

- [<span data-ttu-id="a6df4-124">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="a6df4-124">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
