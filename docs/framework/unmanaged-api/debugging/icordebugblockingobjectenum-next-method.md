---
description: 了解详细信息： ICorDebugBlockingObjectEnum：： Next 方法
title: ICorDebugBlockingObjectEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugBlockingObjectEnum.Next Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBlockingObjectEnum::Next
helpviewer_keywords:
- Next method, ICorDebugBlockingObjectEnum interface [.NET Framework debugging]
- ICorDebugBlockingObjectEnum::Next method [.NET Framework debugging]
ms.assetid: 0121753f-ebea-48d0-aeb2-ed7fda76dc60
topic_type:
- apiref
ms.openlocfilehash: 66999ebf333c7115790b56afc1dc1d1ab7c47d69
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711812"
---
# <a name="icordebugblockingobjectenumnext-method"></a><span data-ttu-id="fba43-103">ICorDebugBlockingObjectEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="fba43-103">ICorDebugBlockingObjectEnum::Next Method</span></span>

<span data-ttu-id="fba43-104">从当前位置开始，获取枚举中指定的 [CorDebugBlockingObject](cordebugblockingobject-structure.md) 对象数。</span><span class="sxs-lookup"><span data-stu-id="fba43-104">Gets the specified number of [CorDebugBlockingObject](cordebugblockingobject-structure.md) objects from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fba43-105">语法</span><span class="sxs-lookup"><span data-stu-id="fba43-105">Syntax</span></span>  
  
```cpp  
HRESULT Next([in] ULONG  celt,  
             [out, size_is(celt), length_is(*pceltFetched)]  
                           CorDebugBlockingObject values[],  
             [out] ULONG *pceltFetched;  
```  
  
## <a name="parameters"></a><span data-ttu-id="fba43-106">参数</span><span class="sxs-lookup"><span data-stu-id="fba43-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="fba43-107">中要检索的对象的数目。</span><span class="sxs-lookup"><span data-stu-id="fba43-107">[in] The number of objects to retrieve.</span></span>  
  
 `values`  
 <span data-ttu-id="fba43-108">弄指向 [CorDebugBlockingObject](cordebugblockingobject-structure.md) 对象的指针的数组。</span><span class="sxs-lookup"><span data-stu-id="fba43-108">[out] An array of pointers to [CorDebugBlockingObject](cordebugblockingobject-structure.md) objects.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="fba43-109">弄一个指针，指向已检索到的对象的数目。</span><span class="sxs-lookup"><span data-stu-id="fba43-109">[out] A pointer to the number of objects that were retrieved.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fba43-110">返回值</span><span class="sxs-lookup"><span data-stu-id="fba43-110">Return Value</span></span>  

 <span data-ttu-id="fba43-111">此方法会返回以下特定的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="fba43-111">This method returns the following specific HRESULTs.</span></span>  
  
|<span data-ttu-id="fba43-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="fba43-112">HRESULT</span></span>|<span data-ttu-id="fba43-113">说明</span><span class="sxs-lookup"><span data-stu-id="fba43-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fba43-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="fba43-114">S_OK</span></span>|<span data-ttu-id="fba43-115">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="fba43-115">The method completed successfully.</span></span>|  
|<span data-ttu-id="fba43-116">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="fba43-116">S_FALSE</span></span>|<span data-ttu-id="fba43-117">`pceltFetched` 不等于 `celt`。</span><span class="sxs-lookup"><span data-stu-id="fba43-117">`pceltFetched` does not equal `celt`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fba43-118">备注</span><span class="sxs-lookup"><span data-stu-id="fba43-118">Remarks</span></span>  

 <span data-ttu-id="fba43-119">此方法的功能类似于典型的 COM 枚举器。</span><span class="sxs-lookup"><span data-stu-id="fba43-119">This method functions like a typical COM enumerator.</span></span>  
  
 <span data-ttu-id="fba43-120">输入数组值必须至少为大小 `celt` 。</span><span class="sxs-lookup"><span data-stu-id="fba43-120">The input array values must be at least of size `celt`.</span></span> <span data-ttu-id="fba43-121">数组将用枚举中的下一个值填充， `celt` 如果小于保留，则用所有剩余值填充 `celt` 。</span><span class="sxs-lookup"><span data-stu-id="fba43-121">The array will be filled with either the next `celt` values in the enumeration or with all remaining values if fewer than `celt` remain.</span></span> <span data-ttu-id="fba43-122">此方法返回时， `pceltFetched` 将用检索到的值的数目进行填充。</span><span class="sxs-lookup"><span data-stu-id="fba43-122">When this method returns, `pceltFetched` will be filled with the number of values that were retrieved.</span></span> <span data-ttu-id="fba43-123">如果 `values` 包含无效指针或指向小于的缓冲区， `celt` 或者如果 `pceltFetched` 是无效指针，则结果是不确定的。</span><span class="sxs-lookup"><span data-stu-id="fba43-123">If `values` contains invalid pointers or points to a buffer that is smaller than `celt`, or if `pceltFetched` is an invalid pointer, the result is undefined.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="fba43-124">尽管不需要释放 [CorDebugBlockingObject](cordebugblockingobject-structure.md) 结构，但它内的 "ICorDebugValue" 接口需要释放。</span><span class="sxs-lookup"><span data-stu-id="fba43-124">Although the [CorDebugBlockingObject](cordebugblockingobject-structure.md) structure does not need to be released, the "ICorDebugValue" interface inside of it does need to be released.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fba43-125">要求</span><span class="sxs-lookup"><span data-stu-id="fba43-125">Requirements</span></span>  

 <span data-ttu-id="fba43-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fba43-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fba43-127">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fba43-127">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fba43-128">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fba43-128">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fba43-129">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fba43-129">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fba43-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="fba43-130">See also</span></span>

- [<span data-ttu-id="fba43-131">ICorDebugDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="fba43-131">ICorDebugDataTarget Interface</span></span>](icordebugdatatarget-interface.md)
- [<span data-ttu-id="fba43-132">调试接口</span><span class="sxs-lookup"><span data-stu-id="fba43-132">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="fba43-133">调试</span><span class="sxs-lookup"><span data-stu-id="fba43-133">Debugging</span></span>](index.md)
