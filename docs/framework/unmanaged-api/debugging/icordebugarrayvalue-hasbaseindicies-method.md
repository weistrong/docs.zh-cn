---
description: 了解详细信息： ICorDebugArrayValue：： HasBaseIndicies 方法
title: ICorDebugArrayValue::HasBaseIndicies 方法
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.HasBaseIndicies
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::HasBaseIndicies
helpviewer_keywords:
- HasBaseIndicies method [.NET Framework debugging]
- ICorDebugArrayValue::HasBaseIndicies method [.NET Framework debugging]
ms.assetid: aa26df07-e0a6-4608-bdef-d4afafec89aa
topic_type:
- apiref
ms.openlocfilehash: b251653004801ff2d312dfb34749c413774ddf40
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722953"
---
# <a name="icordebugarrayvaluehasbaseindicies-method"></a><span data-ttu-id="b6838-103">ICorDebugArrayValue::HasBaseIndicies 方法</span><span class="sxs-lookup"><span data-stu-id="b6838-103">ICorDebugArrayValue::HasBaseIndicies Method</span></span>

<span data-ttu-id="b6838-104">获取一个值，该值指示此数组的任何维度是否具有非零的基本索引。</span><span class="sxs-lookup"><span data-stu-id="b6838-104">Gets a value that indicates whether any dimensions of this array have a base index of non-zero.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6838-105">语法</span><span class="sxs-lookup"><span data-stu-id="b6838-105">Syntax</span></span>  
  
```cpp  
HRESULT HasBaseIndicies (  
    [out] BOOL    *pbHasBaseIndicies  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b6838-106">参数</span><span class="sxs-lookup"><span data-stu-id="b6838-106">Parameters</span></span>  

 `pbHasBaseIndicies`  
 <span data-ttu-id="b6838-107">弄指向布尔值的指针， `true` 如果此对象的一个或多个维度的 `ICorDebugArrayValue` 基本索引为非零，则为; 否则为布尔值 `false` 。</span><span class="sxs-lookup"><span data-stu-id="b6838-107">[out] A pointer to a Boolean value that is `true` if one or more dimensions of this `ICorDebugArrayValue` object have a base index of non-zero; otherwise, the Boolean value is `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b6838-108">要求</span><span class="sxs-lookup"><span data-stu-id="b6838-108">Requirements</span></span>  

 <span data-ttu-id="b6838-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b6838-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b6838-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b6838-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b6838-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b6838-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b6838-112">**.NET Framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b6838-112">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>
