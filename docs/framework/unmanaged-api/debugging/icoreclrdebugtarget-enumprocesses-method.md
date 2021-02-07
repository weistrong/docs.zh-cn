---
description: 了解详细信息： ICoreClrDebugTarget：： EnumProcesses 方法
title: ICoreClrDebugTarget::EnumProcesses 方法
ms.date: 03/30/2017
api_name:
- ICoreClrDebugTarget.EnumProcesses
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- ICoreClrDebugTarget::EnumProcesses
helpviewer_keywords:
- remote debugging API [Silverlight]
- EnumProcesses method, ICorClrDebugTarget interface [Silverlight debugging]
- ICorClrDebugTarget::EnumProcesses method [Silverlight debugging]
- Silverlight, remote debugging
ms.assetid: e00fd477-4f49-43d3-bd0e-3094824b1136
topic_type:
- apiref
ms.openlocfilehash: 73dc8a2b00f7a57879855158e6b871117d015f3c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738034"
---
# <a name="icoreclrdebugtargetenumprocesses-method"></a><span data-ttu-id="799b8-103">ICoreClrDebugTarget::EnumProcesses 方法</span><span class="sxs-lookup"><span data-stu-id="799b8-103">ICoreClrDebugTarget::EnumProcesses Method</span></span>

<span data-ttu-id="799b8-104">枚举远程计算机上运行的进程。</span><span class="sxs-lookup"><span data-stu-id="799b8-104">Enumerates the processes that are running on a remote computer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="799b8-105">语法</span><span class="sxs-lookup"><span data-stu-id="799b8-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumProcesses (  
       [out]  DWORD*                  pcProcs,
       [out]  CoreClrDebugProcInfo**  ppProcs  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="799b8-106">参数</span><span class="sxs-lookup"><span data-stu-id="799b8-106">Parameters</span></span>  

 `pcProcs`  
 <span data-ttu-id="799b8-107">[out] `ppProcs` 中返回的进程数。</span><span class="sxs-lookup"><span data-stu-id="799b8-107">[out] The number of processes returned in `ppProcs`.</span></span> <span data-ttu-id="799b8-108">此值可为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="799b8-108">This value can be 0 (zero).</span></span>  
  
 `ppProcs`  
 <span data-ttu-id="799b8-109">弄 [CoreClrDebugProcInfo](coreclrdebugprocinfo-structure.md) 结构的数组，这些结构表示远程计算机上运行的进程。</span><span class="sxs-lookup"><span data-stu-id="799b8-109">[out] An array of [CoreClrDebugProcInfo](coreclrdebugprocinfo-structure.md) structures that represent the processes running on the remote computer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="799b8-110">返回值</span><span class="sxs-lookup"><span data-stu-id="799b8-110">Return Value</span></span>  

 <span data-ttu-id="799b8-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="799b8-111">S_OK</span></span>  
 <span data-ttu-id="799b8-112">成功。</span><span class="sxs-lookup"><span data-stu-id="799b8-112">Success.</span></span>  
  
 <span data-ttu-id="799b8-113">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="799b8-113">E_OUTOFMEMORY</span></span>  
 <span data-ttu-id="799b8-114">无法为 `ppProcs` 分配足够的内存。</span><span class="sxs-lookup"><span data-stu-id="799b8-114">Unable to allocate enough memory for `ppProcs`.</span></span>  
  
 <span data-ttu-id="799b8-115">E_FAIL（或其他 E_ 返回代码）</span><span class="sxs-lookup"><span data-stu-id="799b8-115">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="799b8-116">其他故障。</span><span class="sxs-lookup"><span data-stu-id="799b8-116">Other failures.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="799b8-117">备注</span><span class="sxs-lookup"><span data-stu-id="799b8-117">Remarks</span></span>  

 <span data-ttu-id="799b8-118">若要释放此方法分配的内存，请调用 [ICoreClrDebugTarget：： FreeMemory](icoreclrdebugtarget-freememory-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="799b8-118">To free the memory that was allocated by this method, call the [ICoreClrDebugTarget::FreeMemory](icoreclrdebugtarget-freememory-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="799b8-119">要求</span><span class="sxs-lookup"><span data-stu-id="799b8-119">Requirements</span></span>  

 <span data-ttu-id="799b8-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="799b8-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="799b8-121">**标头：** CoreClrRemoteDebuggingInterfaces</span><span class="sxs-lookup"><span data-stu-id="799b8-121">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="799b8-122">**库：** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="799b8-122">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="799b8-123">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="799b8-123">**.NET Framework Versions:** 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="799b8-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="799b8-124">See also</span></span>

- [<span data-ttu-id="799b8-125">ICoreClrDebugTarget 接口</span><span class="sxs-lookup"><span data-stu-id="799b8-125">ICoreClrDebugTarget Interface</span></span>](icoreclrdebugtarget-interface.md)
