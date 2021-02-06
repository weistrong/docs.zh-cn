---
description: 了解详细信息： ICorProfilerInfo3：： EnumModules 方法
title: ICorProfilerInfo3::EnumModules 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.EnumModules Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::EnumModules
helpviewer_keywords:
- ICorProfilerInfo3::EnumModules method [.NET Framework profiling]
- EnumModules method [.NET Framework profiling]
ms.assetid: 1bf00b42-69da-4019-91b3-bf88026e83fb
topic_type:
- apiref
ms.openlocfilehash: 9cdb76b77f78fa68eafa111e60b31b738173d658
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646850"
---
# <a name="icorprofilerinfo3enummodules-method"></a><span data-ttu-id="fd6a3-103">ICorProfilerInfo3::EnumModules 方法</span><span class="sxs-lookup"><span data-stu-id="fd6a3-103">ICorProfilerInfo3::EnumModules Method</span></span>

<span data-ttu-id="fd6a3-104">返回一个枚举器，此枚举器提供方法以按顺序循环访问加载到应用程序的托管模块集合。</span><span class="sxs-lookup"><span data-stu-id="fd6a3-104">Returns an enumerator that provides methods to sequentially iterate through a collection of managed modules that are loaded into the application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd6a3-105">语法</span><span class="sxs-lookup"><span data-stu-id="fd6a3-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumModules([out] ICorProfilerModuleEnum** ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fd6a3-106">参数</span><span class="sxs-lookup"><span data-stu-id="fd6a3-106">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="fd6a3-107">弄指向 [ICorProfilerModuleEnum](icorprofilermoduleenum-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="fd6a3-107">[out] A pointer to an [ICorProfilerModuleEnum](icorprofilermoduleenum-interface.md) interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fd6a3-108">备注</span><span class="sxs-lookup"><span data-stu-id="fd6a3-108">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd6a3-109">要求</span><span class="sxs-lookup"><span data-stu-id="fd6a3-109">Requirements</span></span>  

 <span data-ttu-id="fd6a3-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fd6a3-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fd6a3-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fd6a3-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fd6a3-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fd6a3-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fd6a3-113">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd6a3-113">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd6a3-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="fd6a3-114">See also</span></span>

- [<span data-ttu-id="fd6a3-115">ICorProfilerFunctionEnum 接口</span><span class="sxs-lookup"><span data-stu-id="fd6a3-115">ICorProfilerFunctionEnum Interface</span></span>](icorprofilerfunctionenum-interface.md)
- [<span data-ttu-id="fd6a3-116">ICorProfilerInfo3 接口</span><span class="sxs-lookup"><span data-stu-id="fd6a3-116">ICorProfilerInfo3 Interface</span></span>](icorprofilerinfo3-interface.md)
- [<span data-ttu-id="fd6a3-117">分析接口</span><span class="sxs-lookup"><span data-stu-id="fd6a3-117">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="fd6a3-118">分析</span><span class="sxs-lookup"><span data-stu-id="fd6a3-118">Profiling</span></span>](index.md)
