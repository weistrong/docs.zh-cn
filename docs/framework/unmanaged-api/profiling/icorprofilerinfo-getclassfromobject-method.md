---
description: 了解详细信息： ICorProfilerInfo：： GetClassFromObject 方法
title: ICorProfilerInfo::GetClassFromObject 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetClassFromObject
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetClassFromObject
helpviewer_keywords:
- GetClassFromObject method [.NET Framework profiling]
- ICorProfilerInfo::GetClassFromObject method [.NET Framework profiling]
ms.assetid: b97493fb-713e-49d5-a73e-5688b2ad0700
topic_type:
- apiref
ms.openlocfilehash: 1c0224137c839d167263eefb17e3ae0b3ac29ef3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647799"
---
# <a name="icorprofilerinfogetclassfromobject-method"></a><span data-ttu-id="eb3da-103">ICorProfilerInfo::GetClassFromObject 方法</span><span class="sxs-lookup"><span data-stu-id="eb3da-103">ICorProfilerInfo::GetClassFromObject Method</span></span>

<span data-ttu-id="eb3da-104">在 `ClassID` 给定对象的情况下，获取该对象的 `ObjectID` 。</span><span class="sxs-lookup"><span data-stu-id="eb3da-104">Gets the `ClassID` of an object, given its `ObjectID`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb3da-105">语法</span><span class="sxs-lookup"><span data-stu-id="eb3da-105">Syntax</span></span>  
  
```cpp  
HRESULT GetClassFromObject(  
    [in]  ObjectID objectId,  
    [out] ClassID *pClassId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eb3da-106">参数</span><span class="sxs-lookup"><span data-stu-id="eb3da-106">Parameters</span></span>  

 `objectId`  
 <span data-ttu-id="eb3da-107">中要获取的对象的 ID `ClassID` 。</span><span class="sxs-lookup"><span data-stu-id="eb3da-107">[in] The ID of the object for which to get the `ClassID`.</span></span>  
  
 `pClassId`  
 <span data-ttu-id="eb3da-108">弄指向返回的的指针 `ClassID` 。</span><span class="sxs-lookup"><span data-stu-id="eb3da-108">[out] A pointer to the returned `ClassID`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eb3da-109">备注</span><span class="sxs-lookup"><span data-stu-id="eb3da-109">Remarks</span></span>  

 <span data-ttu-id="eb3da-110">如果为 null `pClassId` ， `objectId` 则表示具有正在卸载的类型。</span><span class="sxs-lookup"><span data-stu-id="eb3da-110">A null `pClassId` indicates that `objectId` has a type that is unloading.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eb3da-111">要求</span><span class="sxs-lookup"><span data-stu-id="eb3da-111">Requirements</span></span>  

 <span data-ttu-id="eb3da-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="eb3da-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eb3da-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="eb3da-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="eb3da-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eb3da-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eb3da-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eb3da-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb3da-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="eb3da-116">See also</span></span>

- [<span data-ttu-id="eb3da-117">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="eb3da-117">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
