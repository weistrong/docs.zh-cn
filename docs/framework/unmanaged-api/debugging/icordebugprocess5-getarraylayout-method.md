---
description: 了解详细信息： ICorDebugProcess5：： GetArrayLayout 方法
title: ICorDebugProcess5::GetArrayLayout 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.GetArrayLayout
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::GetArrayLayout
helpviewer_keywords:
- ICorDebugProcess5::GetArrayLayout method [.NET Framework debugging]
- GetArrayLayout method, ICorDebugProcess5 interface [.NET Framework debugging]
ms.assetid: 9a7393b9-9735-43c6-8616-afb103c432fd
topic_type:
- apiref
ms.openlocfilehash: c82b296da3a367f5307240225a560af67a56c866
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746394"
---
# <a name="icordebugprocess5getarraylayout-method"></a><span data-ttu-id="91ff1-103">ICorDebugProcess5::GetArrayLayout 方法</span><span class="sxs-lookup"><span data-stu-id="91ff1-103">ICorDebugProcess5::GetArrayLayout Method</span></span>

<span data-ttu-id="91ff1-104">提供有关数组类型布局的信息。</span><span class="sxs-lookup"><span data-stu-id="91ff1-104">Provides information about the layout of array types.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91ff1-105">语法</span><span class="sxs-lookup"><span data-stu-id="91ff1-105">Syntax</span></span>  
  
```cpp  
HRESULT GetArrayLayout(    [in] COR_TYPEID id,     [out] COR_ARRAY_LAYOUT *pLayout);  
```  
  
## <a name="parameters"></a><span data-ttu-id="91ff1-106">参数</span><span class="sxs-lookup"><span data-stu-id="91ff1-106">Parameters</span></span>  

 `id`  
 <span data-ttu-id="91ff1-107">中一个 [COR_TYPEID](cor-typeid-structure.md) 标记，它指定需要其布局的数组。</span><span class="sxs-lookup"><span data-stu-id="91ff1-107">[in] A [COR_TYPEID](cor-typeid-structure.md) token that specifies the array whose layout is desired.</span></span>  
  
 `pLayout`  
 <span data-ttu-id="91ff1-108">弄指向 [COR_ARRAY_LAYOUT](cor-array-layout-structure.md) 结构的指针，该结构包含有关内存中数组的布局的信息。</span><span class="sxs-lookup"><span data-stu-id="91ff1-108">[out] A pointer to a [COR_ARRAY_LAYOUT](cor-array-layout-structure.md) structure that contains information about the layout of the array in memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="91ff1-109">备注</span><span class="sxs-lookup"><span data-stu-id="91ff1-109">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="91ff1-110">要求</span><span class="sxs-lookup"><span data-stu-id="91ff1-110">Requirements</span></span>  

 <span data-ttu-id="91ff1-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="91ff1-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="91ff1-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="91ff1-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="91ff1-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="91ff1-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="91ff1-114">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="91ff1-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="91ff1-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="91ff1-115">See also</span></span>

- [<span data-ttu-id="91ff1-116">ICorDebugProcess5 接口</span><span class="sxs-lookup"><span data-stu-id="91ff1-116">ICorDebugProcess5 Interface</span></span>](icordebugprocess5-interface.md)
- [<span data-ttu-id="91ff1-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="91ff1-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
