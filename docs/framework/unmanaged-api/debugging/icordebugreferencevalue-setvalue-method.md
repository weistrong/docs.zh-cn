---
description: 了解详细信息： ICorDebugReferenceValue：： SetValue 方法
title: ICorDebugReferenceValue::SetValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugReferenceValue.SetValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue::SetValue
helpviewer_keywords:
- SetValue method, ICorDebugReferenceValue interface [.NET Framework debugging]
- ICorDebugReferenceValue::SetValue method [.NET Framework debugging]
ms.assetid: 3d3f6eec-d772-401f-a028-1a2ecdc31e95
topic_type:
- apiref
ms.openlocfilehash: 44909962d2716ddb606d98a2f6b3804247c581cd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690907"
---
# <a name="icordebugreferencevaluesetvalue-method"></a><span data-ttu-id="5db33-103">ICorDebugReferenceValue::SetValue 方法</span><span class="sxs-lookup"><span data-stu-id="5db33-103">ICorDebugReferenceValue::SetValue Method</span></span>

<span data-ttu-id="5db33-104">设置指定的内存地址。</span><span class="sxs-lookup"><span data-stu-id="5db33-104">Sets the specified memory address.</span></span> <span data-ttu-id="5db33-105">也就是说，此方法会将此 ICorDebugReferenceValue 设置为指向某个对象。</span><span class="sxs-lookup"><span data-stu-id="5db33-105">That is, this method sets this ICorDebugReferenceValue to point to an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5db33-106">语法</span><span class="sxs-lookup"><span data-stu-id="5db33-106">Syntax</span></span>  
  
```cpp  
HRESULT SetValue (  
    [in] CORDB_ADDRESS    value  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5db33-107">参数</span><span class="sxs-lookup"><span data-stu-id="5db33-107">Parameters</span></span>  

 `value`  
 <span data-ttu-id="5db33-108">中一个 `CORDB_ADDRESS` 值，该值指定此指向的对象的地址 `ICorDebugReferenceValue` 。</span><span class="sxs-lookup"><span data-stu-id="5db33-108">[in] A `CORDB_ADDRESS` value that specifies the address of the object to which this `ICorDebugReferenceValue` points.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5db33-109">要求</span><span class="sxs-lookup"><span data-stu-id="5db33-109">Requirements</span></span>  

 <span data-ttu-id="5db33-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5db33-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5db33-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5db33-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5db33-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5db33-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5db33-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5db33-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
