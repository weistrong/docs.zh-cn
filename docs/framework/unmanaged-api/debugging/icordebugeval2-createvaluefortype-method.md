---
description: 了解详细信息： ICorDebugEval2：： CreateValueForType 方法
title: ICorDebugEval2::CreateValueForType 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval2.CreateValueForType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval2::CreateValueForType
helpviewer_keywords:
- CreateValueForType method [.NET Framework debugging]
- ICorDebugEval2::CreateValueForType method [.NET Framework debugging]
ms.assetid: ea38ae20-7e0a-427a-be77-d78fae719d82
topic_type:
- apiref
ms.openlocfilehash: 2a8cd129d6194a4870817eb64b79606c395cb055
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693871"
---
# <a name="icordebugeval2createvaluefortype-method"></a><span data-ttu-id="eb56a-103">ICorDebugEval2::CreateValueForType 方法</span><span class="sxs-lookup"><span data-stu-id="eb56a-103">ICorDebugEval2::CreateValueForType Method</span></span>

<span data-ttu-id="eb56a-104">获取一个指针，该指针指向指定类型的新 ICorDebugValue，其初始值为零或 null。</span><span class="sxs-lookup"><span data-stu-id="eb56a-104">Gets a pointer to a new ICorDebugValue of the specified type, with an initial value of zero or null.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb56a-105">语法</span><span class="sxs-lookup"><span data-stu-id="eb56a-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateValueForType (  
    [in] ICorDebugType         *pType,  
    [out] ICorDebugValue       **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eb56a-106">参数</span><span class="sxs-lookup"><span data-stu-id="eb56a-106">Parameters</span></span>  

 `pType`  
 <span data-ttu-id="eb56a-107">中指向表示该类型的 ICorDebugType 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="eb56a-107">[in] Pointer to an ICorDebugType object that represents the type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="eb56a-108">弄指向表示值的对象的地址的指针 `ICorDebugValue` 。</span><span class="sxs-lookup"><span data-stu-id="eb56a-108">[out] Pointer to the address of an `ICorDebugValue` object that represents the value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eb56a-109">备注</span><span class="sxs-lookup"><span data-stu-id="eb56a-109">Remarks</span></span>  

 <span data-ttu-id="eb56a-110">`CreateValueForType` 通用化 [ICorDebugEval：： CreateValue](icordebugeval-createvalue-method.md) ，它允许指定任意对象类型，包括构造类型（如） `List<int>` 。</span><span class="sxs-lookup"><span data-stu-id="eb56a-110">`CreateValueForType` generalizes [ICorDebugEval::CreateValue](icordebugeval-createvalue-method.md) by allowing you to specify an arbitrary object type, including constructed types such as `List<int>`.</span></span> <span data-ttu-id="eb56a-111">此方法的唯一目的是生成一个可传递给函数计算的值。</span><span class="sxs-lookup"><span data-stu-id="eb56a-111">The only purpose of this method is to generate a value that can be passed to a function evaluation.</span></span>  
  
 <span data-ttu-id="eb56a-112">类型必须是类或值类型。</span><span class="sxs-lookup"><span data-stu-id="eb56a-112">The type must be a class or a value type.</span></span> <span data-ttu-id="eb56a-113">不能使用此方法创建数组值或字符串值。</span><span class="sxs-lookup"><span data-stu-id="eb56a-113">You cannot use this method to create array values or string values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eb56a-114">要求</span><span class="sxs-lookup"><span data-stu-id="eb56a-114">Requirements</span></span>  

 <span data-ttu-id="eb56a-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="eb56a-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eb56a-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="eb56a-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="eb56a-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eb56a-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eb56a-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eb56a-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
