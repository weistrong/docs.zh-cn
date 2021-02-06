---
description: 了解详细信息： ICorProfilerInfo3：： GetAppDomainsContainingModule 方法
title: ICorProfilerInfo3::GetAppDomainsContainingModule 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.GetAppDomainsContainingModule Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::GetAppDomainsContainingModule
helpviewer_keywords:
- GetAppDomainsContainingModule method [.NET Framework profiling]
- ICorProfilerInfo3::GetAppDomainsContainingModule method [.NET Framework profiling]
ms.assetid: 603b3881-ea94-4dca-95cd-91eebac873a0
topic_type:
- apiref
ms.openlocfilehash: 0f0fea5b01b80b110d7ab041574dc195162cb508
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646824"
---
# <a name="icorprofilerinfo3getappdomainscontainingmodule-method"></a><span data-ttu-id="1c485-103">ICorProfilerInfo3::GetAppDomainsContainingModule 方法</span><span class="sxs-lookup"><span data-stu-id="1c485-103">ICorProfilerInfo3::GetAppDomainsContainingModule Method</span></span>

<span data-ttu-id="1c485-104">获取其中已加载给定模块的应用程序域的标识符。</span><span class="sxs-lookup"><span data-stu-id="1c485-104">Gets the identifiers of the application domains in which the given module has been loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1c485-105">语法</span><span class="sxs-lookup"><span data-stu-id="1c485-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAppDomainsContainingModule(  
            [in] ModuleID moduleId,  
            [in] ULONG32 cAppDomainIds,  
            [out] ULONG32 *pcAppDomainIds,  
            [out, size_is(cAppDomainIds), length_is(*pcAppDomainIds)]  
                    AppDomainID appDomainIds[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1c485-106">参数</span><span class="sxs-lookup"><span data-stu-id="1c485-106">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="1c485-107">[in] 已加载模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="1c485-107">[in] The ID of the loaded module.</span></span>  
  
 `cAppDomainIds`  
 <span data-ttu-id="1c485-108">[in] `appDomainIds` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="1c485-108">[in] The size of the `appDomainIds` array.</span></span>  
  
 `pcAppDomainIds`  
 <span data-ttu-id="1c485-109">[out] 指向所返回元素总数的指针。</span><span class="sxs-lookup"><span data-stu-id="1c485-109">[out] A pointer to the total number of returned elements.</span></span>  
  
 `appDomainIds`  
 <span data-ttu-id="1c485-110">[out] 应用程序域 ID 值的数组。</span><span class="sxs-lookup"><span data-stu-id="1c485-110">[out] An array of application domain ID values.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1c485-111">备注</span><span class="sxs-lookup"><span data-stu-id="1c485-111">Remarks</span></span>  

 <span data-ttu-id="1c485-112">此方法使用调用方分配的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="1c485-112">The method uses caller allocated buffers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1c485-113">要求</span><span class="sxs-lookup"><span data-stu-id="1c485-113">Requirements</span></span>  

 <span data-ttu-id="1c485-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1c485-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1c485-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="1c485-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="1c485-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1c485-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1c485-117">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1c485-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c485-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="1c485-118">See also</span></span>

- [<span data-ttu-id="1c485-119">ICorProfilerFunctionEnum 接口</span><span class="sxs-lookup"><span data-stu-id="1c485-119">ICorProfilerFunctionEnum Interface</span></span>](icorprofilerfunctionenum-interface.md)
- [<span data-ttu-id="1c485-120">ICorProfilerInfo3 接口</span><span class="sxs-lookup"><span data-stu-id="1c485-120">ICorProfilerInfo3 Interface</span></span>](icorprofilerinfo3-interface.md)
- [<span data-ttu-id="1c485-121">分析接口</span><span class="sxs-lookup"><span data-stu-id="1c485-121">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="1c485-122">分析</span><span class="sxs-lookup"><span data-stu-id="1c485-122">Profiling</span></span>](index.md)
