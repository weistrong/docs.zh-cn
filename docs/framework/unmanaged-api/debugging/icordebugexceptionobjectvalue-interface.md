---
description: 了解详细信息： ICorDebugExceptionObjectValue 接口
title: ICorDebugExceptionObjectValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugExceptionObjectValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugExceptionObjectValue
helpviewer_keywords:
- ICorDebugExceptionObjectValue interface [.NET Framework debugging]
ms.assetid: 43416dd5-8892-4106-9f59-f9143b19ddb4
topic_type:
- apiref
ms.openlocfilehash: 67672f9921bab31019a42b742480176e6d0bf3d4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693195"
---
# <a name="icordebugexceptionobjectvalue-interface"></a><span data-ttu-id="f7dd8-103">ICorDebugExceptionObjectValue 接口</span><span class="sxs-lookup"><span data-stu-id="f7dd8-103">ICorDebugExceptionObjectValue Interface</span></span>

<span data-ttu-id="f7dd8-104">扩展 "ICorDebugObjectValue" 接口，以提供来自托管异常对象的堆栈跟踪信息。</span><span class="sxs-lookup"><span data-stu-id="f7dd8-104">Extends the "ICorDebugObjectValue" interface to provide stack trace information from a managed exception object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f7dd8-105">方法</span><span class="sxs-lookup"><span data-stu-id="f7dd8-105">Methods</span></span>  
  
|<span data-ttu-id="f7dd8-106">方法</span><span class="sxs-lookup"><span data-stu-id="f7dd8-106">Method</span></span>|<span data-ttu-id="f7dd8-107">说明</span><span class="sxs-lookup"><span data-stu-id="f7dd8-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f7dd8-108">EnumerateExceptionCallStack 方法</span><span class="sxs-lookup"><span data-stu-id="f7dd8-108">EnumerateExceptionCallStack Method</span></span>](icordebugexceptionobjectvalue-enumerateexceptioncallstack-method.md)|<span data-ttu-id="f7dd8-109">获取一个枚举器，该枚举器指向嵌入到异常对象中的调用堆栈。</span><span class="sxs-lookup"><span data-stu-id="f7dd8-109">Gets an enumerator to the call stack embedded in an exception object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f7dd8-110">备注</span><span class="sxs-lookup"><span data-stu-id="f7dd8-110">Remarks</span></span>  

 <span data-ttu-id="f7dd8-111">`QueryInterface`对于派生自的托管对象，对的调用将成功 <xref:System.Exception?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="f7dd8-111">The call to `QueryInterface` will succeed for managed objects that derive from <xref:System.Exception?displayProperty=nameWithType>.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f7dd8-112">要求</span><span class="sxs-lookup"><span data-stu-id="f7dd8-112">Requirements</span></span>  

 <span data-ttu-id="f7dd8-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f7dd8-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f7dd8-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f7dd8-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f7dd8-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f7dd8-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f7dd8-116">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f7dd8-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f7dd8-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="f7dd8-117">See also</span></span>

- [<span data-ttu-id="f7dd8-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="f7dd8-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="f7dd8-119">调试</span><span class="sxs-lookup"><span data-stu-id="f7dd8-119">Debugging</span></span>](index.md)
