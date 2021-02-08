---
description: 了解详细信息： ICorDebugType 接口
title: ICorDebugType 接口
ms.date: 03/30/2017
api_name:
- ICorDebugType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType
helpviewer_keywords:
- ICorDebugType interface [.NET Framework debugging]
ms.assetid: 94e02e31-67ea-4b00-8148-a46740a4571d
topic_type:
- apiref
ms.openlocfilehash: 4cd668263906ef21e1bb665795425ca3a239c2bd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800885"
---
# <a name="icordebugtype-interface"></a><span data-ttu-id="100c8-103">ICorDebugType 接口</span><span class="sxs-lookup"><span data-stu-id="100c8-103">ICorDebugType Interface</span></span>

<span data-ttu-id="100c8-104">表示基本或复杂 (的类型，即用户定义的) 。</span><span class="sxs-lookup"><span data-stu-id="100c8-104">Represents a type, either basic or complex (that is, user-defined).</span></span> <span data-ttu-id="100c8-105">如果该类型是泛型类型，则 `ICorDebugType` 表示未实例化的泛型类型。</span><span class="sxs-lookup"><span data-stu-id="100c8-105">If the type is generic, `ICorDebugType` represents the instantiated generic type.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="100c8-106">方法</span><span class="sxs-lookup"><span data-stu-id="100c8-106">Methods</span></span>  
  
