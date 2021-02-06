---
description: 了解详细信息： ICorDebugProcess5：： GetTypeID 方法
title: ICorDebugProcess5::GetTypeID 方法
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugProcess5.GetTypeID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::GetTypeID
helpviewer_keywords:
- ICorDebugProcess5::GetTypeID method [.NET Framework debugging]
- GetTypeID method, ICorDebugProcess5 interface [.NET Framework debugging]
ms.assetid: 47dbaea4-8857-462e-93ba-fff880fc9e50
topic_type:
- apiref
ms.openlocfilehash: 564fc2819c9c370844111cf497d62e6d89cb28b0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649697"
---
# <a name="icordebugprocess5gettypeid-method"></a><span data-ttu-id="fa19f-103">ICorDebugProcess5::GetTypeID 方法</span><span class="sxs-lookup"><span data-stu-id="fa19f-103">ICorDebugProcess5::GetTypeID Method</span></span>

<span data-ttu-id="fa19f-104">将对象地址转换为 [COR_TYPEID](cor-typeid-structure.md) 的标识符。</span><span class="sxs-lookup"><span data-stu-id="fa19f-104">Converts an object address to a [COR_TYPEID](cor-typeid-structure.md) identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa19f-105">语法</span><span class="sxs-lookup"><span data-stu-id="fa19f-105">Syntax</span></span>  
  
```cpp
HRESULT GetTypeID(  
    [in] CORDB_ADDRESS obj,  
    [out] COR_TYPEID *pId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fa19f-106">参数</span><span class="sxs-lookup"><span data-stu-id="fa19f-106">Parameters</span></span>  

 `obj`  
 <span data-ttu-id="fa19f-107">中对象地址。</span><span class="sxs-lookup"><span data-stu-id="fa19f-107">[in] The object address.</span></span>  
  
 `pId`  
 <span data-ttu-id="fa19f-108">一个指针，指向用于标识对象的 [COR_TYPEID](cor-typeid-structure.md) 值。</span><span class="sxs-lookup"><span data-stu-id="fa19f-108">A pointer to the [COR_TYPEID](cor-typeid-structure.md) value that identifies the object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fa19f-109">备注</span><span class="sxs-lookup"><span data-stu-id="fa19f-109">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fa19f-110">要求</span><span class="sxs-lookup"><span data-stu-id="fa19f-110">Requirements</span></span>  

 <span data-ttu-id="fa19f-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fa19f-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa19f-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fa19f-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fa19f-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fa19f-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fa19f-114">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa19f-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa19f-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="fa19f-115">See also</span></span>

- [<span data-ttu-id="fa19f-116">ICorDebugProcess5 接口</span><span class="sxs-lookup"><span data-stu-id="fa19f-116">ICorDebugProcess5 Interface</span></span>](icordebugprocess5-interface.md)
- [<span data-ttu-id="fa19f-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="fa19f-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
