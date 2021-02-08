---
description: 了解详细信息： ICorProfilerModuleEnum：： GetCount 方法
title: ICorProfilerModuleEnum::GetCount 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerModuleEnum.GetCount Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerModuleEnum::GetCount
helpviewer_keywords:
- ICorProfilerModuleEnum::GetCount method [.NET Framework profiling]
- GetCount method, ICorProfilerModuleEnum interface [.NET Framework profiling]
ms.assetid: f0a4a5e0-4689-474b-b0f4-37ca0639c918
topic_type:
- apiref
ms.openlocfilehash: efdd812795002c25aaeb7634e7a4f4e4287553e8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781384"
---
# <a name="icorprofilermoduleenumgetcount-method"></a><span data-ttu-id="e7281-103">ICorProfilerModuleEnum::GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="e7281-103">ICorProfilerModuleEnum::GetCount Method</span></span>

<span data-ttu-id="e7281-104">获取已加载到应用程序的托管模块数。</span><span class="sxs-lookup"><span data-stu-id="e7281-104">Gets the number of managed modules that were loaded into the application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e7281-105">语法</span><span class="sxs-lookup"><span data-stu-id="e7281-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCount([out] ULONG * pcelt);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e7281-106">参数</span><span class="sxs-lookup"><span data-stu-id="e7281-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="e7281-107">弄集合中的运行时模块数。</span><span class="sxs-lookup"><span data-stu-id="e7281-107">[out] The number of runtime modules in the collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e7281-108">要求</span><span class="sxs-lookup"><span data-stu-id="e7281-108">Requirements</span></span>  

 <span data-ttu-id="e7281-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e7281-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7281-110">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e7281-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e7281-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e7281-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e7281-112">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7281-112">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7281-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="e7281-113">See also</span></span>

- [<span data-ttu-id="e7281-114">ICorProfilerModuleEnum 接口</span><span class="sxs-lookup"><span data-stu-id="e7281-114">ICorProfilerModuleEnum Interface</span></span>](icorprofilermoduleenum-interface.md)
- [<span data-ttu-id="e7281-115">分析接口</span><span class="sxs-lookup"><span data-stu-id="e7281-115">Profiling Interfaces</span></span>](profiling-interfaces.md)
