---
description: 了解详细信息： ICorProfilerInfo2：： GetStaticFieldInfo 方法
title: ICorProfilerInfo2::GetStaticFieldInfo 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetStaticFieldInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetStaticFieldInfo
helpviewer_keywords:
- ICorProfilerInfo2::GetStaticFieldInfo method [.NET Framework profiling]
- GetStaticFieldInfo method [.NET Framework profiling]
ms.assetid: fc663e76-e23f-49a8-bdd5-52cdf1a3b2b3
topic_type:
- apiref
ms.openlocfilehash: 1acde9d5ad1a35b11cb036bced99c1909f0b6b04
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716349"
---
# <a name="icorprofilerinfo2getstaticfieldinfo-method"></a><span data-ttu-id="d25b5-103">ICorProfilerInfo2::GetStaticFieldInfo 方法</span><span class="sxs-lookup"><span data-stu-id="d25b5-103">ICorProfilerInfo2::GetStaticFieldInfo Method</span></span>

<span data-ttu-id="d25b5-104">获取一个值，该值指示应用于指定字段的静态类型。</span><span class="sxs-lookup"><span data-stu-id="d25b5-104">Gets a value that indicates the kind of static that applies to the specified field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d25b5-105">语法</span><span class="sxs-lookup"><span data-stu-id="d25b5-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStaticFieldInfo (  
    [in] ClassID               classId,  
    [in] mdFieldDef            fieldToken,  
    [out] COR_PRF_STATIC_TYPE  *pFieldInfo);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d25b5-106">参数</span><span class="sxs-lookup"><span data-stu-id="d25b5-106">Parameters</span></span>  

 `classId`  
 <span data-ttu-id="d25b5-107">中在其中定义静态字段的类的 ID。</span><span class="sxs-lookup"><span data-stu-id="d25b5-107">[in] The ID of the class in which the static field is defined.</span></span>  
  
 `fieldToken`  
 <span data-ttu-id="d25b5-108">中静态字段的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="d25b5-108">[in] The metadata token for the static field.</span></span>  
  
 `pFieldInfo`  
 <span data-ttu-id="d25b5-109">弄一个指针，指向 [COR_PRF_STATIC_TYPE](cor-prf-static-type-enumeration.md) 枚举的值，该值指示指定字段是否为静态的，如果为，则为应用于该字段的静态类型。</span><span class="sxs-lookup"><span data-stu-id="d25b5-109">[out] A pointer to a value of the [COR_PRF_STATIC_TYPE](cor-prf-static-type-enumeration.md) enumeration that indicates whether the specified field is static, and if so, the kind of static that applies to the field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d25b5-110">备注</span><span class="sxs-lookup"><span data-stu-id="d25b5-110">Remarks</span></span>  

 <span data-ttu-id="d25b5-111">此信息可用于确定要调用哪个函数以获取静态字段的地址。</span><span class="sxs-lookup"><span data-stu-id="d25b5-111">This information can be used to determine which function to call to get the address of the static field.</span></span>  
  
 <span data-ttu-id="d25b5-112">探查器代码仍应检查静态字段的元数据，以确保它实际具有地址。</span><span class="sxs-lookup"><span data-stu-id="d25b5-112">The profiler code should still check the metadata for a static field to ensure that it actually has an address.</span></span> <span data-ttu-id="d25b5-113">静态文本 (也就是说，常量) 只存在于元数据中，并且没有地址。</span><span class="sxs-lookup"><span data-stu-id="d25b5-113">Static literals (that is, constants) exist only in the metadata and do not have an address.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d25b5-114">要求</span><span class="sxs-lookup"><span data-stu-id="d25b5-114">Requirements</span></span>  

 <span data-ttu-id="d25b5-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d25b5-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d25b5-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d25b5-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d25b5-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d25b5-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d25b5-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d25b5-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d25b5-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="d25b5-119">See also</span></span>

- [<span data-ttu-id="d25b5-120">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="d25b5-120">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="d25b5-121">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="d25b5-121">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
