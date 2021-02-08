---
description: 了解详细信息： ICoreClrDebugTarget：： EnumRuntimes 方法
title: ICoreClrDebugTarget::EnumRuntimes 方法
ms.date: 03/30/2017
api_name:
- ICoreClrDebugTarget.EnumRuntimes
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- ICoreClrDebugTarget::EnumRuntimes
helpviewer_keywords:
- remote debugging API [Silverlight]
- ICorClrDebugTarget::EnumRuntimes method [Silverlight debugging]
- EnumRuntimes method, ICoreClrDebugTarget interface [Silverlight debugging]
- Silverlight, remote debugging
ms.assetid: 316df866-442d-40cc-b049-45e8adcb65d1
topic_type:
- apiref
ms.openlocfilehash: 675747106b2acec2e8be3fcdf15831958bea7c7c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794619"
---
# <a name="icoreclrdebugtargetenumruntimes-method"></a><span data-ttu-id="9df9e-103">ICoreClrDebugTarget::EnumRuntimes 方法</span><span class="sxs-lookup"><span data-stu-id="9df9e-103">ICoreClrDebugTarget::EnumRuntimes Method</span></span>

<span data-ttu-id="9df9e-104">枚举在远程计算机上运行的指定进程中的公共语言运行时 (CLR)。</span><span class="sxs-lookup"><span data-stu-id="9df9e-104">Enumerates the common language runtimes (CLRs) in the specified process that is running on a remote computer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9df9e-105">语法</span><span class="sxs-lookup"><span data-stu-id="9df9e-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumRuntimes (  
      [in] DWORD       dwInternalProcessID,  
      [out] DWORD*     pcRuntimes,  
      [out] CoreClrDebugRuntimeInfo**    ppRuntimes  
    );  
```  
  
## <a name="parameters"></a><span data-ttu-id="9df9e-106">参数</span><span class="sxs-lookup"><span data-stu-id="9df9e-106">Parameters</span></span>  

 `dwInternalProcessID`  
 <span data-ttu-id="9df9e-107">[in] 要枚举运行时的进程的内部进程 ID。</span><span class="sxs-lookup"><span data-stu-id="9df9e-107">[in] The internal process ID of the process for which you want to enumerate runtimes.</span></span> <span data-ttu-id="9df9e-108">这将 `m_dwInternalID` 来自相应的 [CoreClrDebugProcInfo](coreclrdebugprocinfo-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="9df9e-108">This will be `m_dwInternalID` from the corresponding [CoreClrDebugProcInfo](coreclrdebugprocinfo-structure.md).</span></span>  
  
 `pcRuntimes`  
 <span data-ttu-id="9df9e-109">[out] `ppRuntimes` 中返回的运行时的数量。</span><span class="sxs-lookup"><span data-stu-id="9df9e-109">[out] The number of runtimes returned in `ppRuntimes`.</span></span> <span data-ttu-id="9df9e-110">此值可为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="9df9e-110">This value can be 0 (zero).</span></span>  
  
 `ppRuntimes`  
 <span data-ttu-id="9df9e-111">弄 [CoreClrDebugRuntimeInfo](coreclrdebugruntimeinfo-structure.md) 结构的数组，这些结构表示远程目标进程中加载的运行时。</span><span class="sxs-lookup"><span data-stu-id="9df9e-111">[out] An array of [CoreClrDebugRuntimeInfo](coreclrdebugruntimeinfo-structure.md) structures that represent the runtimes loaded in the remote target process.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9df9e-112">返回值</span><span class="sxs-lookup"><span data-stu-id="9df9e-112">Return Value</span></span>  

 <span data-ttu-id="9df9e-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9df9e-113">S_OK</span></span>  
 <span data-ttu-id="9df9e-114">成功。</span><span class="sxs-lookup"><span data-stu-id="9df9e-114">Success.</span></span>  
  
 <span data-ttu-id="9df9e-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="9df9e-115">S_FALSE</span></span>  
 <span data-ttu-id="9df9e-116">`dwInternalProcessID` 不匹配计算机上运行的任何进程，可能因为进程已终止。</span><span class="sxs-lookup"><span data-stu-id="9df9e-116">`dwInternalProcessID` does not match any process that is running on the computer, probably because the process was terminated.</span></span> <span data-ttu-id="9df9e-117">`pcRuntimes` 和 `ppRuntimes` 将为 null。</span><span class="sxs-lookup"><span data-stu-id="9df9e-117">`pcRuntimes` and `ppRuntimes` will be null.</span></span>  
  
 <span data-ttu-id="9df9e-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="9df9e-118">E_OUTOFMEMORY</span></span>  
 <span data-ttu-id="9df9e-119">无法为 `ppRuntimes` 分配足够的内存。</span><span class="sxs-lookup"><span data-stu-id="9df9e-119">Unable to allocate enough memory for `ppRuntimes`.</span></span>  
  
 <span data-ttu-id="9df9e-120">E_FAIL（或其他 E_ 返回代码）</span><span class="sxs-lookup"><span data-stu-id="9df9e-120">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="9df9e-121">其他故障。</span><span class="sxs-lookup"><span data-stu-id="9df9e-121">Other failures.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9df9e-122">备注</span><span class="sxs-lookup"><span data-stu-id="9df9e-122">Remarks</span></span>  

 <span data-ttu-id="9df9e-123">若要释放此方法分配的内存，请调用 [ICoreClrDebugTarget：： FreeMemory](icoreclrdebugtarget-freememory-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9df9e-123">To free the memory that was allocated by this method, call the [ICoreClrDebugTarget::FreeMemory](icoreclrdebugtarget-freememory-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9df9e-124">要求</span><span class="sxs-lookup"><span data-stu-id="9df9e-124">Requirements</span></span>  

 <span data-ttu-id="9df9e-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9df9e-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9df9e-126">**标头：** CoreClrRemoteDebuggingInterfaces</span><span class="sxs-lookup"><span data-stu-id="9df9e-126">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="9df9e-127">**库：** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="9df9e-127">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="9df9e-128">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="9df9e-128">**.NET Framework Versions:** 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9df9e-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="9df9e-129">See also</span></span>

- [<span data-ttu-id="9df9e-130">ICoreClrDebugTarget 接口</span><span class="sxs-lookup"><span data-stu-id="9df9e-130">ICoreClrDebugTarget Interface</span></span>](icoreclrdebugtarget-interface.md)
