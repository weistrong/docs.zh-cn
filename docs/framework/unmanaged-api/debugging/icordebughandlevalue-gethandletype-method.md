---
description: 了解详细信息： ICorDebugHandleValue：： GetHandleType 方法
title: ICorDebugHandleValue::GetHandleType 方法
ms.date: 03/30/2017
api_name:
- ICorDebugHandleValue.GetHandleType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHandleValue::GetHandleType
helpviewer_keywords:
- GetHandleType method [.NET Framework debugging]
- ICorDebugHandleValue::GetHandleType method [.NET Framework debugging]
ms.assetid: d5e7b12d-835a-4e86-ae2f-d658d4f1c67c
topic_type:
- apiref
ms.openlocfilehash: 708d60cd8116cf3f0fdc436a34d863380be2543d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660955"
---
# <a name="icordebughandlevaluegethandletype-method"></a><span data-ttu-id="85a9a-103">ICorDebugHandleValue::GetHandleType 方法</span><span class="sxs-lookup"><span data-stu-id="85a9a-103">ICorDebugHandleValue::GetHandleType Method</span></span>

<span data-ttu-id="85a9a-104">获取一个值，该值指示此 ICorDebugHandleValue 对象所引用的句柄的类型。</span><span class="sxs-lookup"><span data-stu-id="85a9a-104">Gets a value that indicates the kind of handle referenced by this ICorDebugHandleValue object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="85a9a-105">语法</span><span class="sxs-lookup"><span data-stu-id="85a9a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetHandleType (  
    [out] CorDebugHandleType  *pType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="85a9a-106">参数</span><span class="sxs-lookup"><span data-stu-id="85a9a-106">Parameters</span></span>  

 `pType`  
 <span data-ttu-id="85a9a-107">弄指向 CorDebugHandleType 枚举的值的指针，该枚举指示此句柄的类型。</span><span class="sxs-lookup"><span data-stu-id="85a9a-107">[out] A pointer to a value of the CorDebugHandleType enumeration that indicates the type of this handle.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="85a9a-108">要求</span><span class="sxs-lookup"><span data-stu-id="85a9a-108">Requirements</span></span>  

 <span data-ttu-id="85a9a-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="85a9a-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="85a9a-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="85a9a-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="85a9a-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="85a9a-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="85a9a-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="85a9a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
