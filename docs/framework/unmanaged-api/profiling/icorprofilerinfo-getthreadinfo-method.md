---
description: 了解详细信息： ICorProfilerInfo：： GetThreadInfo 方法
title: ICorProfilerInfo::GetThreadInfo 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetThreadInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetThreadInfo
helpviewer_keywords:
- ICorProfilerInfo::GetThreadInfo method [.NET Framework profiling]
- GetThreadInfo method [.NET Framework profiling]
ms.assetid: fc994fef-65c9-432a-84cb-66c8141147e7
topic_type:
- apiref
ms.openlocfilehash: 5514b1c4860067a07bf922e9d9a8bfab8c05e218
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760545"
---
# <a name="icorprofilerinfogetthreadinfo-method"></a><span data-ttu-id="03ce0-103">ICorProfilerInfo::GetThreadInfo 方法</span><span class="sxs-lookup"><span data-stu-id="03ce0-103">ICorProfilerInfo::GetThreadInfo Method</span></span>

<span data-ttu-id="03ce0-104">获取指定线程的当前 Win32 线程标识。</span><span class="sxs-lookup"><span data-stu-id="03ce0-104">Gets the current Win32 thread identity for the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="03ce0-105">语法</span><span class="sxs-lookup"><span data-stu-id="03ce0-105">Syntax</span></span>  
  
```cpp  
HRESULT GetThreadInfo(  
    [in]  ThreadID threadId,  
    [out] DWORD    *pdwWin32ThreadId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="03ce0-106">参数</span><span class="sxs-lookup"><span data-stu-id="03ce0-106">Parameters</span></span>  

 `threadId`  
 <span data-ttu-id="03ce0-107">中要获取其当前 Win32 ID 的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="03ce0-107">[in] The ID of the thread for which to get the current Win32 ID.</span></span>  
  
 `pdwWin32ThreadId`  
 <span data-ttu-id="03ce0-108">弄指向指定线程的当前 Win32 线程 ID 的指针。</span><span class="sxs-lookup"><span data-stu-id="03ce0-108">[out] A pointer to the specified thread's current Win32 thread ID.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="03ce0-109">要求</span><span class="sxs-lookup"><span data-stu-id="03ce0-109">Requirements</span></span>  

 <span data-ttu-id="03ce0-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="03ce0-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="03ce0-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="03ce0-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="03ce0-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="03ce0-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="03ce0-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="03ce0-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03ce0-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="03ce0-114">See also</span></span>

- [<span data-ttu-id="03ce0-115">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="03ce0-115">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
