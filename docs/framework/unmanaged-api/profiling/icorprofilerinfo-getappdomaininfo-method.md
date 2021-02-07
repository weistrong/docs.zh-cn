---
description: 了解详细信息： ICorProfilerInfo：： GetAppDomainInfo 方法
title: ICorProfilerInfo::GetAppDomainInfo 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetAppDomainInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetAppDomainInfo
helpviewer_keywords:
- ICorProfilerInfo::GetAppDomainInfo method [.NET Framework profiling]
- GetAppDomainInfo method [.NET Framework profiling]
ms.assetid: a6bf5a04-e03e-44f0-917a-96f6a6d3cc96
topic_type:
- apiref
ms.openlocfilehash: 981577320bdf04a2bf119115f066811d3c11b68f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687278"
---
# <a name="icorprofilerinfogetappdomaininfo-method"></a><span data-ttu-id="70ab5-103">ICorProfilerInfo::GetAppDomainInfo 方法</span><span class="sxs-lookup"><span data-stu-id="70ab5-103">ICorProfilerInfo::GetAppDomainInfo Method</span></span>

<span data-ttu-id="70ab5-104">接受应用程序域 ID。</span><span class="sxs-lookup"><span data-stu-id="70ab5-104">Accepts an application domain ID.</span></span> <span data-ttu-id="70ab5-105">返回应用程序域名称和包含该域的进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="70ab5-105">Returns an application domain name and the ID of the process that contains it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70ab5-106">语法</span><span class="sxs-lookup"><span data-stu-id="70ab5-106">Syntax</span></span>  
  
```cpp  
HRESULT GetAppDomainInfo(  
    [in]  AppDomainID appDomainId,  
    [in]  ULONG       cchName,  
    [out] ULONG       *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
          WCHAR       szName[] ,  
    [out] ProcessID   *pProcessId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="70ab5-107">参数</span><span class="sxs-lookup"><span data-stu-id="70ab5-107">Parameters</span></span>  

 `appDomainId`  
 <span data-ttu-id="70ab5-108">[in] 应用程序域的 ID。</span><span class="sxs-lookup"><span data-stu-id="70ab5-108">[in] The ID of the application domain.</span></span>  
  
 `cchName`  
 <span data-ttu-id="70ab5-109">[in] `szName` 返回缓冲区的长度（以字符为单位）。</span><span class="sxs-lookup"><span data-stu-id="70ab5-109">[in] The length, in characters, of the `szName` return buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="70ab5-110">[out] 指向应用程序域名称的总字符长度的指针。</span><span class="sxs-lookup"><span data-stu-id="70ab5-110">[out] A pointer to the total character length of the application domain name.</span></span>  
  
 `szName`  
 <span data-ttu-id="70ab5-111">[out] 调用方提供的宽字符缓冲区。</span><span class="sxs-lookup"><span data-stu-id="70ab5-111">[out] A caller-provided wide character buffer.</span></span> <span data-ttu-id="70ab5-112">当方法返回时，`szName` 将包含整个或部分应用程序域名称。</span><span class="sxs-lookup"><span data-stu-id="70ab5-112">When the method returns, `szName` will contain the full or partial application domain name.</span></span>  
  
 `pProcessId`  
 <span data-ttu-id="70ab5-113">[out] 指向包含应用程序域的进程的 ID 的指针。</span><span class="sxs-lookup"><span data-stu-id="70ab5-113">[out] A pointer to the ID of the process that contains the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="70ab5-114">备注</span><span class="sxs-lookup"><span data-stu-id="70ab5-114">Remarks</span></span>  

 <span data-ttu-id="70ab5-115">此方法返回后，必须验证 `szName` 缓冲区是否足够大从而可包含应用程序域的完整名称。</span><span class="sxs-lookup"><span data-stu-id="70ab5-115">After this method returns, you must verify that the `szName` buffer was large enough to contain the full name of the application domain.</span></span> <span data-ttu-id="70ab5-116">为此，请比较 `pcchName` 指向的值和 `cchName` 参数的值。</span><span class="sxs-lookup"><span data-stu-id="70ab5-116">To do this, compare the value that `pcchName` points to with the value of the `cchName` parameter.</span></span> <span data-ttu-id="70ab5-117">如果 `pcchName` 指向的值大于 `cchName`，请分配更大的 `szName` 缓冲区，并用新的、更大的大小更新 `cchName`，然后再次调用 `GetAppDomainInfo`。</span><span class="sxs-lookup"><span data-stu-id="70ab5-117">If `pcchName` points to a value that is larger than `cchName`, allocate a larger `szName` buffer, update `cchName` with the new, larger size, and call `GetAppDomainInfo` again.</span></span>  
  
 <span data-ttu-id="70ab5-118">或者，可以先用长度为零的 `szName` 缓冲区调用 `GetAppDomainInfo` 以获取正确的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="70ab5-118">Alternatively, you can first call `GetAppDomainInfo` with a zero-length `szName` buffer to obtain the correct buffer size.</span></span> <span data-ttu-id="70ab5-119">然后，可将缓冲区大小设置为 `pcchName` 中返回的值，并再次调用 `GetAppDomainInfo`。</span><span class="sxs-lookup"><span data-stu-id="70ab5-119">You can then set the buffer size to the value returned in `pcchName` and call `GetAppDomainInfo` again.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="70ab5-120">要求</span><span class="sxs-lookup"><span data-stu-id="70ab5-120">Requirements</span></span>  

 <span data-ttu-id="70ab5-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="70ab5-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="70ab5-122">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="70ab5-122">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="70ab5-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="70ab5-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="70ab5-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="70ab5-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70ab5-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="70ab5-125">See also</span></span>

- [<span data-ttu-id="70ab5-126">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="70ab5-126">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="70ab5-127">分析接口</span><span class="sxs-lookup"><span data-stu-id="70ab5-127">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="70ab5-128">分析</span><span class="sxs-lookup"><span data-stu-id="70ab5-128">Profiling</span></span>](index.md)
