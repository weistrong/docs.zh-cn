---
description: 了解详细信息： ICorDebugGenericValue：： GetValue 方法
title: ICorDebugGenericValue::GetValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugGenericValue.GetValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGenericValue::GetValue
helpviewer_keywords:
- ICorDebugGenericValue::GetValue method [.NET Framework debugging]
- GetValue method, ICorDebugGenericValue interface [.NET Framework debugging]
ms.assetid: 4e95d7cb-144d-4ccf-8a69-d605f4744be2
topic_type:
- apiref
ms.openlocfilehash: 9c8459ce6a9fb59e934b1ebd355aa091a37b2d7b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661020"
---
# <a name="icordebuggenericvaluegetvalue-method"></a><span data-ttu-id="585a3-103">ICorDebugGenericValue::GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="585a3-103">ICorDebugGenericValue::GetValue Method</span></span>

<span data-ttu-id="585a3-104">将此泛型的值复制到指定的缓冲区中。</span><span class="sxs-lookup"><span data-stu-id="585a3-104">Copies the value of this generic into the specified buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="585a3-105">语法</span><span class="sxs-lookup"><span data-stu-id="585a3-105">Syntax</span></span>  
  
```cpp  
HRESULT GetValue (  
    [out] void     *pTo  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="585a3-106">参数</span><span class="sxs-lookup"><span data-stu-id="585a3-106">Parameters</span></span>  

 `pTo`  
 <span data-ttu-id="585a3-107">弄一个指针，指向由此 ICorDebugGenericValue 对象表示的值。</span><span class="sxs-lookup"><span data-stu-id="585a3-107">[out] A pointer to the value that is represented by this ICorDebugGenericValue object.</span></span> <span data-ttu-id="585a3-108">此值可以是简单类型，也可以是引用类型 (即，指针) 。</span><span class="sxs-lookup"><span data-stu-id="585a3-108">The value may be a simple type or a reference type (that is, a pointer).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="585a3-109">要求</span><span class="sxs-lookup"><span data-stu-id="585a3-109">Requirements</span></span>  

 <span data-ttu-id="585a3-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="585a3-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="585a3-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="585a3-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="585a3-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="585a3-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="585a3-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="585a3-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
