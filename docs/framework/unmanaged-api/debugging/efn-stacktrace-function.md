---
description: 了解详细信息： _EFN_StackTrace 函数
title: _EFN_StackTrace 函数
ms.date: 03/30/2017
api_name:
- _EFN_StackTrace
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- _EFN_StackTrace
helpviewer_keywords:
- _EFN_StackTrace function [.NET Framework debugging]
ms.assetid: caea7754-867c-4360-a65c-5ced4408fd9d
topic_type:
- apiref
ms.openlocfilehash: 6092d0793967cc422e30342783ab4dfd70b33de9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738255"
---
# <a name="_efn_stacktrace-function"></a><span data-ttu-id="b9850-103">\_EFN \_ StackTrace 函数</span><span class="sxs-lookup"><span data-stu-id="b9850-103">\_EFN\_StackTrace Function</span></span>

<span data-ttu-id="b9850-104">提供托管堆栈跟踪的文本表示形式以及 `CONTEXT` 记录的数组，其中每项对应非托管代码和托管代码之间的每个转换。</span><span class="sxs-lookup"><span data-stu-id="b9850-104">Provides a text representation of a managed stack trace and an array of `CONTEXT` records, one for each transition between unmanaged and managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9850-105">语法</span><span class="sxs-lookup"><span data-stu-id="b9850-105">Syntax</span></span>  
  
