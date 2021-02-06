---
description: 了解详细信息： ICorDebugType：： GetClass 方法
title: ICorDebugType::GetClass 方法
ms.date: 03/30/2017
api_name:
- ICorDebugType.GetClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::GetClass
helpviewer_keywords:
- ICorDebugType::GetClass method [.NET Framework debugging]
- GetClass method, ICorDebugType interface [.NET Framework debugging]
ms.assetid: 2644f48b-db3c-429f-ae62-76f1c98a1af5
topic_type:
- apiref
ms.openlocfilehash: 2e8d68fbc8909599ca649ba0e226cc84af820939
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658316"
---
# <a name="icordebugtypegetclass-method"></a><span data-ttu-id="5f6fb-103">ICorDebugType::GetClass 方法</span><span class="sxs-lookup"><span data-stu-id="5f6fb-103">ICorDebugType::GetClass Method</span></span>

<span data-ttu-id="5f6fb-104">获取一个接口指针，该指针指向表示未实例化的泛型类型的 ICorDebugClass。</span><span class="sxs-lookup"><span data-stu-id="5f6fb-104">Gets an interface pointer to an ICorDebugClass that represents the uninstantiated generic type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f6fb-105">语法</span><span class="sxs-lookup"><span data-stu-id="5f6fb-105">Syntax</span></span>  
  
```cpp  
HRESULT GetClass (  
    [out] ICorDebugClass   **ppClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5f6fb-106">参数</span><span class="sxs-lookup"><span data-stu-id="5f6fb-106">Parameters</span></span>  

 `ppClass`  
 <span data-ttu-id="5f6fb-107">弄一个指针，指向 `ICorDebugClass` 表示未实例化的泛型类型的接口的地址。</span><span class="sxs-lookup"><span data-stu-id="5f6fb-107">[out] A pointer to the address of an `ICorDebugClass` interface that represents the uninstantiated generic type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5f6fb-108">备注</span><span class="sxs-lookup"><span data-stu-id="5f6fb-108">Remarks</span></span>  

 <span data-ttu-id="5f6fb-109">`GetClass` 只能在某些条件下调用。</span><span class="sxs-lookup"><span data-stu-id="5f6fb-109">`GetClass` can be called only under certain conditions.</span></span> <span data-ttu-id="5f6fb-110">调用 [ICorDebugType：： GetType](icordebugtype-gettype-method.md) ，然后调用 `GetClass` 。</span><span class="sxs-lookup"><span data-stu-id="5f6fb-110">Call [ICorDebugType::GetType](icordebugtype-gettype-method.md) before calling `GetClass`.</span></span> <span data-ttu-id="5f6fb-111">如果 `ICorDebugType::GetType` 返回 ELEMENT_TYPE_CLASS 或 ELEMENT_TYPE_VALUETYPE 的 CorElementType 值，则 `GetClass` 可以调用来获取泛型类型的实例化类型。</span><span class="sxs-lookup"><span data-stu-id="5f6fb-111">If `ICorDebugType::GetType` returns a CorElementType value that is ELEMENT_TYPE_CLASS or ELEMENT_TYPE_VALUETYPE, `GetClass` can be called to get the uninstantiated type for a generic type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5f6fb-112">要求</span><span class="sxs-lookup"><span data-stu-id="5f6fb-112">Requirements</span></span>  

 <span data-ttu-id="5f6fb-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5f6fb-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f6fb-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5f6fb-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5f6fb-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5f6fb-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5f6fb-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f6fb-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
