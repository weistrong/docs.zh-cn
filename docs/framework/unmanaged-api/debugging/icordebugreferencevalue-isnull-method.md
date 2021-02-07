---
description: 了解详细信息： ICorDebugReferenceValue：： IsNull 方法
title: ICorDebugReferenceValue::IsNull 方法
ms.date: 03/30/2017
api_name:
- ICorDebugReferenceValue.IsNull
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue::IsNull
helpviewer_keywords:
- IsNull method, ICorDebugReferenceValue interface [.NET Framework debugging]
- ICorDebugReferenceValue::IsNull method [.NET Framework debugging]
ms.assetid: 99e8c8d7-a1c0-47c8-9dbd-03e0b2bcb4d5
topic_type:
- apiref
ms.openlocfilehash: 9fffc869e20d1d3aa3a347ff2e026e6b55e6bd4f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691012"
---
# <a name="icordebugreferencevalueisnull-method"></a><span data-ttu-id="279f0-103">ICorDebugReferenceValue::IsNull 方法</span><span class="sxs-lookup"><span data-stu-id="279f0-103">ICorDebugReferenceValue::IsNull Method</span></span>

<span data-ttu-id="279f0-104">获取一个值，该值指示此 ICorDebugReferenceValue 是否为 null 值，在这种情况下，不 `ICorDebugReferenceValue` 指向对象。</span><span class="sxs-lookup"><span data-stu-id="279f0-104">Gets a value that indicates whether this ICorDebugReferenceValue is a null value, in which case the `ICorDebugReferenceValue` does not point to an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="279f0-105">语法</span><span class="sxs-lookup"><span data-stu-id="279f0-105">Syntax</span></span>  
  
```cpp  
HRESULT IsNull (  
    [out] BOOL   *pbNull  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="279f0-106">参数</span><span class="sxs-lookup"><span data-stu-id="279f0-106">Parameters</span></span>  

 `pbNull`  
 <span data-ttu-id="279f0-107">弄 `true` 如果此对象为 null，则为指向布尔值的指针 `ICorDebugReferenceValue` ; 否则为 `pbNull` `false` 。</span><span class="sxs-lookup"><span data-stu-id="279f0-107">[out] A pointer to a Boolean value that is `true` if this `ICorDebugReferenceValue` object is null; otherwise, `pbNull` is `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="279f0-108">要求</span><span class="sxs-lookup"><span data-stu-id="279f0-108">Requirements</span></span>  

 <span data-ttu-id="279f0-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="279f0-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="279f0-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="279f0-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="279f0-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="279f0-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="279f0-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="279f0-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
