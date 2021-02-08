---
description: 了解详细信息： ICorProfilerInfo4：： GetObjectSize2 方法
title: ICorProfilerInfo4::GetObjectSize2 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.GetObjectSize2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::GetObjectSize2
helpviewer_keywords:
- GetObjectSize2 method, ICorProfilerInfo4 interface [.NET Framework profiling]
- ICorProfilerInfo4::GetObjectSize2 method [.NET Framework profiling]
ms.assetid: 4a3e43ed-3ee3-4395-ab14-f78b903be13e
topic_type:
- apiref
ms.openlocfilehash: 986c3d99501e21feec95dd3b6014f8d11d809704
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794518"
---
# <a name="icorprofilerinfo4getobjectsize2-method"></a><span data-ttu-id="92267-103">ICorProfilerInfo4::GetObjectSize2 方法</span><span class="sxs-lookup"><span data-stu-id="92267-103">ICorProfilerInfo4::GetObjectSize2 Method</span></span>

<span data-ttu-id="92267-104">返回指定的对象的大小。</span><span class="sxs-lookup"><span data-stu-id="92267-104">Returns the size of a specified object.</span></span> <span data-ttu-id="92267-105">通过报告大于可在中表示的对象的大小来替换 [ICorProfilerInfo：： GetObjectSize](icorprofilerinfo-getobjectsize-method.md) 方法 `ULONG` 。</span><span class="sxs-lookup"><span data-stu-id="92267-105">Replaces the [ICorProfilerInfo::GetObjectSize](icorprofilerinfo-getobjectsize-method.md) method by reporting sizes of objects that are larger than what can be expressed in a `ULONG`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="92267-106">语法</span><span class="sxs-lookup"><span data-stu-id="92267-106">Syntax</span></span>  
  
```cpp  
HRESULT GetObjectSize2(  
    [in]  ObjectID objectId,  
    [out] SIZE_T *pcSize);  
```  
  
## <a name="parameters"></a><span data-ttu-id="92267-107">参数</span><span class="sxs-lookup"><span data-stu-id="92267-107">Parameters</span></span>  

 `objectId`  
 <span data-ttu-id="92267-108">中对象的 ID。</span><span class="sxs-lookup"><span data-stu-id="92267-108">[in] The ID of the object.</span></span>  
  
 `pcSize`  
 <span data-ttu-id="92267-109">弄一个指针，指向对象的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="92267-109">[out] A pointer to the object's size, in bytes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="92267-110">备注</span><span class="sxs-lookup"><span data-stu-id="92267-110">Remarks</span></span>  

 <span data-ttu-id="92267-111">相同类型的不同对象通常具有相同的大小。</span><span class="sxs-lookup"><span data-stu-id="92267-111">Different objects of the same types often have the same size.</span></span> <span data-ttu-id="92267-112">但是，某些类型（例如数组或字符串）对于每个对象可能有不同的大小。</span><span class="sxs-lookup"><span data-stu-id="92267-112">However, some types, such as arrays or strings, may have a different size for each object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="92267-113">要求</span><span class="sxs-lookup"><span data-stu-id="92267-113">Requirements</span></span>  

 <span data-ttu-id="92267-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="92267-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="92267-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="92267-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="92267-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="92267-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="92267-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="92267-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="92267-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="92267-118">See also</span></span>

- [<span data-ttu-id="92267-119">ICorProfilerInfo4 接口</span><span class="sxs-lookup"><span data-stu-id="92267-119">ICorProfilerInfo4 Interface</span></span>](icorprofilerinfo4-interface.md)
