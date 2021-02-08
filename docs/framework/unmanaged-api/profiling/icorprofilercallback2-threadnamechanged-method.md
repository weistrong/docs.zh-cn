---
description: 了解详细信息： ICorProfilerCallback2：： ThreadNameChanged 方法
title: ICorProfilerCallback2::ThreadNameChanged 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.ThreadNameChanged
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::ThreadNameChanged
helpviewer_keywords:
- ThreadNameChanged method [.NET Framework profiling]
- ICorProfilerCallback2::ThreadNameChanged method [.NET Framework profiling]
ms.assetid: c8bbd76d-a9ff-44f2-87a6-be052819da36
topic_type:
- apiref
ms.openlocfilehash: 161247f9692d1307d063e244b200eb0d8f739e9a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799032"
---
# <a name="icorprofilercallback2threadnamechanged-method"></a><span data-ttu-id="df2b7-103">ICorProfilerCallback2::ThreadNameChanged 方法</span><span class="sxs-lookup"><span data-stu-id="df2b7-103">ICorProfilerCallback2::ThreadNameChanged Method</span></span>

<span data-ttu-id="df2b7-104">通知代码探查器线程的名称已更改。</span><span class="sxs-lookup"><span data-stu-id="df2b7-104">Notifies the code profiler that the name of a thread has changed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df2b7-105">语法</span><span class="sxs-lookup"><span data-stu-id="df2b7-105">Syntax</span></span>  
  
```cpp  
HRESULT ThreadNameChanged(  
    [in] ThreadID threadId,  
    [in] ULONG cchName,  
    [in] WCHAR name[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="df2b7-106">参数</span><span class="sxs-lookup"><span data-stu-id="df2b7-106">Parameters</span></span>  

 `threadId`  
 <span data-ttu-id="df2b7-107">中线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="df2b7-107">[in] The ID of the thread.</span></span>  
  
 `cchName`  
 <span data-ttu-id="df2b7-108">中线程的新名称的长度。</span><span class="sxs-lookup"><span data-stu-id="df2b7-108">[in] The length of the new name of the thread.</span></span>  
  
 `name`  
 <span data-ttu-id="df2b7-109">中线程的新名称。</span><span class="sxs-lookup"><span data-stu-id="df2b7-109">[in] The new name of the thread.</span></span> <span data-ttu-id="df2b7-110">名称不以 null 结尾。</span><span class="sxs-lookup"><span data-stu-id="df2b7-110">The name is not null-terminated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="df2b7-111">要求</span><span class="sxs-lookup"><span data-stu-id="df2b7-111">Requirements</span></span>  

 <span data-ttu-id="df2b7-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="df2b7-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="df2b7-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="df2b7-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="df2b7-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="df2b7-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="df2b7-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="df2b7-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df2b7-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="df2b7-116">See also</span></span>

- [<span data-ttu-id="df2b7-117">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="df2b7-117">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="df2b7-118">ICorProfilerCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="df2b7-118">ICorProfilerCallback2 Interface</span></span>](icorprofilercallback2-interface.md)