|<span data-ttu-id="100c8-107">方法</span><span class="sxs-lookup"><span data-stu-id="100c8-107">Method</span></span>|<span data-ttu-id="100c8-108">说明</span><span class="sxs-lookup"><span data-stu-id="100c8-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="100c8-109">EnumerateTypeParameters 方法</span><span class="sxs-lookup"><span data-stu-id="100c8-109">EnumerateTypeParameters Method</span></span>](icordebugtype-enumeratetypeparameters-method.md)|<span data-ttu-id="100c8-110">获取一个接口指针，该指针指向引用 <xref:System.Type> 此所引用类的泛型参数的 ICorDebugTypeEnum `ICorDebugType` 。</span><span class="sxs-lookup"><span data-stu-id="100c8-110">Gets an interface pointer to an ICorDebugTypeEnum that references the generic <xref:System.Type> parameters of the class referenced by this `ICorDebugType`.</span></span>|  
|[<span data-ttu-id="100c8-111">GetBase 方法</span><span class="sxs-lookup"><span data-stu-id="100c8-111">GetBase Method</span></span>](icordebugtype-getbase-method.md)|<span data-ttu-id="100c8-112">获取一个接口指针，该指针指向 `ICorDebugType` 引用此引用的类 `ICorDebugType` （如果存在此类）的基类。</span><span class="sxs-lookup"><span data-stu-id="100c8-112">Gets an interface pointer to an `ICorDebugType` that references the base class of the class referenced by this `ICorDebugType`, if one exists.</span></span>|  
|[<span data-ttu-id="100c8-113">GetClass 方法</span><span class="sxs-lookup"><span data-stu-id="100c8-113">GetClass Method</span></span>](icordebugtype-getclass-method.md)|<span data-ttu-id="100c8-114">获取一个接口指针，该指针指向引用此的类型化构造函数的 ICorDebugClass `ICorDebugType` 。</span><span class="sxs-lookup"><span data-stu-id="100c8-114">Gets an interface pointer to an ICorDebugClass that references the typed constructor of this `ICorDebugType`.</span></span>|  
|[<span data-ttu-id="100c8-115">GetFirstTypeParameter 方法</span><span class="sxs-lookup"><span data-stu-id="100c8-115">GetFirstTypeParameter Method</span></span>](icordebugtype-getfirsttypeparameter-method.md)|<span data-ttu-id="100c8-116">获取一个接口指针 `ICorDebugType` ，该指针指向引用此引用的类的构造函数的第一个泛型 <xref:System.Type> 参数 `ICorDebugType` 。</span><span class="sxs-lookup"><span data-stu-id="100c8-116">Gets an interface pointer to an `ICorDebugType` that references the first generic <xref:System.Type> parameter for the constructor of the class referenced by this `ICorDebugType`.</span></span>|  
|[<span data-ttu-id="100c8-117">GetRank 方法</span><span class="sxs-lookup"><span data-stu-id="100c8-117">GetRank Method</span></span>](icordebugtype-getrank-method.md)|<span data-ttu-id="100c8-118">获取数组类型中的维度数。</span><span class="sxs-lookup"><span data-stu-id="100c8-118">Gets the number of dimensions in an array type.</span></span>|  
|[<span data-ttu-id="100c8-119">GetStaticFieldValue 方法</span><span class="sxs-lookup"><span data-stu-id="100c8-119">GetStaticFieldValue Method</span></span>](icordebugtype-getstaticfieldvalue-method.md)|<span data-ttu-id="100c8-120">获取一个指向 ICorDebugValue 的接口指针，该指针包含指定的堆栈帧中指定字段标记所引用的静态字段的值。</span><span class="sxs-lookup"><span data-stu-id="100c8-120">Gets an interface pointer to an ICorDebugValue that contains the value of the static field referenced by the specified field token in the specified stack frame.</span></span>|  
|[<span data-ttu-id="100c8-121">GetType 方法</span><span class="sxs-lookup"><span data-stu-id="100c8-121">GetType Method</span></span>](icordebugtype-gettype-method.md)|<span data-ttu-id="100c8-122">获取一个 CorElementType 值，该值描述此所引用的公共语言运行时的本机类型 <xref:System.Type> `ICorDebugType` 。</span><span class="sxs-lookup"><span data-stu-id="100c8-122">Gets a CorElementType value that describes the native type of the common language runtime <xref:System.Type> referenced by this `ICorDebugType`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="100c8-123">备注</span><span class="sxs-lookup"><span data-stu-id="100c8-123">Remarks</span></span>  

 <span data-ttu-id="100c8-124">如果类型为泛型，则 `ICorDebugClass` 表示未实例化的类型。</span><span class="sxs-lookup"><span data-stu-id="100c8-124">If the type is generic, `ICorDebugClass` represents the uninstantiated type.</span></span> <span data-ttu-id="100c8-125">`ICorDebugType`接口表示一个实例化的泛型类型。</span><span class="sxs-lookup"><span data-stu-id="100c8-125">The `ICorDebugType` interface represents an instantiated generic type.</span></span> <span data-ttu-id="100c8-126">例如，Hashtable 由 \<K, V> 表示 `ICorDebugClass` ，而哈希表将由 \<Int32, String> 表示 `ICorDebugType` 。</span><span class="sxs-lookup"><span data-stu-id="100c8-126">For example, Hashtable\<K, V> would be represented by `ICorDebugClass`, whereas Hashtable\<Int32, String> would be represented by `ICorDebugType`.</span></span>  
  
 <span data-ttu-id="100c8-127">非泛型类型由 `ICorDebugClass` 和表示 `ICorDebugType` 。</span><span class="sxs-lookup"><span data-stu-id="100c8-127">Non-generic types are represented by both `ICorDebugClass` and `ICorDebugType`.</span></span> <span data-ttu-id="100c8-128">后一种接口在 .NET Framework 版本2.0 中引入，用于处理类型实例化。</span><span class="sxs-lookup"><span data-stu-id="100c8-128">The latter interface was introduced in the .NET Framework version 2.0 to deal with type instantiation.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="100c8-129">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="100c8-129">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="100c8-130">要求</span><span class="sxs-lookup"><span data-stu-id="100c8-130">Requirements</span></span>  

 <span data-ttu-id="100c8-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="100c8-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="100c8-132">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="100c8-132">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="100c8-133">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="100c8-133">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="100c8-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="100c8-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="100c8-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="100c8-135">See also</span></span>

- [<span data-ttu-id="100c8-136">调试接口</span><span class="sxs-lookup"><span data-stu-id="100c8-136">Debugging Interfaces</span></span>](debugging-interfaces.md)
