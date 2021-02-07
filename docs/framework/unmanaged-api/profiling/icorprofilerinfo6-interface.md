---
description: 了解详细信息： ICorProfilerInfo6 接口
title: ICorProfilerInfo6 接口
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo6
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: 6f2bb148-1e2b-4e45-a5a5-0ceddc40064b
ms.openlocfilehash: c093930b102ca99a8524e6d5d6129690f80a5353
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737150"
---
# <a name="icorprofilerinfo6-interface"></a><span data-ttu-id="a2913-103">ICorProfilerInfo6 接口</span><span class="sxs-lookup"><span data-stu-id="a2913-103">ICorProfilerInfo6 Interface</span></span>

<span data-ttu-id="a2913-104">[.NET Framework 4.6 及更高版本中支持]</span><span class="sxs-lookup"><span data-stu-id="a2913-104">[Supported in the .NET Framework 4.6 and later versions]</span></span>  
  
 <span data-ttu-id="a2913-105">[ICorProfilerInfo5](icorprofilerinfo5-interface.md)的子类，为在给定的 NGen 模块中定义并内联给定方法的所有方法提供了一个枚举器。</span><span class="sxs-lookup"><span data-stu-id="a2913-105">A subclass of [ICorProfilerInfo5](icorprofilerinfo5-interface.md) that provides an enumerator for all methods that are defined in a given NGen module and inline a given method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a2913-106">方法</span><span class="sxs-lookup"><span data-stu-id="a2913-106">Methods</span></span>  
  
|<span data-ttu-id="a2913-107">方法</span><span class="sxs-lookup"><span data-stu-id="a2913-107">Method</span></span>|<span data-ttu-id="a2913-108">说明</span><span class="sxs-lookup"><span data-stu-id="a2913-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a2913-109">ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod 方法</span><span class="sxs-lookup"><span data-stu-id="a2913-109">ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod Method</span></span>](icorprofilerinfo6-enumngenmodulemethodsinliningthismethod-method.md)|<span data-ttu-id="a2913-110">返回属于给定的 NGen 模块并在给定方法的主体中内联的所有方法的枚举器。</span><span class="sxs-lookup"><span data-stu-id="a2913-110">Returns an enumerator for all methods that belong to a given NGen module and that are inlined in the body of a given method.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a2913-111">要求</span><span class="sxs-lookup"><span data-stu-id="a2913-111">Requirements</span></span>  

 <span data-ttu-id="a2913-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a2913-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a2913-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a2913-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a2913-114">**.NET Framework 版本：**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a2913-114">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2913-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="a2913-115">See also</span></span>

- [<span data-ttu-id="a2913-116">分析接口</span><span class="sxs-lookup"><span data-stu-id="a2913-116">Profiling Interfaces</span></span>](profiling-interfaces.md)