```cpp  
HRESULT CALLBACK _EFN_StackTrace(  
    [in]  PDEBUG_CLIENT  Client,  
    [out] WCHAR          wszTextOut[],  
    [out] size_t         *puiTextLength,  
    [out] LPVOID         pTransitionContexts,  
    [out] size_t         *puiTransitionContextCount,  
    [in]  size_t         uiSizeOfContext,  
    [in]  DWORD          Flags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b9850-106">参数</span><span class="sxs-lookup"><span data-stu-id="b9850-106">Parameters</span></span>  

 `Client`  
 <span data-ttu-id="b9850-107">中正在调试的客户端。</span><span class="sxs-lookup"><span data-stu-id="b9850-107">[in] The client being debugged.</span></span>  
  
 `wszTextOut`  
 <span data-ttu-id="b9850-108">弄堆栈跟踪的文本表示形式。</span><span class="sxs-lookup"><span data-stu-id="b9850-108">[out] The text representation of the stack trace.</span></span>  
  
 `puiTextLength`  
 <span data-ttu-id="b9850-109">弄一个指针，指向中的字符数 `wszTextOut` 。</span><span class="sxs-lookup"><span data-stu-id="b9850-109">[out] A pointer to the number of characters in `wszTextOut`.</span></span>  
  
 `pTransitionContexts`  
 <span data-ttu-id="b9850-110">弄转换上下文的数组。</span><span class="sxs-lookup"><span data-stu-id="b9850-110">[out] The array of transition contexts.</span></span>  
  
 `puiTransitionContextCount`  
 <span data-ttu-id="b9850-111">弄指向数组中的转换上下文数的指针。</span><span class="sxs-lookup"><span data-stu-id="b9850-111">[out] A pointer to the number of transition contexts in the array.</span></span>  
  
 `uiSizeOfContext`  
 <span data-ttu-id="b9850-112">中上下文结构的大小。</span><span class="sxs-lookup"><span data-stu-id="b9850-112">[in] The size of the context structure.</span></span>  
  
 `Flags`  
 <span data-ttu-id="b9850-113">中设置为0或 SOS_STACKTRACE_SHOWADDRESSES (0x01) ，以显示 EBP 寄存器，并在每一行前面 (ESP) 输入堆栈指针 `module!functionname` 。</span><span class="sxs-lookup"><span data-stu-id="b9850-113">[in] Set to either 0 or SOS_STACKTRACE_SHOWADDRESSES (0x01) to show the EBP register and the enter stack pointer (ESP) in front of each `module!functionname` line.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b9850-114">备注</span><span class="sxs-lookup"><span data-stu-id="b9850-114">Remarks</span></span>  

 <span data-ttu-id="b9850-115">此 `_EFN_StackTrace` 结构可从 WinDbg 编程界面调用。</span><span class="sxs-lookup"><span data-stu-id="b9850-115">The `_EFN_StackTrace` structure can be called from a WinDbg programmatic interface.</span></span> <span data-ttu-id="b9850-116">参数的使用方式如下：</span><span class="sxs-lookup"><span data-stu-id="b9850-116">Parameters are used as follows:</span></span>  
  
- <span data-ttu-id="b9850-117">如果 `wszTextOut` 为 null 且不为 `puiTextLength` null，则该函数将返回中的字符串长度 `puiTextLength` 。</span><span class="sxs-lookup"><span data-stu-id="b9850-117">If `wszTextOut` is null and `puiTextLength` is not null, the function returns the string length in `puiTextLength`.</span></span>  
  
- <span data-ttu-id="b9850-118">如果不为 `wszTextOut` null，则该函数将文本存储 `wszTextOut` 到指示的位置 `puiTextLength` 。</span><span class="sxs-lookup"><span data-stu-id="b9850-118">If `wszTextOut` is not null, the function stores text in `wszTextOut` up to the location indicated by `puiTextLength`.</span></span> <span data-ttu-id="b9850-119">如果缓冲区中有足够的空间，则它将成功返回，如果缓冲区不够长，则返回 E_OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="b9850-119">It returns successfully if there was enough room in the buffer, or returns E_OUTOFMEMORY if the buffer was not long enough.</span></span>  
  
- <span data-ttu-id="b9850-120">如果 `pTransitionContexts` 和都为 null，则忽略函数的转换部分 `puiTransitionContextCount` 。</span><span class="sxs-lookup"><span data-stu-id="b9850-120">The transition portion of the function is ignored if `pTransitionContexts` and `puiTransitionContextCount` are both null.</span></span> <span data-ttu-id="b9850-121">在这种情况下，函数向调用方提供仅包含函数名称的文本输出。</span><span class="sxs-lookup"><span data-stu-id="b9850-121">In this case, the function provides callers with text output of only the function names.</span></span>  
  
- <span data-ttu-id="b9850-122">如果 `pTransitionContexts` 为 null 且不为 `puiTransitionContextCount` null，则该函数将在中返回所需数量的上下文项 `puiTransitionContextCount` 。</span><span class="sxs-lookup"><span data-stu-id="b9850-122">If `pTransitionContexts` is null and `puiTransitionContextCount` is not null, the function returns the necessary number of context entries in `puiTransitionContextCount`.</span></span>  
  
- <span data-ttu-id="b9850-123">如果 `pTransitionContexts` 不为 null，则函数会将其视为长度的结构数组 `puiTransitionContextCount` 。</span><span class="sxs-lookup"><span data-stu-id="b9850-123">If `pTransitionContexts` is not null, the function treats it as an array of structures of length `puiTransitionContextCount`.</span></span> <span data-ttu-id="b9850-124">结构大小由指定 `uiSizeOfContext` ，并且必须是 [SimpleContext](stacktrace-simplecontext-structure.md) 的大小或 `CONTEXT` 体系结构的大小。</span><span class="sxs-lookup"><span data-stu-id="b9850-124">The structure size is given by `uiSizeOfContext`, and must be the size of [SimpleContext](stacktrace-simplecontext-structure.md) or `CONTEXT` for the architecture.</span></span>  
  
- <span data-ttu-id="b9850-125">`wszTextOut` 采用以下格式编写：</span><span class="sxs-lookup"><span data-stu-id="b9850-125">`wszTextOut` is written in the following format:</span></span>  
  
    ```output  
    "<ModuleName>!<Function Name>[+<offset in hex>]  
    ...  
    (TRANSITION)  
    ..."  
    ```  
  
- <span data-ttu-id="b9850-126">如果偏移量（十六进制）为0x0，则不写入偏移量。</span><span class="sxs-lookup"><span data-stu-id="b9850-126">If the offset in hex is 0x0, no offset is written.</span></span>  
  
- <span data-ttu-id="b9850-127">如果线程上当前没有托管代码，该函数将返回 SOS_E_NOMANAGEDCODE。</span><span class="sxs-lookup"><span data-stu-id="b9850-127">If there is no managed code on the thread currently in context, the function returns SOS_E_NOMANAGEDCODE.</span></span>  
  
- <span data-ttu-id="b9850-128">`Flags`参数为0或 SOS_STACKTRACE_SHOWADDRESSES，以在每行的前面显示 EBP 和 ESP `module!functionname` 。</span><span class="sxs-lookup"><span data-stu-id="b9850-128">The `Flags` parameter is either 0 or SOS_STACKTRACE_SHOWADDRESSES to see EBP and ESP in front of each `module!functionname` line.</span></span> <span data-ttu-id="b9850-129">默认情况下，它是0。</span><span class="sxs-lookup"><span data-stu-id="b9850-129">By default, it is 0.</span></span>  
  
    ```cpp  
    #define SOS_STACKTRACE_SHOWADDRESSES   0x00000001  
    ```  
  
## <a name="requirements"></a><span data-ttu-id="b9850-130">要求</span><span class="sxs-lookup"><span data-stu-id="b9850-130">Requirements</span></span>  

 <span data-ttu-id="b9850-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b9850-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9850-132">**标头：** SOS_Stacktrace。h</span><span class="sxs-lookup"><span data-stu-id="b9850-132">**Header:** SOS_Stacktrace.h</span></span>  
  
 <span data-ttu-id="b9850-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b9850-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9850-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="b9850-134">See also</span></span>

- [<span data-ttu-id="b9850-135">调试全局静态函数</span><span class="sxs-lookup"><span data-stu-id="b9850-135">Debugging Global Static Functions</span></span>](debugging-global-static-functions.md)
