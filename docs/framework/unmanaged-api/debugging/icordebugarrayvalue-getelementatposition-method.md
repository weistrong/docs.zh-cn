---
description: 了解详细信息： ICorDebugArrayValue：： GetElementAtPosition 方法
title: ICorDebugArrayValue::GetElementAtPosition 方法
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetElementAtPosition
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetElementAtPosition
helpviewer_keywords:
- GetElementAtPosition method [.NET Framework debugging]
- ICorDebugArrayValue::GetElementAtPosition method [.NET Framework debugging]
ms.assetid: 6fd5eaa4-1997-4910-82f5-3887480db764
topic_type:
- apiref
ms.openlocfilehash: ef8e4a39f5fe4088b1883803aee037c51f410241
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723021"
---
# <a name="icordebugarrayvaluegetelementatposition-method"></a><span data-ttu-id="2d834-103">ICorDebugArrayValue::GetElementAtPosition 方法</span><span class="sxs-lookup"><span data-stu-id="2d834-103">ICorDebugArrayValue::GetElementAtPosition Method</span></span>

<span data-ttu-id="2d834-104">获取位于给定位置的元素，并将该数组视为从零开始的一维数组。</span><span class="sxs-lookup"><span data-stu-id="2d834-104">Gets the element at the given position, treating the array as a zero-based, single-dimensional array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d834-105">语法</span><span class="sxs-lookup"><span data-stu-id="2d834-105">Syntax</span></span>  
  
```cpp  
HRESULT GetElementAtPosition (  
    [in]  ULONG32          nPosition,  
    [out] ICorDebugValue   **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2d834-106">参数</span><span class="sxs-lookup"><span data-stu-id="2d834-106">Parameters</span></span>  

 `nPosition`  
 <span data-ttu-id="2d834-107">中要检索的元素的位置。</span><span class="sxs-lookup"><span data-stu-id="2d834-107">[in] The position of the element to be retrieved.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="2d834-108">弄指向表示元素值的 ICorDebugValue 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="2d834-108">[out] A pointer to the address of an ICorDebugValue object that represents the value of the element.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2d834-109">备注</span><span class="sxs-lookup"><span data-stu-id="2d834-109">Remarks</span></span>  

 <span data-ttu-id="2d834-110">多维数组的布局遵循数组布局的 c + + 样式。</span><span class="sxs-lookup"><span data-stu-id="2d834-110">The layout of a multi-dimension array follows the C++ style of array layout.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d834-111">要求</span><span class="sxs-lookup"><span data-stu-id="2d834-111">Requirements</span></span>  

 <span data-ttu-id="2d834-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2d834-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d834-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2d834-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2d834-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2d834-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2d834-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d834-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
