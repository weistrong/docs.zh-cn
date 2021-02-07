---
description: 了解详细信息： ICorProfilerModuleEnum：： Clone 方法
title: ICorProfilerModuleEnum::Clone 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerModuleEnum.Clone Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerModuleEnum::Clone
helpviewer_keywords:
- Clone method, ICorProfilerModuleEnum interface [.NET Framework profiling]
- ICorProfilerModuleEnum::Clone method [.NET Framework profiling]
ms.assetid: 7dec7e36-8d88-416d-b437-abf98b76c1df
topic_type:
- apiref
ms.openlocfilehash: 0d2a235def6d3b16d661e51979742426ebe1942f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736929"
---
# <a name="icorprofilermoduleenumclone-method"></a><span data-ttu-id="39d31-103">ICorProfilerModuleEnum::Clone 方法</span><span class="sxs-lookup"><span data-stu-id="39d31-103">ICorProfilerModuleEnum::Clone Method</span></span>

<span data-ttu-id="39d31-104">获取一个接口指针，该指针指向此 [ICorProfilerModuleEnum](icorprofilermoduleenum-interface.md) 接口的副本。</span><span class="sxs-lookup"><span data-stu-id="39d31-104">Gets an interface pointer to a copy of this [ICorProfilerModuleEnum](icorprofilermoduleenum-interface.md) interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39d31-105">语法</span><span class="sxs-lookup"><span data-stu-id="39d31-105">Syntax</span></span>  
  
```cpp  
HRESULT Clone([out] ICorProfilerObjectEnum **ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="39d31-106">参数</span><span class="sxs-lookup"><span data-stu-id="39d31-106">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="39d31-107">弄指向接口指针的指针，该指针指向此 [ICorProfilerModuleEnum](icorprofilermoduleenum-interface.md) 接口的副本。</span><span class="sxs-lookup"><span data-stu-id="39d31-107">[out] A pointer to the interface pointer that in turn points to the copy of this [ICorProfilerModuleEnum](icorprofilermoduleenum-interface.md) interface.</span></span> <span data-ttu-id="39d31-108">枚举器的副本与此枚举器分别维护自己的枚举状态。</span><span class="sxs-lookup"><span data-stu-id="39d31-108">The copy of the enumerator maintains its own enumeration state separately from this enumerator.</span></span> <span data-ttu-id="39d31-109">但是，副本的初始光标位置与此枚举器的当前游标位置相同。</span><span class="sxs-lookup"><span data-stu-id="39d31-109">However, the copy's initial cursor position is the same as this enumerator's current cursor position.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="39d31-110">要求</span><span class="sxs-lookup"><span data-stu-id="39d31-110">Requirements</span></span>  

 <span data-ttu-id="39d31-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="39d31-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="39d31-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="39d31-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="39d31-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="39d31-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="39d31-114">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="39d31-114">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39d31-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="39d31-115">See also</span></span>

- [<span data-ttu-id="39d31-116">ICorProfilerModuleEnum 接口</span><span class="sxs-lookup"><span data-stu-id="39d31-116">ICorProfilerModuleEnum Interface</span></span>](icorprofilermoduleenum-interface.md)
- [<span data-ttu-id="39d31-117">分析接口</span><span class="sxs-lookup"><span data-stu-id="39d31-117">Profiling Interfaces</span></span>](profiling-interfaces.md)
