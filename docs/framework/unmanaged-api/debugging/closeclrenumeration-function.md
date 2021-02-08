---
description: 了解详细信息： CloseCLREnumeration 函数
title: CloseCLREnumeration 函数
ms.date: 03/30/2017
api_name:
- CloseCLREnumeration
api_location:
- dbgshim.dll
api_type:
- COM
f1_keywords:
- CloseCLREnumeration
helpviewer_keywords:
- debugging API [Silverlight]
- Silverlight, debugging
- CloseCLR Enumeration function
ms.assetid: 5e3c3958-80bb-43b1-a96b-dd3e6dbd9cd7
topic_type:
- apiref
ms.openlocfilehash: 7669332cc23b78afbb3bf597e7d208a5f707aae5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772765"
---
# <a name="closeclrenumeration-function"></a><span data-ttu-id="5fd51-103">CloseCLREnumeration 函数</span><span class="sxs-lookup"><span data-stu-id="5fd51-103">CloseCLREnumeration Function</span></span>

<span data-ttu-id="5fd51-104">关闭位于 [EnumerateCLRs 函数](enumerateclrs-function.md)所返回的句柄数组中 (CLR) 继续启动事件，并释放句柄和字符串路径数组的内存。</span><span class="sxs-lookup"><span data-stu-id="5fd51-104">Closes any valid common language runtime (CLR) continue-startup events located in an array of handles returned by the [EnumerateCLRs function](enumerateclrs-function.md), and frees the memory for the handle and string path arrays.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5fd51-105">语法</span><span class="sxs-lookup"><span data-stu-id="5fd51-105">Syntax</span></span>  
  
```cpp  
HRESULT CloseCLREnumeration (  
    [in]  DWORD      pHandleArray,  
    [in]  LPWSTR**   pStringArray,  
    [in]  DWORD*     dwArrayLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5fd51-106">参数</span><span class="sxs-lookup"><span data-stu-id="5fd51-106">Parameters</span></span>  

 `pHandleArray`  
 <span data-ttu-id="5fd51-107">中指向从 [EnumerateCLRs 函数](enumerateclrs-function.md)返回的事件句柄的数组的指针。</span><span class="sxs-lookup"><span data-stu-id="5fd51-107">[in] Pointer to the array of event handles returned from the [EnumerateCLRs function](enumerateclrs-function.md).</span></span>  
  
 `pStringArray`  
 <span data-ttu-id="5fd51-108">中一个指针，指向从 [EnumerateCLRs 函数](enumerateclrs-function.md)返回的 CLR 字符串路径的数组。</span><span class="sxs-lookup"><span data-stu-id="5fd51-108">[in] Pointer to the array of CLR string paths returned from the [EnumerateCLRs function](enumerateclrs-function.md).</span></span>  
  
 `dwArrayLength`  
 <span data-ttu-id="5fd51-109">[in] 包含 `pHandleArray` 或 `pStringArray`大小（长度）（它们是相同）的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="5fd51-109">[in] DWORD that contains the size (length) of either `pHandleArray` or `pStringArray` (they are the same).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5fd51-110">返回值</span><span class="sxs-lookup"><span data-stu-id="5fd51-110">Return Value</span></span>  

 <span data-ttu-id="5fd51-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="5fd51-111">S_OK</span></span>  
 <span data-ttu-id="5fd51-112">[EnumerateCLRs 函数](enumerateclrs-function.md)打开的句柄将关闭，并且将释放分配给句柄和字符串数组的内存。</span><span class="sxs-lookup"><span data-stu-id="5fd51-112">Handles opened by the [EnumerateCLRs function](enumerateclrs-function.md) are closed, and memory allocated for the handle and string arrays is freed.</span></span>  
  
 <span data-ttu-id="5fd51-113">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="5fd51-113">E_INVALIDARG</span></span>  
 <span data-ttu-id="5fd51-114">`pHandleArray` 的长度与传入 `dwArrayLength` 的长度不匹配。</span><span class="sxs-lookup"><span data-stu-id="5fd51-114">The length of `pHandleArray` does not match the length that is passed in `dwArrayLength`.</span></span>  
  
 <span data-ttu-id="5fd51-115">E_FAIL（或其他 E_ 返回代码）</span><span class="sxs-lookup"><span data-stu-id="5fd51-115">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="5fd51-116">此函数无法释放 `pHandleArray` 和 `pStringArray` 的内存。</span><span class="sxs-lookup"><span data-stu-id="5fd51-116">The function is unable to free the memory for `pHandleArray` and `pStringArray`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5fd51-117">要求</span><span class="sxs-lookup"><span data-stu-id="5fd51-117">Requirements</span></span>  

 <span data-ttu-id="5fd51-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5fd51-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5fd51-119">**标头：** dbgshim.dll</span><span class="sxs-lookup"><span data-stu-id="5fd51-119">**Header:** dbgshim.h</span></span>  
  
 <span data-ttu-id="5fd51-120">**库：** dbgshim.dll</span><span class="sxs-lookup"><span data-stu-id="5fd51-120">**Library:** dbgshim.dll</span></span>  
  
 <span data-ttu-id="5fd51-121">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="5fd51-121">**.NET Framework Versions:** 3.5 SP1</span></span>
