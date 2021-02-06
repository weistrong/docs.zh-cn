---
description: 了解详细信息： ICorProfilerInfo：： GetModuleInfo 方法
title: ICorProfilerInfo::GetModuleInfo 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetModuleInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetModuleInfo
helpviewer_keywords:
- GetModuleInfo method [.NET Framework profiling]
- ICorProfilerInfo::GetModuleInfo method [.NET Framework profiling]
ms.assetid: 5a90d16f-7929-4987-8f83-a631becf564d
topic_type:
- apiref
ms.openlocfilehash: 003f40e6637490be23e8bf87a6bac8ab76bc50e5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647188"
---
# <a name="icorprofilerinfogetmoduleinfo-method"></a><span data-ttu-id="e1901-103">ICorProfilerInfo::GetModuleInfo 方法</span><span class="sxs-lookup"><span data-stu-id="e1901-103">ICorProfilerInfo::GetModuleInfo Method</span></span>

<span data-ttu-id="e1901-104">给定模块 ID 后，将返回模块的文件名和模块的父程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="e1901-104">Given a module ID, returns the file name of the module and the ID of the module's parent assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e1901-105">语法</span><span class="sxs-lookup"><span data-stu-id="e1901-105">Syntax</span></span>  
  
```cpp  
HRESULT GetModuleInfo(  
    [in]  ModuleID   moduleId,  
    [out] LPCBYTE    *ppBaseLoadAddress,  
    [in]  ULONG      cchName,  
    [out] ULONG      *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
          WCHAR      szName[] ,  
    [out] AssemblyID *pAssemblyId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e1901-106">参数</span><span class="sxs-lookup"><span data-stu-id="e1901-106">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="e1901-107">[in] 将为其检索信息的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="e1901-107">[in] The ID of the module for which information will be retrieved.</span></span>  
  
 `ppBaseLoadAddress`  
 <span data-ttu-id="e1901-108">[out] 加载模块的基址。</span><span class="sxs-lookup"><span data-stu-id="e1901-108">[out] The base address at which the module is loaded.</span></span>  
  
 `cchName`  
 <span data-ttu-id="e1901-109">[in] `szName` 返回缓冲区的长度（以字符为单位）。</span><span class="sxs-lookup"><span data-stu-id="e1901-109">[in] The length, in characters, of the `szName` return buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="e1901-110">[out] 指向返回的模块文件名总字符长度的指针。</span><span class="sxs-lookup"><span data-stu-id="e1901-110">[out] A pointer to the total character length of the module's file name that is returned.</span></span>  
  
 `szName`  
 <span data-ttu-id="e1901-111">[out] 调用方提供的宽字符缓冲区。</span><span class="sxs-lookup"><span data-stu-id="e1901-111">[out] A caller-provided wide character buffer.</span></span> <span data-ttu-id="e1901-112">方法返回后，此缓冲区包含模块的文件名。</span><span class="sxs-lookup"><span data-stu-id="e1901-112">When the method returns, this buffer contains the file name of the module.</span></span>  
  
 `pAssemblyId`  
 <span data-ttu-id="e1901-113">[out] 指向模块的父程序集的 ID 的指针。</span><span class="sxs-lookup"><span data-stu-id="e1901-113">[out] A pointer to the ID of the module's parent assembly.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e1901-114">备注</span><span class="sxs-lookup"><span data-stu-id="e1901-114">Remarks</span></span>  

 <span data-ttu-id="e1901-115">对于动态模块，`szName` 参数是空字符串，并且基址是 0（零）。</span><span class="sxs-lookup"><span data-stu-id="e1901-115">For dynamic modules, the `szName` parameter is an empty string, and the base address is 0 (zero).</span></span>  
  
 <span data-ttu-id="e1901-116">尽管在 `GetModuleInfo` 模块的 ID 存在后可以调用方法，但在探查器接收到 [ICorProfilerCallback：： ModuleAttachedToAssembly](icorprofilercallback-moduleattachedtoassembly-method.md) 回调之前，父程序集的 ID 将不可用。</span><span class="sxs-lookup"><span data-stu-id="e1901-116">Although the `GetModuleInfo` method may be called as soon as the module's ID exists, the ID of the parent assembly will not be available until the profiler receives the [ICorProfilerCallback::ModuleAttachedToAssembly](icorprofilercallback-moduleattachedtoassembly-method.md) callback.</span></span>  
  
 <span data-ttu-id="e1901-117">返回 `GetModuleInfo` 后，必须验证 `szName` 缓冲区的大小是否足够包含模块的完整文件名。</span><span class="sxs-lookup"><span data-stu-id="e1901-117">When `GetModuleInfo` returns, you must verify that the `szName` buffer was large enough to contain the full file name of the module.</span></span> <span data-ttu-id="e1901-118">为此，请比较 `pcchName` 指向的值和 `cchName` 参数的值。</span><span class="sxs-lookup"><span data-stu-id="e1901-118">To do this, compare the value that `pcchName` points to with the value of the `cchName` parameter.</span></span> <span data-ttu-id="e1901-119">如果 `pcchName` 指向的值大于 `cchName`，请分配更大的 `szName` 缓冲区，并用新的、更大的大小更新 `cchName`，然后再次调用 `GetModuleInfo`。</span><span class="sxs-lookup"><span data-stu-id="e1901-119">If `pcchName` points to a value that is larger than `cchName`, allocate a larger `szName` buffer, update `cchName` with the new, larger size, and call `GetModuleInfo` again.</span></span>  
  
 <span data-ttu-id="e1901-120">或者，可以先用长度为零的 `szName` 缓冲区调用 `GetModuleInfo` 以获取正确的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="e1901-120">Alternatively, you can first call `GetModuleInfo` with a zero-length `szName` buffer to obtain the correct buffer size.</span></span> <span data-ttu-id="e1901-121">然后，可将缓冲区大小设置为 `pcchName` 中返回的值，并再次调用 `GetModuleInfo`。</span><span class="sxs-lookup"><span data-stu-id="e1901-121">You can then set the buffer size to the value returned in `pcchName` and call `GetModuleInfo` again.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e1901-122">要求</span><span class="sxs-lookup"><span data-stu-id="e1901-122">Requirements</span></span>  

 <span data-ttu-id="e1901-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e1901-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e1901-124">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e1901-124">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e1901-125">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e1901-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e1901-126">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e1901-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1901-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="e1901-127">See also</span></span>

- [<span data-ttu-id="e1901-128">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="e1901-128">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="e1901-129">分析接口</span><span class="sxs-lookup"><span data-stu-id="e1901-129">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="e1901-130">分析</span><span class="sxs-lookup"><span data-stu-id="e1901-130">Profiling</span></span>](index.md)
- [<span data-ttu-id="e1901-131">GetModuleInfo2 方法</span><span class="sxs-lookup"><span data-stu-id="e1901-131">GetModuleInfo2 Method</span></span>](icorprofilerinfo3-getmoduleinfo2-method.md)
