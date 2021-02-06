---
description: 了解详细信息： ICorProfilerInfo：： GetClassIDInfo 方法
title: ICorProfilerInfo::GetClassIDInfo 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetClassIDInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetClassIDInfo
helpviewer_keywords:
- GetClassIDInfo method [.NET Framework profiling]
- ICorProfilerInfo::GetClassIDInfo method [.NET Framework profiling]
ms.assetid: 9e93b99e-5aca-415c-8e37-7f33753b612d
topic_type:
- apiref
ms.openlocfilehash: 05937580bd8bd672da16875964548829d071f4bf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647708"
---
# <a name="icorprofilerinfogetclassidinfo-method"></a><span data-ttu-id="85afa-103">ICorProfilerInfo::GetClassIDInfo 方法</span><span class="sxs-lookup"><span data-stu-id="85afa-103">ICorProfilerInfo::GetClassIDInfo Method</span></span>

<span data-ttu-id="85afa-104">获取指定类的父模块和元数据标记。</span><span class="sxs-lookup"><span data-stu-id="85afa-104">Gets the parent module and the metadata token for the specified class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="85afa-105">语法</span><span class="sxs-lookup"><span data-stu-id="85afa-105">Syntax</span></span>  
  
```cpp  
HRESULT GetClassIDInfo(  
    [in]  ClassID   classId,  
    [out] ModuleID  *pModuleId,  
    [out] mdTypeDef *pTypeDefToken);  
```  
  
## <a name="parameters"></a><span data-ttu-id="85afa-106">参数</span><span class="sxs-lookup"><span data-stu-id="85afa-106">Parameters</span></span>  

 `classId`  
 <span data-ttu-id="85afa-107">中要获取其信息的类的 ID。</span><span class="sxs-lookup"><span data-stu-id="85afa-107">[in] The ID of the class for which to get the information.</span></span>  
  
 `pModuleId`  
 <span data-ttu-id="85afa-108">弄指向类的父模块的 ID 的指针。</span><span class="sxs-lookup"><span data-stu-id="85afa-108">[out] A pointer to the ID of the parent module of the class.</span></span>  
  
 `pTypeDefToken`  
 <span data-ttu-id="85afa-109">弄指向类的元数据标记的指针。</span><span class="sxs-lookup"><span data-stu-id="85afa-109">[out] A pointer to the metadata token for the class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="85afa-110">备注</span><span class="sxs-lookup"><span data-stu-id="85afa-110">Remarks</span></span>  

 <span data-ttu-id="85afa-111">探查器代码可调用 [ICorProfilerInfo：： GetModuleMetaData](icorprofilerinfo-getmodulemetadata-method.md) 以获取给定模块的元数据接口。</span><span class="sxs-lookup"><span data-stu-id="85afa-111">The profiler code can call [ICorProfilerInfo::GetModuleMetaData](icorprofilerinfo-getmodulemetadata-method.md) to obtain a metadata interface for a given module.</span></span> <span data-ttu-id="85afa-112">返回至 `pTypeDefToken` 所引用的位置的元数据标记可用于访问类的元数据。</span><span class="sxs-lookup"><span data-stu-id="85afa-112">The metadata token that is returned to the location referenced by `pTypeDefToken` can then be used to access the metadata for the class.</span></span>  
  
 <span data-ttu-id="85afa-113">若要获取有关泛型类型的详细信息，请使用 [ICorProfilerInfo2：： GetClassIDInfo2](icorprofilerinfo2-getclassidinfo2-method.md)。</span><span class="sxs-lookup"><span data-stu-id="85afa-113">To get more information for generic types, use [ICorProfilerInfo2::GetClassIDInfo2](icorprofilerinfo2-getclassidinfo2-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="85afa-114">要求</span><span class="sxs-lookup"><span data-stu-id="85afa-114">Requirements</span></span>  

 <span data-ttu-id="85afa-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="85afa-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="85afa-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="85afa-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="85afa-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="85afa-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="85afa-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="85afa-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="85afa-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="85afa-119">See also</span></span>

- [<span data-ttu-id="85afa-120">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="85afa-120">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
