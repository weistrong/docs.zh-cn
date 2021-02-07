---
description: 了解详细信息： ICorDebugEval2 接口
title: ICorDebugEval2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugEval2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval2
helpviewer_keywords:
- ICorDebugEval2 interface [.NET Framework debugging]
ms.assetid: fce34531-2687-406d-9131-d6ad94f2ce0e
topic_type:
- apiref
ms.openlocfilehash: 2c279335bdd30b8dc2698f348d9537443b236a45
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693754"
---
# <a name="icordebugeval2-interface"></a><span data-ttu-id="771db-103">ICorDebugEval2 接口</span><span class="sxs-lookup"><span data-stu-id="771db-103">ICorDebugEval2 Interface</span></span>

<span data-ttu-id="771db-104">扩展 "ICorDebugEval" 以提供对泛型类型的支持。</span><span class="sxs-lookup"><span data-stu-id="771db-104">Extends "ICorDebugEval" to provide support for generic types.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="771db-105">方法</span><span class="sxs-lookup"><span data-stu-id="771db-105">Methods</span></span>  
  
|<span data-ttu-id="771db-106">方法</span><span class="sxs-lookup"><span data-stu-id="771db-106">Method</span></span>|<span data-ttu-id="771db-107">说明</span><span class="sxs-lookup"><span data-stu-id="771db-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="771db-108">CallParameterizedFunction 方法</span><span class="sxs-lookup"><span data-stu-id="771db-108">CallParameterizedFunction Method</span></span>](icordebugeval2-callparameterizedfunction-method.md)|<span data-ttu-id="771db-109">设置对指定的 "ICorDebugFunction" 的调用，该调用可以嵌套在其构造函数采用类型参数的类型内，也可以采用类型参数。</span><span class="sxs-lookup"><span data-stu-id="771db-109">Sets up a call to the specified "ICorDebugFunction", which can be nested inside a type whose constructor takes type parameters, or can itself take type parameters.</span></span>|  
|[<span data-ttu-id="771db-110">CreateValueForType 方法</span><span class="sxs-lookup"><span data-stu-id="771db-110">CreateValueForType Method</span></span>](icordebugeval2-createvaluefortype-method.md)|<span data-ttu-id="771db-111">获取一个指针，该指针指向指定类型的新 "ICorDebugValue"，其初始值为 null 或零。</span><span class="sxs-lookup"><span data-stu-id="771db-111">Gets a pointer to a new "ICorDebugValue" of the specified type, with an initial value of null or zero.</span></span>|  
|[<span data-ttu-id="771db-112">NewParameterizedArray 方法</span><span class="sxs-lookup"><span data-stu-id="771db-112">NewParameterizedArray Method</span></span>](icordebugeval2-newparameterizedarray-method.md)|<span data-ttu-id="771db-113">分配指定元素类型和维度的新数组。</span><span class="sxs-lookup"><span data-stu-id="771db-113">Allocates a new array of the specified element type and dimensions.</span></span>|  
|[<span data-ttu-id="771db-114">NewParameterizedObject 方法</span><span class="sxs-lookup"><span data-stu-id="771db-114">NewParameterizedObject Method</span></span>](icordebugeval2-newparameterizedobject-method.md)|<span data-ttu-id="771db-115">实例化一个新的参数化类型对象，并调用该对象的构造函数方法。</span><span class="sxs-lookup"><span data-stu-id="771db-115">Instantiates a new parameterized type object and calls the object's constructor method.</span></span>|  
|[<span data-ttu-id="771db-116">NewParameterizedObjectNoConstructor 方法</span><span class="sxs-lookup"><span data-stu-id="771db-116">NewParameterizedObjectNoConstructor Method</span></span>](icordebugeval2-newparameterizedobjectnoconstructor-method.md)|<span data-ttu-id="771db-117">实例化指定类的一个新参数化类型对象，而不尝试调用构造函数方法</span><span class="sxs-lookup"><span data-stu-id="771db-117">Instantiates a new parameterized type object of the specified class without attempting to call a constructor method</span></span>|  
|[<span data-ttu-id="771db-118">NewStringWithLength 方法</span><span class="sxs-lookup"><span data-stu-id="771db-118">NewStringWithLength Method</span></span>](icordebugeval2-newstringwithlength-method.md)|<span data-ttu-id="771db-119">使用指定的内容创建指定长度的新字符串。</span><span class="sxs-lookup"><span data-stu-id="771db-119">Creates a new string of the specified length with the specified contents.</span></span>|  
|[<span data-ttu-id="771db-120">RudeAbort 方法</span><span class="sxs-lookup"><span data-stu-id="771db-120">RudeAbort Method</span></span>](icordebugeval2-rudeabort-method.md)|<span data-ttu-id="771db-121">中止此当前正在执行的计算 `ICorDebugEval2` 。</span><span class="sxs-lookup"><span data-stu-id="771db-121">Aborts the computation that this `ICorDebugEval2` is currently performing.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="771db-122">备注</span><span class="sxs-lookup"><span data-stu-id="771db-122">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="771db-123">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="771db-123">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="771db-124">要求</span><span class="sxs-lookup"><span data-stu-id="771db-124">Requirements</span></span>  

 <span data-ttu-id="771db-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="771db-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="771db-126">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="771db-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="771db-127">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="771db-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="771db-128">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="771db-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="771db-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="771db-129">See also</span></span>

- [<span data-ttu-id="771db-130">调试接口</span><span class="sxs-lookup"><span data-stu-id="771db-130">Debugging Interfaces</span></span>](debugging-interfaces.md)
