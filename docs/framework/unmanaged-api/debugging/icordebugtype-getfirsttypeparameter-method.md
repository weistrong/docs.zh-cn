---
description: 了解详细信息： ICorDebugType：： GetFirstTypeParameter 方法
title: ICorDebugType::GetFirstTypeParameter 方法
ms.date: 03/30/2017
api_name:
- ICorDebugType.GetFirstTypeParameter
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::GetFirstTypeParameter
helpviewer_keywords:
- ICorDebugType::GetFirstTypeParameter method [.NET Framework debugging]
- GetFirstTypeParameter method [.NET Framework debugging]
ms.assetid: 35bb594f-af6a-4349-83fe-e98702674e03
topic_type:
- apiref
ms.openlocfilehash: 4c37217f34f80c916d618d88e4917eab794a1d90
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658264"
---
# <a name="icordebugtypegetfirsttypeparameter-method"></a><span data-ttu-id="de7e7-103">ICorDebugType::GetFirstTypeParameter 方法</span><span class="sxs-lookup"><span data-stu-id="de7e7-103">ICorDebugType::GetFirstTypeParameter Method</span></span>

<span data-ttu-id="de7e7-104">获取一个接口指针，该指针指向表示由此表示的类型的第一个 <xref:System.Type> 参数的 ICorDebugType `ICorDebugType` 。</span><span class="sxs-lookup"><span data-stu-id="de7e7-104">Gets an interface pointer to an ICorDebugType that represents the first <xref:System.Type> parameter of the type represented by this `ICorDebugType`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de7e7-105">语法</span><span class="sxs-lookup"><span data-stu-id="de7e7-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFirstTypeParameter (  
    [out] ICorDebugType   **value  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="de7e7-106">参数</span><span class="sxs-lookup"><span data-stu-id="de7e7-106">Parameters</span></span>  

 `value`  
 <span data-ttu-id="de7e7-107">弄一个指针，指向 `ICorDebugType` 表示第一个参数的对象的地址。</span><span class="sxs-lookup"><span data-stu-id="de7e7-107">[out] A pointer to the address of an `ICorDebugType` object that represents the first parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="de7e7-108">备注</span><span class="sxs-lookup"><span data-stu-id="de7e7-108">Remarks</span></span>  

 <span data-ttu-id="de7e7-109">`GetFirstTypeParameter` 当有关类型的附加信息最多涉及一个类型参数时，可以调用。</span><span class="sxs-lookup"><span data-stu-id="de7e7-109">`GetFirstTypeParameter` can be called in cases where the additional information about the type involves, at most, one type parameter.</span></span> <span data-ttu-id="de7e7-110">特别是，如果类型是 ELEMENT_TYPE_ARRAY、ELEMENT_TYPE_SZARRAY、ELEMENT_TYPE_BYREF 或 ELEMENT_TYPE_PTR （如 [ICorDebugType：： GetType](icordebugtype-gettype-method.md) 方法所示），则可以使用此方法。</span><span class="sxs-lookup"><span data-stu-id="de7e7-110">In particular, it can be used if the type is an ELEMENT_TYPE_ARRAY, ELEMENT_TYPE_SZARRAY, ELEMENT_TYPE_BYREF, or ELEMENT_TYPE_PTR, as indicated by the [ICorDebugType::GetType](icordebugtype-gettype-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="de7e7-111">要求</span><span class="sxs-lookup"><span data-stu-id="de7e7-111">Requirements</span></span>  

 <span data-ttu-id="de7e7-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="de7e7-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="de7e7-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="de7e7-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="de7e7-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="de7e7-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="de7e7-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="de7e7-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
