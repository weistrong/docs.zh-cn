---
description: 了解详细信息： ICorDebugObjectValue：： IsValueClass 方法
title: ICorDebugObjectValue::IsValueClass 方法
ms.date: 03/30/2017
api_name:
- ICorDebugObjectValue.IsValueClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectValue::IsValueClass
helpviewer_keywords:
- ICorDebugObjectValue::IsValueClass method [.NET Framework debugging]
- IsValueClass method [.NET Framework debugging]
ms.assetid: 13d89a4a-5d9d-4a79-9600-5e2a98c3d166
topic_type:
- apiref
ms.openlocfilehash: bf3ce94a06092209507fd1ff737e09a77b5d0c70
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728920"
---
# <a name="icordebugobjectvalueisvalueclass-method"></a><span data-ttu-id="8cbef-103">ICorDebugObjectValue::IsValueClass 方法</span><span class="sxs-lookup"><span data-stu-id="8cbef-103">ICorDebugObjectValue::IsValueClass Method</span></span>

<span data-ttu-id="8cbef-104">获取一个值，该值指示此对象值是否为值类型。</span><span class="sxs-lookup"><span data-stu-id="8cbef-104">Gets a value that indicates whether this object value is a value type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8cbef-105">语法</span><span class="sxs-lookup"><span data-stu-id="8cbef-105">Syntax</span></span>  
  
```cpp  
HRESULT IsValueClass (  
    [out] BOOL               *pbIsValueClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8cbef-106">参数</span><span class="sxs-lookup"><span data-stu-id="8cbef-106">Parameters</span></span>  

 `pbIsValueClass`  
 <span data-ttu-id="8cbef-107">弄一个指向布尔值的指针， `true` 如果该对象值由此 "ICorDebugObjectValue" 表示，则为值类型而不是引用类型; 否则为 `pbIsValueClass` `false` 。</span><span class="sxs-lookup"><span data-stu-id="8cbef-107">[out] A pointer to a Boolean value that is `true` if the object value, represented by this "ICorDebugObjectValue", is a value type rather than a reference type; otherwise, `pbIsValueClass` is `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8cbef-108">要求</span><span class="sxs-lookup"><span data-stu-id="8cbef-108">Requirements</span></span>  

 <span data-ttu-id="8cbef-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8cbef-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8cbef-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8cbef-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8cbef-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8cbef-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8cbef-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8cbef-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8cbef-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="8cbef-113">See also</span></span>
