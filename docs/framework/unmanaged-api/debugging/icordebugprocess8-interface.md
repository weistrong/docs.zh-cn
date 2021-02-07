---
description: 了解详细信息： ICorDebugProcess8 接口
title: ICorDebugProcess8 接口
ms.date: 03/30/2017
ms.assetid: 7ab1a70f-ec11-46ff-8869-cd8ca679cc51
ms.openlocfilehash: d858470216cfe64c60902836e552f750f4b2d5ec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691284"
---
# <a name="icordebugprocess8-interface"></a><span data-ttu-id="ed91a-103">ICorDebugProcess8 接口</span><span class="sxs-lookup"><span data-stu-id="ed91a-103">ICorDebugProcess8 Interface</span></span>

<span data-ttu-id="ed91a-104">[.NET Framework 4.6 及更高版本中支持]</span><span class="sxs-lookup"><span data-stu-id="ed91a-104">[Supported in the .NET Framework 4.6 and later versions]</span></span>  
  
 <span data-ttu-id="ed91a-105">对 ICorDebugProcess 接口进行逻辑扩展，以启用或禁用某些类型的 [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) 异常回调。</span><span class="sxs-lookup"><span data-stu-id="ed91a-105">Logically extends the ICorDebugProcess interface to enable or disable certain types of [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) exception callbacks.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ed91a-106">方法</span><span class="sxs-lookup"><span data-stu-id="ed91a-106">Methods</span></span>  
  
|<span data-ttu-id="ed91a-107">方法</span><span class="sxs-lookup"><span data-stu-id="ed91a-107">Method</span></span>|<span data-ttu-id="ed91a-108">说明</span><span class="sxs-lookup"><span data-stu-id="ed91a-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ed91a-109">EnableExceptionCallbacksOutsideOfMyCode 方法</span><span class="sxs-lookup"><span data-stu-id="ed91a-109">EnableExceptionCallbacksOutsideOfMyCode Method</span></span>](icordebugprocess8-enableexceptioncallbacksoutsideofmycode-method.md)|<span data-ttu-id="ed91a-110">启用或禁用某些类型的 [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) 异常回调。</span><span class="sxs-lookup"><span data-stu-id="ed91a-110">Enables or disables certain types of [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) exception callbacks.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ed91a-111">备注</span><span class="sxs-lookup"><span data-stu-id="ed91a-111">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ed91a-112">要求</span><span class="sxs-lookup"><span data-stu-id="ed91a-112">Requirements</span></span>  

 <span data-ttu-id="ed91a-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ed91a-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ed91a-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ed91a-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ed91a-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ed91a-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ed91a-116">**.NET Framework 版本：**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ed91a-116">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed91a-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="ed91a-117">See also</span></span>

- [<span data-ttu-id="ed91a-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="ed91a-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="ed91a-119">调试</span><span class="sxs-lookup"><span data-stu-id="ed91a-119">Debugging</span></span>](index.md)
