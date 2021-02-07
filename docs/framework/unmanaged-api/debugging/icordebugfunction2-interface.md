---
description: 了解详细信息： ICorDebugFunction2 接口
title: ICorDebugFunction2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugFunction2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction2
helpviewer_keywords:
- ICorDebugFunction2 interface [.NET Framework debugging]
ms.assetid: 2b936bef-9b75-48bf-859f-42e419c65f1c
topic_type:
- apiref
ms.openlocfilehash: e5297d46acb9b174537363fc185fa2d540d55a75
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692191"
---
# <a name="icordebugfunction2-interface"></a><span data-ttu-id="88352-103">ICorDebugFunction2 接口</span><span class="sxs-lookup"><span data-stu-id="88352-103">ICorDebugFunction2 Interface</span></span>

<span data-ttu-id="88352-104">对 ICorDebugFunction 接口进行逻辑扩展，以便为跳过非用户代码仅我的代码逐步调试提供支持。</span><span class="sxs-lookup"><span data-stu-id="88352-104">Logically extends the ICorDebugFunction interface to provide support for Just My Code step-through debugging, which skips non-user code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="88352-105">方法</span><span class="sxs-lookup"><span data-stu-id="88352-105">Methods</span></span>  
  
|<span data-ttu-id="88352-106">方法</span><span class="sxs-lookup"><span data-stu-id="88352-106">Method</span></span>|<span data-ttu-id="88352-107">说明</span><span class="sxs-lookup"><span data-stu-id="88352-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="88352-108">EnumerateNativeCode 方法</span><span class="sxs-lookup"><span data-stu-id="88352-108">EnumerateNativeCode Method</span></span>](icordebugfunction2-enumeratenativecode-method.md)|<span data-ttu-id="88352-109"> (尚未实现。 ) 获取一个指向 ICorDebugCodeEnum 的接口指针，该指针包含此 ICorDebugFunction2 对象引用的函数中的本机代码语句。</span><span class="sxs-lookup"><span data-stu-id="88352-109">(Not yet implemented.) Gets an interface pointer to an ICorDebugCodeEnum that contains the native code statements in the function referenced by this ICorDebugFunction2 object.</span></span>|  
|[<span data-ttu-id="88352-110">GetJMCStatus 方法</span><span class="sxs-lookup"><span data-stu-id="88352-110">GetJMCStatus Method</span></span>](icordebugfunction2-getjmcstatus-method.md)|<span data-ttu-id="88352-111">获取一个值，该值指示此函数是否被标记为 "用户代码"。</span><span class="sxs-lookup"><span data-stu-id="88352-111">Gets a value that indicates whether this function is marked as user code.</span></span>|  
|[<span data-ttu-id="88352-112">GetVersionNumber 方法</span><span class="sxs-lookup"><span data-stu-id="88352-112">GetVersionNumber Method</span></span>](icordebugfunction2-getversionnumber-method.md)|<span data-ttu-id="88352-113">获取此函数的 "编辑并继续" 版本。</span><span class="sxs-lookup"><span data-stu-id="88352-113">Gets the Edit and Continue version of this function.</span></span>|  
|[<span data-ttu-id="88352-114">SetJMCStatus 方法</span><span class="sxs-lookup"><span data-stu-id="88352-114">SetJMCStatus Method</span></span>](icordebugfunction2-setjmcstatus-method.md)|<span data-ttu-id="88352-115">将此函数标记仅我的代码单步执行。</span><span class="sxs-lookup"><span data-stu-id="88352-115">Marks this function for Just My Code stepping.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="88352-116">备注</span><span class="sxs-lookup"><span data-stu-id="88352-116">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="88352-117">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="88352-117">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="88352-118">要求</span><span class="sxs-lookup"><span data-stu-id="88352-118">Requirements</span></span>  

 <span data-ttu-id="88352-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="88352-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="88352-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="88352-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="88352-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="88352-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="88352-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="88352-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="88352-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="88352-123">See also</span></span>

- [<span data-ttu-id="88352-124">调试接口</span><span class="sxs-lookup"><span data-stu-id="88352-124">Debugging Interfaces</span></span>](debugging-interfaces.md)
