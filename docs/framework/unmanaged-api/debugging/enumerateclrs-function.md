---
description: 了解详细信息： EnumerateCLRs 函数
title: EnumerateCLRs 函数
ms.date: 03/30/2017
api_name:
- EnumerateCLRs
api_location:
- dbgshim.dll
api_type:
- COM
f1_keywords:
- EnumerateCLRs
helpviewer_keywords:
- debugging API [Silverlight]
- Silverlight, debugging
- EnumerateCLRs function
ms.assetid: f8d50cb3-ec4f-4529-8fe3-bd61fd28e13c
topic_type:
- apiref
ms.openlocfilehash: 75124ef1e1e8588cb3d709161c3c1119e960be9e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637776"
---
# <a name="enumerateclrs-function"></a><span data-ttu-id="35964-103">EnumerateCLRs 函数</span><span class="sxs-lookup"><span data-stu-id="35964-103">EnumerateCLRs Function</span></span>

<span data-ttu-id="35964-104">提供枚举进程中 CLR 的机制。</span><span class="sxs-lookup"><span data-stu-id="35964-104">Provides a mechanism for enumerating the CLRs in a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35964-105">语法</span><span class="sxs-lookup"><span data-stu-id="35964-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateCLRs (  
    [in]  DWORD      debuggeePID,  
    [out] HANDLE**   ppHandleArrayOut,  
    [out] LPWSTR**   ppStringArrayOut,  
    [out] DWORD*     pdwArrayLengthOut  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="35964-106">参数</span><span class="sxs-lookup"><span data-stu-id="35964-106">Parameters</span></span>  

 `debuggeePID`  
 <span data-ttu-id="35964-107">[in] 要从其枚举已加载的 CLR 的进程的进程标识符。</span><span class="sxs-lookup"><span data-stu-id="35964-107">[in] Process identifier of the process from which loaded CLRs will be enumerated.</span></span>  
  
 `ppHandleArrayOut`  
 <span data-ttu-id="35964-108">[out] 指向包含用于继续 CLR 启动的事件句柄的数组的指针。</span><span class="sxs-lookup"><span data-stu-id="35964-108">[out] Pointer to an array containing event handles that are used to continue a CLR startup.</span></span> <span data-ttu-id="35964-109">不保证数组中的每个句柄都有效。</span><span class="sxs-lookup"><span data-stu-id="35964-109">Each handle in the array is not guaranteed to be valid.</span></span> <span data-ttu-id="35964-110">有效的句柄将作为相应运行时（位于与 `ppStringArrayOut` 相同的索引中）的继续启动事件使用。</span><span class="sxs-lookup"><span data-stu-id="35964-110">If valid, the handle is to be used as the continue-startup event for the corresponding runtime located in the same index of `ppStringArrayOut`.</span></span>  
  
 `ppStringArrayOut`  
 <span data-ttu-id="35964-111">[out] 指向一个字符串数组的指针，该字符串数组指定进程中加载的 CLR 的完整路径。</span><span class="sxs-lookup"><span data-stu-id="35964-111">[out] Pointer to an array of strings that specify full paths to CLRs loaded in the process.</span></span>  
  
 `pdwArrayLengthOut`  
 <span data-ttu-id="35964-112">[out] 指向包含大小相等的 `ppHandleArrayOut` 和 `pdwArrayLengthOut` 的长度的 DWORD 的指针。</span><span class="sxs-lookup"><span data-stu-id="35964-112">[out] Pointer to a DWORD that contains the length of the equally sized `ppHandleArrayOut` and `pdwArrayLengthOut`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="35964-113">返回值</span><span class="sxs-lookup"><span data-stu-id="35964-113">Return Value</span></span>  

 <span data-ttu-id="35964-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="35964-114">S_OK</span></span>  
 <span data-ttu-id="35964-115">已成功确定该进程中的 CLR 的数目，并已正确填写相应的句柄数组和路径数组。</span><span class="sxs-lookup"><span data-stu-id="35964-115">The number of CLRs in the process was successfully determined, and the corresponding handle and path arrays were properly filled.</span></span>  
  
 <span data-ttu-id="35964-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="35964-116">E_INVALIDARG</span></span>  
 <span data-ttu-id="35964-117">`ppHandleArrayOut` 或 `ppStringArrayOut` 为 null，或 `pdwArrayLengthOut` 为 null。</span><span class="sxs-lookup"><span data-stu-id="35964-117">Either `ppHandleArrayOut` or `ppStringArrayOut` is null, or `pdwArrayLengthOut` is null.</span></span>  
  
 <span data-ttu-id="35964-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="35964-118">E_OUTOFMEMORY</span></span>  
 <span data-ttu-id="35964-119">该函数不能为句柄和路径数组分配足够的内存。</span><span class="sxs-lookup"><span data-stu-id="35964-119">The function is unable to allocate enough memory for the handle and path arrays.</span></span>  
  
 <span data-ttu-id="35964-120">E_FAIL（或其他 E_ 返回代码）</span><span class="sxs-lookup"><span data-stu-id="35964-120">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="35964-121">无法枚举加载的 CLR。</span><span class="sxs-lookup"><span data-stu-id="35964-121">Unable to enumerate loaded CLRs.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="35964-122">备注</span><span class="sxs-lookup"><span data-stu-id="35964-122">Remarks</span></span>  

 <span data-ttu-id="35964-123">对于由 `debuggeePID` 标识的目标进程，函数将路径数组 `ppStringArrayOut` 返回到进程中加载的 CLR；并返回事件句柄数组 `ppHandleArrayOut`（其中可能包含相同索引处 CLR 的继续启动事件）以及数组的大小 `pdwArrayLengthOut`（它指定已加载的 CLR 的数目）。</span><span class="sxs-lookup"><span data-stu-id="35964-123">For a target process that is identified by `debuggeePID`, the function returns an array of paths, `ppStringArrayOut`, to CLRs loaded in the process; an array of event handles, `ppHandleArrayOut`, which may contain a continue-startup event for the CLR at the same index; and the size of the arrays, `pdwArrayLengthOut`, which specifies the number of CLRs that are loaded.</span></span>  
  
 <span data-ttu-id="35964-124">在 Windows 操作系统上，`debuggeePID` 映射到 OS 进程标识符。</span><span class="sxs-lookup"><span data-stu-id="35964-124">On the Windows operating system, `debuggeePID` maps to an OS process identifier.</span></span>  
  
 <span data-ttu-id="35964-125">`ppHandleArrayOut` 和 `ppStringArrayOut` 的内存由此函数分配。</span><span class="sxs-lookup"><span data-stu-id="35964-125">The memory for `ppHandleArrayOut` and `ppStringArrayOut` are allocated by this function.</span></span> <span data-ttu-id="35964-126">若要释放分配的内存，必须调用 [CloseCLREnumeration 函数](closeclrenumeration-function.md)。</span><span class="sxs-lookup"><span data-stu-id="35964-126">To free the memory allocated, you must call [CloseCLREnumeration Function](closeclrenumeration-function.md).</span></span>  
  
 <span data-ttu-id="35964-127">为了在目标进程中返回 CLR 计数，可在两个数组参数均设为 null 的情况下调用此函数。</span><span class="sxs-lookup"><span data-stu-id="35964-127">This function can be called with both array parameters set to null in order to return the count of CLRs in the target process.</span></span> <span data-ttu-id="35964-128">调用方可以从此计数推断将创建的缓冲区的大小：`(sizeof(HANDLE) * count) + (sizeof(LPWSTR) * count) + (sizeof(WCHAR*) * count * MAX_PATH)`。</span><span class="sxs-lookup"><span data-stu-id="35964-128">From this count, a caller can infer the size of the buffer that will be created: `(sizeof(HANDLE) * count) + (sizeof(LPWSTR) * count) + (sizeof(WCHAR*) * count * MAX_PATH)`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="35964-129">要求</span><span class="sxs-lookup"><span data-stu-id="35964-129">Requirements</span></span>  

 <span data-ttu-id="35964-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="35964-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="35964-131">**标头：** dbgshim.dll</span><span class="sxs-lookup"><span data-stu-id="35964-131">**Header:** dbgshim.h</span></span>  
  
 <span data-ttu-id="35964-132">**库：** dbgshim.dll</span><span class="sxs-lookup"><span data-stu-id="35964-132">**Library:** dbgshim.dll</span></span>  
  
 <span data-ttu-id="35964-133">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="35964-133">**.NET Framework Versions:** 3.5 SP1</span></span>
