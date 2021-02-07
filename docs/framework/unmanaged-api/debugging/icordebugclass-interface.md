---
description: 了解详细信息： ICorDebugClass 接口
title: ICorDebugClass 接口
ms.date: 03/30/2017
api_name:
- ICorDebugClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass
helpviewer_keywords:
- ICorDebugClass interface [.NET Framework debugging]
ms.assetid: 03a6facb-f12f-49be-9839-e73b9c791cd5
topic_type:
- apiref
ms.openlocfilehash: 5ded26a8b3a98bd273bbfe1bfa9efd1bb70d5595
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711500"
---
# <a name="icordebugclass-interface"></a><span data-ttu-id="169ee-103">ICorDebugClass 接口</span><span class="sxs-lookup"><span data-stu-id="169ee-103">ICorDebugClass Interface</span></span>

<span data-ttu-id="169ee-104">表示基类型或复杂类型（即用户定义的类型）。</span><span class="sxs-lookup"><span data-stu-id="169ee-104">Represents a type, which can be either basic or complex (that is, user-defined).</span></span> <span data-ttu-id="169ee-105">如果该类型为泛型类型，则 `ICorDebugClass` 表示实例化的泛型类型。</span><span class="sxs-lookup"><span data-stu-id="169ee-105">If the type is generic, `ICorDebugClass` represents the uninstantiated generic type.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="169ee-106">方法</span><span class="sxs-lookup"><span data-stu-id="169ee-106">Methods</span></span>  
  
|<span data-ttu-id="169ee-107">方法</span><span class="sxs-lookup"><span data-stu-id="169ee-107">Method</span></span>|<span data-ttu-id="169ee-108">说明</span><span class="sxs-lookup"><span data-stu-id="169ee-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="169ee-109">GetModule 方法</span><span class="sxs-lookup"><span data-stu-id="169ee-109">GetModule Method</span></span>](icordebugclass-getmodule-method.md)|<span data-ttu-id="169ee-110">获取定义此类的模块。</span><span class="sxs-lookup"><span data-stu-id="169ee-110">Gets the module that defines this class.</span></span>|  
|[<span data-ttu-id="169ee-111">GetStaticFieldValue 方法</span><span class="sxs-lookup"><span data-stu-id="169ee-111">GetStaticFieldValue Method</span></span>](icordebugclass-getstaticfieldvalue-method.md)|<span data-ttu-id="169ee-112">获取指定的静态字段的值。</span><span class="sxs-lookup"><span data-stu-id="169ee-112">Gets the value of the specified static field.</span></span>|  
|[<span data-ttu-id="169ee-113">GetToken 方法</span><span class="sxs-lookup"><span data-stu-id="169ee-113">GetToken Method</span></span>](icordebugclass-gettoken-method.md)|<span data-ttu-id="169ee-114">获取 `TypeDef` 此类的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="169ee-114">Gets the `TypeDef` metadata token for this class.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="169ee-115">备注</span><span class="sxs-lookup"><span data-stu-id="169ee-115">Remarks</span></span>  

 <span data-ttu-id="169ee-116">`ICorDebugClass`接口表示未实例化的泛型类型。</span><span class="sxs-lookup"><span data-stu-id="169ee-116">The `ICorDebugClass` interface represents an uninstantiated generic type.</span></span> <span data-ttu-id="169ee-117">ICorDebugType 接口表示一个实例化的泛型类型。</span><span class="sxs-lookup"><span data-stu-id="169ee-117">The ICorDebugType interface represents an instantiated generic type.</span></span> <span data-ttu-id="169ee-118">例如，将由 `Hashtable<K, V>` 表示 `ICorDebugClass` ，而将由 `Hashtable<Int32, String>` 表示 `ICorDebugType` 。</span><span class="sxs-lookup"><span data-stu-id="169ee-118">For example, `Hashtable<K, V>` would be represented by `ICorDebugClass`, whereas `Hashtable<Int32, String>` would be represented by `ICorDebugType`.</span></span>  
  
 <span data-ttu-id="169ee-119">非泛型类型由 `ICorDebugClass` 和表示 `ICorDebugType` 。</span><span class="sxs-lookup"><span data-stu-id="169ee-119">Non-generic types are represented by both `ICorDebugClass` and `ICorDebugType`.</span></span> <span data-ttu-id="169ee-120">后一种接口在 .NET Framework 版本2.0 中引入，用于处理类型实例化。</span><span class="sxs-lookup"><span data-stu-id="169ee-120">The latter interface was introduced in the .NET Framework version 2.0 to deal with type instantiation.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="169ee-121">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="169ee-121">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="169ee-122">要求</span><span class="sxs-lookup"><span data-stu-id="169ee-122">Requirements</span></span>  

 <span data-ttu-id="169ee-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="169ee-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="169ee-124">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="169ee-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="169ee-125">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="169ee-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="169ee-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="169ee-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="169ee-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="169ee-127">See also</span></span>

- [<span data-ttu-id="169ee-128">调试接口</span><span class="sxs-lookup"><span data-stu-id="169ee-128">Debugging Interfaces</span></span>](debugging-interfaces.md)
