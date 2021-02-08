---
description: 了解详细信息： ICorDebugVariableHome：： GetSlotIndex 方法
title: ICorDebugVariableHome：： GetSlotIndex 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetSlotIndex
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetSlotIndex
helpviewer_keywords:
- ICorDebugVariableHome::GetSlotIndex method [.NET Framework debugging]
- GetSlotIndex method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: 966da50d-5665-4fff-bf7b-1c72bbadd9a4
topic_type:
- apiref
ms.openlocfilehash: 7f6ee01c2bfcee4c78f8463a7cefac1f90a3295f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790641"
---
# <a name="icordebugvariablehomegetslotindex-method"></a><span data-ttu-id="7fe7d-103">ICorDebugVariableHome：： GetSlotIndex 方法</span><span class="sxs-lookup"><span data-stu-id="7fe7d-103">ICorDebugVariableHome::GetSlotIndex Method</span></span>

<span data-ttu-id="7fe7d-104">获取本地变量的托管槽索引。</span><span class="sxs-lookup"><span data-stu-id="7fe7d-104">Gets the managed slot-index of a local variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7fe7d-105">语法</span><span class="sxs-lookup"><span data-stu-id="7fe7d-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSlotIndex(  
    [out] ULONG32 *pSlotIndex  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7fe7d-106">参数</span><span class="sxs-lookup"><span data-stu-id="7fe7d-106">Parameters</span></span>  

 `pSlotIndex`  
 <span data-ttu-id="7fe7d-107">弄指向局部变量的槽索引的指针。</span><span class="sxs-lookup"><span data-stu-id="7fe7d-107">[out] A pointer to the slot-index of a local variable.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7fe7d-108">返回值</span><span class="sxs-lookup"><span data-stu-id="7fe7d-108">Return Value</span></span>  

 <span data-ttu-id="7fe7d-109">方法返回以下值。</span><span class="sxs-lookup"><span data-stu-id="7fe7d-109">The method returns the following values.</span></span>  
  
|<span data-ttu-id="7fe7d-110">值</span><span class="sxs-lookup"><span data-stu-id="7fe7d-110">Value</span></span>|<span data-ttu-id="7fe7d-111">说明</span><span class="sxs-lookup"><span data-stu-id="7fe7d-111">Description</span></span>|  
|-----------|-----------------|  
|`S_OK`|<span data-ttu-id="7fe7d-112">方法调用返回中的槽索引值 `pSlotIndex` 。</span><span class="sxs-lookup"><span data-stu-id="7fe7d-112">The method call returned a slot-index value in `pSlotIndex`.</span></span>|  
|`E_FAIL`|<span data-ttu-id="7fe7d-113">当前 [ICorDebugVariableHome](icordebugvariablehome-interface.md) 实例表示函数参数。</span><span class="sxs-lookup"><span data-stu-id="7fe7d-113">The current [ICorDebugVariableHome](icordebugvariablehome-interface.md) instance represents a function argument.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7fe7d-114">备注</span><span class="sxs-lookup"><span data-stu-id="7fe7d-114">Remarks</span></span>  

 <span data-ttu-id="7fe7d-115">槽索引可用于检索此局部变量的元数据。</span><span class="sxs-lookup"><span data-stu-id="7fe7d-115">The slot-index can be used to retrieve the metadata for this local variable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7fe7d-116">要求</span><span class="sxs-lookup"><span data-stu-id="7fe7d-116">Requirements</span></span>  

 <span data-ttu-id="7fe7d-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7fe7d-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7fe7d-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7fe7d-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7fe7d-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7fe7d-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7fe7d-120">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7fe7d-120">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7fe7d-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="7fe7d-121">See also</span></span>

- [<span data-ttu-id="7fe7d-122">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="7fe7d-122">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
