---
description: 了解详细信息： ICorProfilerInfo2：： GetThreadAppDomain 方法
title: ICorProfilerInfo2::GetThreadAppDomain 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetThreadAppDomain
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetThreadAppDomain
helpviewer_keywords:
- ICorProfilerInfo2::GetThreadAppDomain method [.NET Framework profiling]
- GetThreadAppDomain method [.NET Framework profiling]
ms.assetid: 4a11b264-8540-4732-aa35-bc2d95b95b8e
topic_type:
- apiref
ms.openlocfilehash: b480388254a6ee84db9f6c3e8d44b7358246502a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647053"
---
# <a name="icorprofilerinfo2getthreadappdomain-method"></a><span data-ttu-id="53c36-103">ICorProfilerInfo2::GetThreadAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="53c36-103">ICorProfilerInfo2::GetThreadAppDomain Method</span></span>

<span data-ttu-id="53c36-104">获取指定线程当前正在执行代码的应用程序域的 ID。</span><span class="sxs-lookup"><span data-stu-id="53c36-104">Gets the ID of the application domain in which the specified thread is currently executing code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53c36-105">语法</span><span class="sxs-lookup"><span data-stu-id="53c36-105">Syntax</span></span>  
  
```cpp  
HRESULT GetThreadAppDomain(  
    [in]  ThreadID threadId,  
    [out] AppDomainID *pAppDomainId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="53c36-106">参数</span><span class="sxs-lookup"><span data-stu-id="53c36-106">Parameters</span></span>  

 `threadId`  
 <span data-ttu-id="53c36-107">中指定线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="53c36-107">[in] The ID specifying the thread.</span></span>  
  
 `pAppDomainId`  
 <span data-ttu-id="53c36-108">弄指向应用程序域的 ID 的指针。</span><span class="sxs-lookup"><span data-stu-id="53c36-108">[out] A pointer to the ID of the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="53c36-109">要求</span><span class="sxs-lookup"><span data-stu-id="53c36-109">Requirements</span></span>  

 <span data-ttu-id="53c36-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="53c36-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="53c36-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="53c36-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="53c36-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="53c36-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="53c36-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="53c36-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53c36-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="53c36-114">See also</span></span>

- [<span data-ttu-id="53c36-115">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="53c36-115">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="53c36-116">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="53c36-116">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
