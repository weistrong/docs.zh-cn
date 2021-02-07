---
description: 了解详细信息： ICorProfilerInfo：： GetThreadContext 方法
title: ICorProfilerInfo::GetThreadContext 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetThreadContext
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetThreadContext
helpviewer_keywords:
- ICorProfilerInfo::GetThreadContext method [.NET Framework profiling]
- GetThreadContext method, ICorProfilerInfo interface [.NET Framework profiling]
ms.assetid: 79446216-4b8b-484c-8fe3-e87dbf9df2fd
topic_type:
- apiref
ms.openlocfilehash: b2970da90250819cc68eee55b70188d4830113a6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687267"
---
# <a name="icorprofilerinfogetthreadcontext-method"></a><span data-ttu-id="ab641-103">ICorProfilerInfo::GetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="ab641-103">ICorProfilerInfo::GetThreadContext Method</span></span>

<span data-ttu-id="ab641-104">获取当前与指定线程关联的上下文标识。</span><span class="sxs-lookup"><span data-stu-id="ab641-104">Gets the context identity currently associated with the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab641-105">语法</span><span class="sxs-lookup"><span data-stu-id="ab641-105">Syntax</span></span>  
  
```cpp  
HRESULT GetThreadContext(  
    [in]  ThreadID  threadId,  
    [out] ContextID *pContextId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ab641-106">参数</span><span class="sxs-lookup"><span data-stu-id="ab641-106">Parameters</span></span>  

 `threadId`  
 <span data-ttu-id="ab641-107">中线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="ab641-107">[in] The ID of the thread.</span></span>  
  
 `pContextId`  
 <span data-ttu-id="ab641-108">弄指向当前与指定线程关联的上下文 ID 的指针。</span><span class="sxs-lookup"><span data-stu-id="ab641-108">[out] A pointer to the context ID currently associated with the specified thread.</span></span> <span data-ttu-id="ab641-109">如果该线程当前没有关联的上下文，则此函数将返回 CORPROF_E_DATAINCOMPLETE。</span><span class="sxs-lookup"><span data-stu-id="ab641-109">If the thread has no context currently associated with it, this function will return CORPROF_E_DATAINCOMPLETE.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ab641-110">要求</span><span class="sxs-lookup"><span data-stu-id="ab641-110">Requirements</span></span>  

 <span data-ttu-id="ab641-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ab641-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab641-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ab641-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ab641-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ab641-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ab641-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ab641-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab641-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="ab641-115">See also</span></span>

- [<span data-ttu-id="ab641-116">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="ab641-116">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
