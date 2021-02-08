---
description: 了解详细信息： ICorDebugVariableHomeEnum：： Next 方法
title: ICorDebugVariableHomeEnum：： Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHomeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHomeEnum::Next
helpviewer_keywords:
- ICorDebugVariableHomeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugVariableHomeEnum interface [.NET Framework debugging]
ms.assetid: eb9ea96c-5b58-4655-8104-094fc8b393b8
topic_type:
- apiref
ms.openlocfilehash: 0aa0174e67bceaa724ddfeadc2560d12e112b859
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790602"
---
# <a name="icordebugvariablehomeenumnext-method"></a><span data-ttu-id="00e57-103">ICorDebugVariableHomeEnum：： Next 方法</span><span class="sxs-lookup"><span data-stu-id="00e57-103">ICorDebugVariableHomeEnum::Next Method</span></span>

<span data-ttu-id="00e57-104">获取指定数量的 [ICorDebugVariableHome](icordebugvariablehome-interface.md) 实例，其中包含有关函数中的局部变量和参数的信息。</span><span class="sxs-lookup"><span data-stu-id="00e57-104">Gets the specified number of [ICorDebugVariableHome](icordebugvariablehome-interface.md) instances that contain information about the local variables and arguments in a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00e57-105">语法</span><span class="sxs-lookup"><span data-stu-id="00e57-105">Syntax</span></span>  
  
```cpp  
HRESULT Next(  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)] ICorDebugVariableHome *homes[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="00e57-106">参数</span><span class="sxs-lookup"><span data-stu-id="00e57-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="00e57-107">[in] 要检索的对象数。</span><span class="sxs-lookup"><span data-stu-id="00e57-107">[in] The number of objects to be retrieved.</span></span>  
  
 `homes`  
 <span data-ttu-id="00e57-108">指针的数组，其中每个都指向一个 [ICorDebugVariableHome](icordebugvariablehome-interface.md) 对象，该对象提供有关函数的局部变量或自变量的信息。</span><span class="sxs-lookup"><span data-stu-id="00e57-108">An array of pointers, each of which points to a [ICorDebugVariableHome](icordebugvariablehome-interface.md) object that provides information about  a local variable or argument of a function.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="00e57-109">弄对象中实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="00e57-109">[out] The number of instances actually returned in objects.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="00e57-110">返回值</span><span class="sxs-lookup"><span data-stu-id="00e57-110">Return Value</span></span>  

 <span data-ttu-id="00e57-111">方法返回以下值。</span><span class="sxs-lookup"><span data-stu-id="00e57-111">The method returns the following values.</span></span>  
  
|<span data-ttu-id="00e57-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="00e57-112">HRESULT</span></span>|<span data-ttu-id="00e57-113">说明</span><span class="sxs-lookup"><span data-stu-id="00e57-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="00e57-114">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="00e57-114">The method completed successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="00e57-115">检索到的实际实例数小于所请求的 `pceltFetched` 实例数。</span><span class="sxs-lookup"><span data-stu-id="00e57-115">The actual number of instances retrieved, as reflected in `pceltFetched`, is less than the number of instances requested.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="00e57-116">备注</span><span class="sxs-lookup"><span data-stu-id="00e57-116">Remarks</span></span>  

 <span data-ttu-id="00e57-117">[ICorDebugVariableHomeEnum：： Next](icordebugvariablehomeenum-next-method.md)方法 `celt` 从枚举器的当前位置开始检索最多对象。</span><span class="sxs-lookup"><span data-stu-id="00e57-117">The [ICorDebugVariableHomeEnum::Next](icordebugvariablehomeenum-next-method.md) method retrieves a maximum of  `celt` objects starting at the current position of the enumerator.</span></span> <span data-ttu-id="00e57-118">当方法返回时， `pceltFetched` 包含检索到的对象的实际数目。</span><span class="sxs-lookup"><span data-stu-id="00e57-118">When the method returns, `pceltFetched` contains the actual number of objects retrieved.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="00e57-119">要求</span><span class="sxs-lookup"><span data-stu-id="00e57-119">Requirements</span></span>  

 <span data-ttu-id="00e57-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="00e57-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="00e57-121">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="00e57-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="00e57-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="00e57-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="00e57-123">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="00e57-123">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00e57-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="00e57-124">See also</span></span>

- [<span data-ttu-id="00e57-125">ICorDebugVariableHomeEnum 接口</span><span class="sxs-lookup"><span data-stu-id="00e57-125">ICorDebugVariableHomeEnum Interface</span></span>](icordebugvariablehomeenum-interface.md)
- [<span data-ttu-id="00e57-126">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="00e57-126">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
