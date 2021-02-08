---
description: 了解详细信息： ICorDebugVariableHomeEnum 接口
title: ICorDebugVariableHomeEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHomeEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHomeEnum
helpviewer_keywords:
- ICorDebugVariableHomeEnum interface [.NET Framework debugging]
ms.assetid: c312ae6d-c8dc-48d6-9f1e-ead515c88fdf
topic_type:
- apiref
ms.openlocfilehash: c56c68a6b5f9d329fe8af23f47b40fa629bfe3ba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790615"
---
# <a name="icordebugvariablehomeenum-interface"></a><span data-ttu-id="c7cf0-103">ICorDebugVariableHomeEnum 接口</span><span class="sxs-lookup"><span data-stu-id="c7cf0-103">ICorDebugVariableHomeEnum Interface</span></span>

<span data-ttu-id="c7cf0-104">提供对函数中的局部变量和参数的枚举器。</span><span class="sxs-lookup"><span data-stu-id="c7cf0-104">Provides an enumerator to the local variables and arguments in a function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c7cf0-105">方法</span><span class="sxs-lookup"><span data-stu-id="c7cf0-105">Methods</span></span>  
  
|<span data-ttu-id="c7cf0-106">方法</span><span class="sxs-lookup"><span data-stu-id="c7cf0-106">Method</span></span>|<span data-ttu-id="c7cf0-107">说明</span><span class="sxs-lookup"><span data-stu-id="c7cf0-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c7cf0-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="c7cf0-108">Next Method</span></span>](icordebugvariablehomeenum-next-method.md)|<span data-ttu-id="c7cf0-109">获取指定数量的 [ICorDebugVariableHome](icordebugvariablehome-interface.md) 实例，其中包含有关函数中的局部变量和参数的信息。</span><span class="sxs-lookup"><span data-stu-id="c7cf0-109">Gets the specified number of [ICorDebugVariableHome](icordebugvariablehome-interface.md) instances that contain information about the local variables and arguments in a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c7cf0-110">备注</span><span class="sxs-lookup"><span data-stu-id="c7cf0-110">Remarks</span></span>  

 <span data-ttu-id="c7cf0-111">`ICorDebugVariableHomeEnum`接口实现 ICorDebugEnum 接口。</span><span class="sxs-lookup"><span data-stu-id="c7cf0-111">The `ICorDebugVariableHomeEnum` interface implements the ICorDebugEnum interface.</span></span>  
  
 <span data-ttu-id="c7cf0-112">`ICorDebugVariableHomeEnum`实例通过调用[ICorDebugCode4：： EnumerateVariableHomes](icordebugcode4-enumeratevariablehomes-method.md)方法，使用[ICorDebugVariableHome](icordebugvariablehome-interface.md)实例进行填充。</span><span class="sxs-lookup"><span data-stu-id="c7cf0-112">An `ICorDebugVariableHomeEnum` instance is populated with [ICorDebugVariableHome](icordebugvariablehome-interface.md) instances by calling the [ICorDebugCode4::EnumerateVariableHomes](icordebugcode4-enumeratevariablehomes-method.md) method.</span></span> <span data-ttu-id="c7cf0-113">集合中的每个 [ICorDebugVariableHome](icordebugvariablehome-interface.md) 实例都表示函数中的局部变量或自变量。</span><span class="sxs-lookup"><span data-stu-id="c7cf0-113">Each [ICorDebugVariableHome](icordebugvariablehome-interface.md) instance in the collection represents a local variable or argument in a function.</span></span> <span data-ttu-id="c7cf0-114">可以通过调用[ICorDebugVariableHomeEnum：： Next](icordebugvariablehomeenum-next-method.md)方法来枚举集合中的[ICorDebugVariableHome](icordebugvariablehome-interface.md)对象。</span><span class="sxs-lookup"><span data-stu-id="c7cf0-114">The  [ICorDebugVariableHome](icordebugvariablehome-interface.md) objects in the collection can be enumerated by calling the [ICorDebugVariableHomeEnum::Next](icordebugvariablehomeenum-next-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c7cf0-115">要求</span><span class="sxs-lookup"><span data-stu-id="c7cf0-115">Requirements</span></span>  

 <span data-ttu-id="c7cf0-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c7cf0-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7cf0-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c7cf0-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c7cf0-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c7cf0-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c7cf0-119">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7cf0-119">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7cf0-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="c7cf0-120">See also</span></span>

- [<span data-ttu-id="c7cf0-121">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="c7cf0-121">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
- [<span data-ttu-id="c7cf0-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="c7cf0-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
