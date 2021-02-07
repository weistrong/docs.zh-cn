---
description: 了解详细信息： ICorDebugValue：： GetSize 方法
title: ICorDebugValue::GetSize 方法
ms.date: 03/30/2017
api_name:
- ICorDebugValue.GetSize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue::GetSize
helpviewer_keywords:
- GetSize method, ICorDebugValue interface [.NET Framework debugging]
- ICorDebugValue::GetSize method [.NET Framework debugging]
ms.assetid: 445a9ee3-e050-4f3a-931a-96b0efb00110
topic_type:
- apiref
ms.openlocfilehash: 3fc2582990d58fa2e42f240dfd3e563eed34e372
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690335"
---
# <a name="icordebugvaluegetsize-method"></a><span data-ttu-id="3fc3d-103">ICorDebugValue::GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="3fc3d-103">ICorDebugValue::GetSize Method</span></span>

<span data-ttu-id="3fc3d-104">获取此 "ICorDebugValue" 对象的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="3fc3d-104">Gets the size, in bytes, of this "ICorDebugValue" object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3fc3d-105">语法</span><span class="sxs-lookup"><span data-stu-id="3fc3d-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSize (  
    [out] ULONG32   *pSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3fc3d-106">参数</span><span class="sxs-lookup"><span data-stu-id="3fc3d-106">Parameters</span></span>  

 `pSize`  
 <span data-ttu-id="3fc3d-107">弄此值对象的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="3fc3d-107">[out] The size, in bytes, of this value object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3fc3d-108">备注</span><span class="sxs-lookup"><span data-stu-id="3fc3d-108">Remarks</span></span>  

 <span data-ttu-id="3fc3d-109">如果值的类型为引用类型，则此方法返回指针的大小，而不是对象的大小。</span><span class="sxs-lookup"><span data-stu-id="3fc3d-109">If the value's type is a reference type, this method returns the size of the pointer rather than the size of the object.</span></span>  
  
 <span data-ttu-id="3fc3d-110">此 `ICorDebugValue::GetSize` 方法 `COR_E_OVERFLOW` 为64位平台上大于 4 GB 的对象返回。</span><span class="sxs-lookup"><span data-stu-id="3fc3d-110">The `ICorDebugValue::GetSize` method returns `COR_E_OVERFLOW` for objects that are larger than 4 GB on 64-bit platforms.</span></span> <span data-ttu-id="3fc3d-111">使用 [ICorDebugValue3：： GetSize64](icordebugvalue3-getsize64-method.md) 方法代替大于 4 GB 的对象。</span><span class="sxs-lookup"><span data-stu-id="3fc3d-111">Use the [ICorDebugValue3::GetSize64](icordebugvalue3-getsize64-method.md) method instead for objects that are larger than 4 GB.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3fc3d-112">要求</span><span class="sxs-lookup"><span data-stu-id="3fc3d-112">Requirements</span></span>  

 <span data-ttu-id="3fc3d-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3fc3d-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3fc3d-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3fc3d-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3fc3d-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3fc3d-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3fc3d-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3fc3d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3fc3d-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="3fc3d-117">See also</span></span>

- [<span data-ttu-id="3fc3d-118">GetSize64 方法</span><span class="sxs-lookup"><span data-stu-id="3fc3d-118">GetSize64 Method</span></span>](icordebugvalue3-getsize64-method.md)
