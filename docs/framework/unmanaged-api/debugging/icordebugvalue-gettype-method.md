---
description: 了解详细信息： ICorDebugValue：： GetType 方法
title: ICorDebugValue::GetType 方法
ms.date: 03/30/2017
api_name:
- ICorDebugValue.GetType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue::GetType
helpviewer_keywords:
- ICorDebugValue::GetType method [.NET Framework debugging]
- GetType method, ICorDebugValue interface [.NET Framework debugging]
ms.assetid: 41e2d503-e1f1-407b-abe0-6a29adb3e0d1
topic_type:
- apiref
ms.openlocfilehash: 750e73634683a03e811d2756cc62c16b6dcea3de
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690320"
---
# <a name="icordebugvaluegettype-method"></a><span data-ttu-id="daeae-103">ICorDebugValue::GetType 方法</span><span class="sxs-lookup"><span data-stu-id="daeae-103">ICorDebugValue::GetType Method</span></span>

<span data-ttu-id="daeae-104">获取此 "ICorDebugValue" 对象的基元类型。</span><span class="sxs-lookup"><span data-stu-id="daeae-104">Gets the primitive type of this "ICorDebugValue" object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="daeae-105">语法</span><span class="sxs-lookup"><span data-stu-id="daeae-105">Syntax</span></span>  
  
```cpp  
HRESULT GetType (  
    [out] CorElementType   *pType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="daeae-106">参数</span><span class="sxs-lookup"><span data-stu-id="daeae-106">Parameters</span></span>  

 `pType`  
 <span data-ttu-id="daeae-107">弄一个指针，指向 "CorElementType" 枚举的值，该值指示值的类型。</span><span class="sxs-lookup"><span data-stu-id="daeae-107">[out] A pointer to a value of the "CorElementType" enumeration that indicates the value's type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="daeae-108">备注</span><span class="sxs-lookup"><span data-stu-id="daeae-108">Remarks</span></span>  

 <span data-ttu-id="daeae-109">如果对象是复杂的运行时类型，则可以通过接口的相应子类检查该类型 `ICorDebugValue` 。</span><span class="sxs-lookup"><span data-stu-id="daeae-109">If the object is a complex run-time type, that type may be examined through the appropriate subclasses of the `ICorDebugValue` interface.</span></span> <span data-ttu-id="daeae-110">例如，"ICorDebugObjectValue" 是从继承的，它 `ICorDebugValue` 表示一个复杂类型。</span><span class="sxs-lookup"><span data-stu-id="daeae-110">For example, "ICorDebugObjectValue", which inherits from `ICorDebugValue`, represents a complex type.</span></span>  
  
 <span data-ttu-id="daeae-111">`GetType`和[ICorDebugObjectValue：： GetClass](icordebugobjectvalue-getclass-method.md)方法各自返回值类型的相关信息。</span><span class="sxs-lookup"><span data-stu-id="daeae-111">The `GetType` and [ICorDebugObjectValue::GetClass](icordebugobjectvalue-getclass-method.md) methods each return information about the type of a value.</span></span> <span data-ttu-id="daeae-112">它们都是由识别泛型的 [ICorDebugValue2：： GetExactType](icordebugvalue2-getexacttype-method.md) 方法取代的。</span><span class="sxs-lookup"><span data-stu-id="daeae-112">They are both superseded by the generics-aware [ICorDebugValue2::GetExactType](icordebugvalue2-getexacttype-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="daeae-113">要求</span><span class="sxs-lookup"><span data-stu-id="daeae-113">Requirements</span></span>  

 <span data-ttu-id="daeae-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="daeae-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="daeae-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="daeae-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="daeae-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="daeae-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="daeae-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="daeae-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="daeae-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="daeae-118">See also</span></span>
