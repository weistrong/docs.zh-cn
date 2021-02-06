---
description: 了解详细信息： ICorDebugProcess5：： GetTypeFields 方法
title: ICorDebugProcess5::GetTypeFields 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.GetTypeFields
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::GetTypeFields
helpviewer_keywords:
- GetTypeFields method, ICorDebugProcess5 interface [.NET Framework debugging]
- ICorDebugProcess5::GetTypeFields method [.NET Framework debugging]
ms.assetid: 6a0ad3ee-dacb-47e9-abae-4536bcc4804b
topic_type:
- apiref
ms.openlocfilehash: bdbb0be76400262d83876b9fc37cc4f00eb34e43
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649812"
---
# <a name="icordebugprocess5gettypefields-method"></a><span data-ttu-id="aca32-103">ICorDebugProcess5::GetTypeFields 方法</span><span class="sxs-lookup"><span data-stu-id="aca32-103">ICorDebugProcess5::GetTypeFields Method</span></span>

<span data-ttu-id="aca32-104">提供有关属于类型的字段的信息。</span><span class="sxs-lookup"><span data-stu-id="aca32-104">Provides information about the fields that belong to a type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aca32-105">语法</span><span class="sxs-lookup"><span data-stu-id="aca32-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTypeFields(  
    [in] COR_TYPEID id,  
    [in] ULONG32 celt,  
    [out] COR_FIELD fields[],
    [out] ULONG32 *pceltNeeded  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="aca32-106">参数</span><span class="sxs-lookup"><span data-stu-id="aca32-106">Parameters</span></span>  

 `id`  
 <span data-ttu-id="aca32-107">中检索其字段信息的类型的标识符。</span><span class="sxs-lookup"><span data-stu-id="aca32-107">[in] The identifier of the type whose field information is retrieved.</span></span>  
  
 `celt`  
 <span data-ttu-id="aca32-108">中要检索其字段信息的 [COR_FIELD](cor-field-structure.md) 对象的数量。</span><span class="sxs-lookup"><span data-stu-id="aca32-108">[in] The number of [COR_FIELD](cor-field-structure.md) objects whose field information is to be retrieved.</span></span>  
  
 `fields`  
 <span data-ttu-id="aca32-109">弄 [COR_FIELD](cor-field-structure.md) 对象的数组，这些对象提供有关属于类型的字段的信息。</span><span class="sxs-lookup"><span data-stu-id="aca32-109">[out] An array of [COR_FIELD](cor-field-structure.md) objects that provide information about the fields that belong to the type.</span></span>  
  
 `pceltNeeded`  
 <span data-ttu-id="aca32-110">弄一个指针，指向中包含的 [COR_FIELD](cor-field-structure.md) 对象的数量 `fields` 。</span><span class="sxs-lookup"><span data-stu-id="aca32-110">[out] A pointer to the number of [COR_FIELD](cor-field-structure.md) objects included in `fields`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="aca32-111">备注</span><span class="sxs-lookup"><span data-stu-id="aca32-111">Remarks</span></span>  

 <span data-ttu-id="aca32-112">`celt`参数，该参数指定方法用来填充字段信息的字段数量 `fields` ，应与字段的值相对应 `COR_TYPE_LAYOUT::numFields` 。</span><span class="sxs-lookup"><span data-stu-id="aca32-112">The `celt` parameter, which specifies the number of fields whose field information the method uses to populate `fields`, should correspond to the value of the `COR_TYPE_LAYOUT::numFields` field.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aca32-113">要求</span><span class="sxs-lookup"><span data-stu-id="aca32-113">Requirements</span></span>  

 <span data-ttu-id="aca32-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="aca32-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aca32-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="aca32-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="aca32-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aca32-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="aca32-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aca32-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aca32-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="aca32-118">See also</span></span>

- [<span data-ttu-id="aca32-119">ICorDebugProcess5 接口</span><span class="sxs-lookup"><span data-stu-id="aca32-119">ICorDebugProcess5 Interface</span></span>](icordebugprocess5-interface.md)
- [<span data-ttu-id="aca32-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="aca32-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
