---
description: 了解详细信息： ICorDebugClass2 接口
title: ICorDebugClass2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugClass2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass2
helpviewer_keywords:
- ICorDebugClass2 interface [.NET Framework debugging]
ms.assetid: 5416de70-43f2-4cdf-a11f-d570759c9c0c
topic_type:
- apiref
ms.openlocfilehash: 80aa8e59ccc774141e7fcea130d1fc6a38fa37da
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711435"
---
# <a name="icordebugclass2-interface"></a><span data-ttu-id="f7be4-103">ICorDebugClass2 接口</span><span class="sxs-lookup"><span data-stu-id="f7be4-103">ICorDebugClass2 Interface</span></span>

<span data-ttu-id="f7be4-104">表示泛型类或具有 <xref:System.Type> 类型的方法参数的类。</span><span class="sxs-lookup"><span data-stu-id="f7be4-104">Represents a generic class or a class with a method parameter of type <xref:System.Type>.</span></span> <span data-ttu-id="f7be4-105">此接口扩展 [ICorDebugClass](icordebugclass-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="f7be4-105">This interface extends [ICorDebugClass](icordebugclass-interface.md).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f7be4-106">方法</span><span class="sxs-lookup"><span data-stu-id="f7be4-106">Methods</span></span>  
  
|<span data-ttu-id="f7be4-107">方法</span><span class="sxs-lookup"><span data-stu-id="f7be4-107">Method</span></span>|<span data-ttu-id="f7be4-108">说明</span><span class="sxs-lookup"><span data-stu-id="f7be4-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f7be4-109">GetParameterizedType 方法</span><span class="sxs-lookup"><span data-stu-id="f7be4-109">GetParameterizedType Method</span></span>](icordebugclass2-getparameterizedtype-method.md)|<span data-ttu-id="f7be4-110">获取此类的类型声明。</span><span class="sxs-lookup"><span data-stu-id="f7be4-110">Gets the type declaration for this class.</span></span>|  
|[<span data-ttu-id="f7be4-111">SetJMCStatus 方法</span><span class="sxs-lookup"><span data-stu-id="f7be4-111">SetJMCStatus Method</span></span>](icordebugclass2-setjmcstatus-method.md)|<span data-ttu-id="f7be4-112">对于此类的每个方法，设置一个值，该值指示该方法是否为用户定义的代码。</span><span class="sxs-lookup"><span data-stu-id="f7be4-112">For each method of this class, sets a value that indicates whether the method is user-defined code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f7be4-113">备注</span><span class="sxs-lookup"><span data-stu-id="f7be4-113">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f7be4-114">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="f7be4-114">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f7be4-115">要求</span><span class="sxs-lookup"><span data-stu-id="f7be4-115">Requirements</span></span>  

 <span data-ttu-id="f7be4-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f7be4-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f7be4-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f7be4-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f7be4-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f7be4-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f7be4-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f7be4-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f7be4-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="f7be4-120">See also</span></span>

- [<span data-ttu-id="f7be4-121">ICorDebugClass 接口</span><span class="sxs-lookup"><span data-stu-id="f7be4-121">ICorDebugClass Interface</span></span>](icordebugclass-interface.md)
- [<span data-ttu-id="f7be4-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="f7be4-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
