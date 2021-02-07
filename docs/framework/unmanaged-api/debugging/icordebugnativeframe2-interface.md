---
description: 了解详细信息： ICorDebugNativeFrame2 接口
title: ICorDebugNativeFrame2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame2
helpviewer_keywords:
- ICorDebugNativeFrame2 interface [.NET Framework debugging]
ms.assetid: 52a80838-af36-4399-bc97-d8a4c6d76df2
topic_type:
- apiref
ms.openlocfilehash: 9ed0e20bb29bef3b210258956ebecb1ee7a96df8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722342"
---
# <a name="icordebugnativeframe2-interface"></a><span data-ttu-id="df1c4-103">ICorDebugNativeFrame2 接口</span><span class="sxs-lookup"><span data-stu-id="df1c4-103">ICorDebugNativeFrame2 Interface</span></span>

<span data-ttu-id="df1c4-104">提供用于测试子帧与父帧关系的方法。</span><span class="sxs-lookup"><span data-stu-id="df1c4-104">Provides methods that test for child and parent frame relationships.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="df1c4-105">方法</span><span class="sxs-lookup"><span data-stu-id="df1c4-105">Methods</span></span>  
  
|<span data-ttu-id="df1c4-106">方法</span><span class="sxs-lookup"><span data-stu-id="df1c4-106">Method</span></span>|<span data-ttu-id="df1c4-107">说明</span><span class="sxs-lookup"><span data-stu-id="df1c4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="df1c4-108">IsChild 方法</span><span class="sxs-lookup"><span data-stu-id="df1c4-108">IsChild Method</span></span>](icordebugnativeframe2-ischild-method.md)|<span data-ttu-id="df1c4-109">确定当前帧是否为子框架。</span><span class="sxs-lookup"><span data-stu-id="df1c4-109">Determines whether the current frame is a child frame.</span></span>|  
|[<span data-ttu-id="df1c4-110">IsMatchingParentFrame 方法</span><span class="sxs-lookup"><span data-stu-id="df1c4-110">IsMatchingParentFrame Method</span></span>](icordebugnativeframe2-ismatchingparentframe-method.md)|<span data-ttu-id="df1c4-111">确定指定的帧是否为当前帧的父级。</span><span class="sxs-lookup"><span data-stu-id="df1c4-111">Determines whether the specified frame is the parent of the current frame.</span></span>|  
|[<span data-ttu-id="df1c4-112">GetStackParameterSize 方法</span><span class="sxs-lookup"><span data-stu-id="df1c4-112">GetStackParameterSize Method</span></span>](icordebugnativeframe2-getstackparametersize-method.md)|<span data-ttu-id="df1c4-113">返回 x86 操作系统上堆栈上的参数的累积大小。</span><span class="sxs-lookup"><span data-stu-id="df1c4-113">Returns the cumulative size of the parameters on the stack on x86 operating systems.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="df1c4-114">备注</span><span class="sxs-lookup"><span data-stu-id="df1c4-114">Remarks</span></span>  

 <span data-ttu-id="df1c4-115">此接口以逻辑方式扩展了 "ICorDebugNativeFrame" 接口。</span><span class="sxs-lookup"><span data-stu-id="df1c4-115">This interface logically extends the "ICorDebugNativeFrame" interface.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="df1c4-116">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="df1c4-116">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="df1c4-117">要求</span><span class="sxs-lookup"><span data-stu-id="df1c4-117">Requirements</span></span>  

 <span data-ttu-id="df1c4-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="df1c4-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="df1c4-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="df1c4-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="df1c4-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="df1c4-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="df1c4-121">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="df1c4-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df1c4-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="df1c4-122">See also</span></span>

- [<span data-ttu-id="df1c4-123">调试接口</span><span class="sxs-lookup"><span data-stu-id="df1c4-123">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="df1c4-124">调试</span><span class="sxs-lookup"><span data-stu-id="df1c4-124">Debugging</span></span>](index.md)
