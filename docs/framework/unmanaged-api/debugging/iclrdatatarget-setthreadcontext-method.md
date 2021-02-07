---
description: 了解详细信息： ICLRDataTarget：： SetThreadContext 方法
title: ICLRDataTarget::SetThreadContext 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.SetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::SetThreadContext
helpviewer_keywords:
- SetThreadContext method, ICLRDataTarget interface [.NET Framework debugging]
- ICLRDataTarget::SetThreadContext method [.NET Framework debugging]
ms.assetid: 103c8502-81fe-40d7-9c1e-9008d8fb19e1
topic_type:
- apiref
ms.openlocfilehash: fc428bc887f7ba10f3096cdf17a757fb252418f0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738182"
---
# <a name="iclrdatatargetsetthreadcontext-method"></a><span data-ttu-id="6b2bc-103">ICLRDataTarget::SetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="6b2bc-103">ICLRDataTarget::SetThreadContext Method</span></span>

<span data-ttu-id="6b2bc-104">设置目标进程中指定线程的当前上下文。</span><span class="sxs-lookup"><span data-stu-id="6b2bc-104">Sets the current context of the specified thread in the target process.</span></span> <span data-ttu-id="6b2bc-105">此方法由公共语言运行时 (CLR) 数据访问服务调用。</span><span class="sxs-lookup"><span data-stu-id="6b2bc-105">This method is called by the common language runtime (CLR) data access services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6b2bc-106">语法</span><span class="sxs-lookup"><span data-stu-id="6b2bc-106">Syntax</span></span>  
  
```cpp  
HRESULT SetThreadContext (  
    [in] ULONG32            threadID,  
    [in] ULONG32            contextSize,  
    [in, size_is(contextSize)]
         BYTE               *context  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6b2bc-107">参数</span><span class="sxs-lookup"><span data-stu-id="6b2bc-107">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="6b2bc-108">中目标进程中的线程的操作系统标识符。</span><span class="sxs-lookup"><span data-stu-id="6b2bc-108">[in] The operating system identifier of a thread in the target process.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="6b2bc-109">中上下文的大小。</span><span class="sxs-lookup"><span data-stu-id="6b2bc-109">[in] The size of the context.</span></span>  
  
 `context`  
 <span data-ttu-id="6b2bc-110">中指向包含上下文的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="6b2bc-110">[in] Pointer to a buffer containing the context.</span></span>  
  
 <span data-ttu-id="6b2bc-111">缓冲区中的数据 `context` 将采用 Win32 结构的格式 `CONTEXT` 。</span><span class="sxs-lookup"><span data-stu-id="6b2bc-111">The data in the `context` buffer will be in the format of the Win32 `CONTEXT` structure.</span></span> <span data-ttu-id="6b2bc-112">上下文指定处理器特定的寄存器数据，因此 Win32 结构的定义 `CONTEXT` 取决于处理器的体系结构。</span><span class="sxs-lookup"><span data-stu-id="6b2bc-112">The context specifies processor-specific register data, so the definition of the Win32 `CONTEXT` structure depends on the processor's architecture.</span></span> <span data-ttu-id="6b2bc-113">有关 Win32 结构的定义，请参阅 WinNT. .h 头文件 `CONTEXT` 。</span><span class="sxs-lookup"><span data-stu-id="6b2bc-113">Refer to the WinNT.h header file for the definition of the Win32 `CONTEXT` structure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6b2bc-114">备注</span><span class="sxs-lookup"><span data-stu-id="6b2bc-114">Remarks</span></span>  

 <span data-ttu-id="6b2bc-115">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="6b2bc-115">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6b2bc-116">要求</span><span class="sxs-lookup"><span data-stu-id="6b2bc-116">Requirements</span></span>  

 <span data-ttu-id="6b2bc-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6b2bc-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6b2bc-118">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="6b2bc-118">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="6b2bc-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6b2bc-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6b2bc-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6b2bc-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6b2bc-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="6b2bc-121">See also</span></span>

- [<span data-ttu-id="6b2bc-122">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="6b2bc-122">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
