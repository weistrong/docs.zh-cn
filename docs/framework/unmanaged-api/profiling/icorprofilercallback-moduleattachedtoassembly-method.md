---
description: 了解详细信息： ICorProfilerCallback：： ModuleAttachedToAssembly 方法
title: ICorProfilerCallback::ModuleAttachedToAssembly 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleAttachedToAssembly
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleAttachedToAssembly
helpviewer_keywords:
- ICorProfilerCallback::ModuleAttachedToAssembly method [.NET Framework profiling]
- ModuleAttachedToAssembly method [.NET Framework profiling]
ms.assetid: b595798a-5d40-4cac-ab4f-911c61d2c5d2
topic_type:
- apiref
ms.openlocfilehash: cc6a83188a8bdc4826232aa6ff6e416cbb8ae893
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99705561"
---
# <a name="icorprofilercallbackmoduleattachedtoassembly-method"></a><span data-ttu-id="f37dd-103">ICorProfilerCallback::ModuleAttachedToAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="f37dd-103">ICorProfilerCallback::ModuleAttachedToAssembly Method</span></span>

<span data-ttu-id="f37dd-104">通知探查器模块正在附加到其父程序集。</span><span class="sxs-lookup"><span data-stu-id="f37dd-104">Notifies the profiler that a module is being attached to its parent assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f37dd-105">语法</span><span class="sxs-lookup"><span data-stu-id="f37dd-105">Syntax</span></span>  
  
```cpp  
HRESULT ModuleAttachedToAssembly(  
    [in] ModuleID   moduleId,  
    [in] AssemblyID AssemblyId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f37dd-106">参数</span><span class="sxs-lookup"><span data-stu-id="f37dd-106">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="f37dd-107">中要附加的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="f37dd-107">[in] The ID of the module that is being attached.</span></span>  
  
 `AssemblyId`  
 <span data-ttu-id="f37dd-108">中模块附加到的父程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="f37dd-108">[in] The ID of the parent assembly to which the module is attached.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f37dd-109">备注</span><span class="sxs-lookup"><span data-stu-id="f37dd-109">Remarks</span></span>  

 <span data-ttu-id="f37dd-110">可以通过导入地址表 (IAT) 、通过调用 `LoadLibrary` 或元数据引用来加载模块。</span><span class="sxs-lookup"><span data-stu-id="f37dd-110">A module can be loaded through an import address table (IAT), through a call to `LoadLibrary`, or through a metadata reference.</span></span> <span data-ttu-id="f37dd-111">因此，公共语言运行时 (CLR) 加载程序具有多个用于确定模块所在程序集的代码路径。</span><span class="sxs-lookup"><span data-stu-id="f37dd-111">As a result, the common language runtime (CLR) loader has multiple code paths for determining the assembly in which a module lives.</span></span> <span data-ttu-id="f37dd-112">因此，在调用 [ICorProfilerCallback：： ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) 后，模块并不知道它所在的程序集，因此无法获取父程序集 ID。</span><span class="sxs-lookup"><span data-stu-id="f37dd-112">Therefore, it is possible that after [ICorProfilerCallback::ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) is called, the module does not know what assembly it is in and getting the parent assembly ID is not possible.</span></span> <span data-ttu-id="f37dd-113">`ModuleAttachedToAssembly`当模块附加到其父程序集并且可以获得其父程序集 ID 时，将调用方法。</span><span class="sxs-lookup"><span data-stu-id="f37dd-113">The `ModuleAttachedToAssembly` method is called when the module is attached to its parent assembly and its parent assembly ID can be obtained.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f37dd-114">要求</span><span class="sxs-lookup"><span data-stu-id="f37dd-114">Requirements</span></span>  

 <span data-ttu-id="f37dd-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f37dd-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f37dd-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="f37dd-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="f37dd-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f37dd-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f37dd-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f37dd-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f37dd-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="f37dd-119">See also</span></span>

- [<span data-ttu-id="f37dd-120">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="f37dd-120">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
