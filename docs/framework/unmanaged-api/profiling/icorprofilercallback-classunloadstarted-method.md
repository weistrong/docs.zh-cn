---
description: 了解详细信息： ICorProfilerCallback：： ClassUnloadStarted 方法
title: ICorProfilerCallback::ClassUnloadStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ClassUnloadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ClassUnloadStarted
helpviewer_keywords:
- ClassUnloadStarted method [.NET Framework profiling]
- ICorProfilerCallback::ClassUnloadStarted method [.NET Framework profiling]
ms.assetid: bc93bead-f3a9-415c-b919-ddd3ca80facc
topic_type:
- apiref
ms.openlocfilehash: 3dae88d9cbe9ed2a2e234d02420a65c6a9ca003d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706365"
---
# <a name="icorprofilercallbackclassunloadstarted-method"></a><span data-ttu-id="7574a-103">ICorProfilerCallback::ClassUnloadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="7574a-103">ICorProfilerCallback::ClassUnloadStarted Method</span></span>

<span data-ttu-id="7574a-104">通知探查器正在卸载某个类。</span><span class="sxs-lookup"><span data-stu-id="7574a-104">Notifies the profiler that a class is being unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7574a-105">语法</span><span class="sxs-lookup"><span data-stu-id="7574a-105">Syntax</span></span>  
  
```cpp  
HRESULT ClassUnloadStarted(  
    [in] ClassID classId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7574a-106">参数</span><span class="sxs-lookup"><span data-stu-id="7574a-106">Parameters</span></span>

- `classId`

  <span data-ttu-id="7574a-107">\[in] 标识正在卸载的类。</span><span class="sxs-lookup"><span data-stu-id="7574a-107">\[in] Identifies the class that is being unloaded.</span></span>

## <a name="remarks"></a><span data-ttu-id="7574a-108">备注</span><span class="sxs-lookup"><span data-stu-id="7574a-108">Remarks</span></span>  

 <span data-ttu-id="7574a-109">在 `classId` 方法返回后，的值对信息请求无效 `ClassUnloadStarted` -这是探查器获取有关此类的信息的最后机会。</span><span class="sxs-lookup"><span data-stu-id="7574a-109">The value of `classId` is not valid for an information request after the `ClassUnloadStarted` method returns — this is the profiler's last chance to obtain information about this class.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7574a-110">要求</span><span class="sxs-lookup"><span data-stu-id="7574a-110">Requirements</span></span>  

 <span data-ttu-id="7574a-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7574a-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7574a-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7574a-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7574a-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7574a-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7574a-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7574a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7574a-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="7574a-115">See also</span></span>

- [<span data-ttu-id="7574a-116">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="7574a-116">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="7574a-117">ClassUnloadFinished 方法</span><span class="sxs-lookup"><span data-stu-id="7574a-117">ClassUnloadFinished Method</span></span>](icorprofilercallback-classunloadfinished-method.md)
