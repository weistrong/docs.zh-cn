---
description: 了解详细信息： ICorDebugReferenceValue：:D ereference 方法
title: ICorDebugReferenceValue::Dereference 方法
ms.date: 03/30/2017
api_name:
- ICorDebugReferenceValue.Dereference
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue::Dereference
helpviewer_keywords:
- ICorDebugReferenceValue::Dereference method [.NET Framework debugging]
- Dereference method [.NET Framework debugging]
ms.assetid: 5ec8cf76-3deb-4ce6-9a49-77a4c35d80b9
topic_type:
- apiref
ms.openlocfilehash: af225f746a9c67a90a7ad73046cd03401e4ba735
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691102"
---
# <a name="icordebugreferencevaluedereference-method"></a><span data-ttu-id="b9fde-103">ICorDebugReferenceValue::Dereference 方法</span><span class="sxs-lookup"><span data-stu-id="b9fde-103">ICorDebugReferenceValue::Dereference Method</span></span>

<span data-ttu-id="b9fde-104">获取所引用的对象。</span><span class="sxs-lookup"><span data-stu-id="b9fde-104">Gets the object that is referenced.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9fde-105">语法</span><span class="sxs-lookup"><span data-stu-id="b9fde-105">Syntax</span></span>  
  
```cpp  
HRESULT Dereference (  
    [out] ICorDebugValue  **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b9fde-106">参数</span><span class="sxs-lookup"><span data-stu-id="b9fde-106">Parameters</span></span>  

 `ppValue`  
 <span data-ttu-id="b9fde-107">弄一个指针，指向表示此 ICorDebugReferenceValue 对象指向的对象的 ICorDebugValue 的地址。</span><span class="sxs-lookup"><span data-stu-id="b9fde-107">[out] A pointer to the address of an ICorDebugValue that represents the object to which this ICorDebugReferenceValue object points.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b9fde-108">备注</span><span class="sxs-lookup"><span data-stu-id="b9fde-108">Remarks</span></span>  

 <span data-ttu-id="b9fde-109">此 `ICorDebugValue` 对象仅在其引用尚未禁用时有效。</span><span class="sxs-lookup"><span data-stu-id="b9fde-109">The `ICorDebugValue` object is valid only while its reference has not yet been disabled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b9fde-110">要求</span><span class="sxs-lookup"><span data-stu-id="b9fde-110">Requirements</span></span>  

 <span data-ttu-id="b9fde-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b9fde-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9fde-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b9fde-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b9fde-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b9fde-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b9fde-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b9fde-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
