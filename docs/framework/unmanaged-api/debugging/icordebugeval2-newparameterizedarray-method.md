---
description: 了解详细信息： ICorDebugEval2：： NewParameterizedArray 方法
title: ICorDebugEval2::NewParameterizedArray 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval2.NewParameterizedArray
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval2::NewParameterizedArray
helpviewer_keywords:
- ICorDebugEval2::NewParameterizedArray method [.NET Framework debugging]
- NewParameterizedArray method [.NET Framework debugging]
ms.assetid: 45efb8ba-c4de-4109-945f-e734d376b43c
topic_type:
- apiref
ms.openlocfilehash: 0ce8582328013ad02357361f05efb55ade8780e5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693741"
---
# <a name="icordebugeval2newparameterizedarray-method"></a><span data-ttu-id="63d91-103">ICorDebugEval2::NewParameterizedArray 方法</span><span class="sxs-lookup"><span data-stu-id="63d91-103">ICorDebugEval2::NewParameterizedArray Method</span></span>

<span data-ttu-id="63d91-104">分配指定元素类型和维度的新数组。</span><span class="sxs-lookup"><span data-stu-id="63d91-104">Allocates a new array of the specified element type and dimensions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63d91-105">语法</span><span class="sxs-lookup"><span data-stu-id="63d91-105">Syntax</span></span>  
  
```cpp  
HRESULT NewParameterizedArray(  
    [in] ICorDebugType          *pElementType,  
    [in] ULONG32                rank,  
    [in, size_is(rank)] ULONG32 dims[],  
    [in, size_is(rank)] ULONG32 lowBounds[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="63d91-106">参数</span><span class="sxs-lookup"><span data-stu-id="63d91-106">Parameters</span></span>  

 `pElementType`  
 <span data-ttu-id="63d91-107">中指向 ICorDebugType 对象的指针，该对象表示存储在数组中的元素的类型。</span><span class="sxs-lookup"><span data-stu-id="63d91-107">[in] A pointer to an ICorDebugType object that represents the type of element stored in the array.</span></span>  
  
 `rank`  
 <span data-ttu-id="63d91-108">中数组的维数。</span><span class="sxs-lookup"><span data-stu-id="63d91-108">[in] The number of dimensions of the array.</span></span> <span data-ttu-id="63d91-109">在 .NET Framework 版本2.0 中，此值必须为1。</span><span class="sxs-lookup"><span data-stu-id="63d91-109">In the .NET Framework version 2.0, this value must be 1.</span></span>  
  
 `dims`  
 <span data-ttu-id="63d91-110">中数组每个维度的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="63d91-110">[in] The size, in bytes, of each dimension of the array.</span></span>  
  
 `lowBounds`  
 <span data-ttu-id="63d91-111">[in] 可选。</span><span class="sxs-lookup"><span data-stu-id="63d91-111">[in] Optional.</span></span> <span data-ttu-id="63d91-112">数组的每个维度的下限。</span><span class="sxs-lookup"><span data-stu-id="63d91-112">The lower bound of each dimension of the array.</span></span> <span data-ttu-id="63d91-113">如果省略此值，则假定每个维度的下限为零。</span><span class="sxs-lookup"><span data-stu-id="63d91-113">If this value is omitted, a lower bound of zero is assumed for each dimension.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="63d91-114">备注</span><span class="sxs-lookup"><span data-stu-id="63d91-114">Remarks</span></span>  

 <span data-ttu-id="63d91-115">数组的元素可以是泛型类型的实例。</span><span class="sxs-lookup"><span data-stu-id="63d91-115">The elements of the array may be instances of a generic type.</span></span> <span data-ttu-id="63d91-116">始终在当前运行线程的应用程序域中创建数组。</span><span class="sxs-lookup"><span data-stu-id="63d91-116">The array is always created in the application domain in which the thread is currently running.</span></span> <span data-ttu-id="63d91-117">在 .NET Framework 2.0 中，的值 `rank` 必须为1。</span><span class="sxs-lookup"><span data-stu-id="63d91-117">In the .NET Framework 2.0, the value of `rank` must be 1.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="63d91-118">要求</span><span class="sxs-lookup"><span data-stu-id="63d91-118">Requirements</span></span>  

 <span data-ttu-id="63d91-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="63d91-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="63d91-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="63d91-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="63d91-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="63d91-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="63d91-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="63d91-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
