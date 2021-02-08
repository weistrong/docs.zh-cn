---
description: 了解详细信息： ICorDebugMDA 接口
title: ICorDebugMDA 接口
ms.date: 03/30/2017
api_name:
- ICorDebugMDA
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA
helpviewer_keywords:
- ICorDebugMDA interface [.NET Framework debugging]
ms.assetid: 8ecbb854-295c-4dd4-b9fc-01ebeac46e06
topic_type:
- apiref
ms.openlocfilehash: 8e6e779c58d71b07edc9b63dff72aef728ebe050
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801119"
---
# <a name="icordebugmda-interface"></a><span data-ttu-id="2adf4-103">ICorDebugMDA 接口</span><span class="sxs-lookup"><span data-stu-id="2adf4-103">ICorDebugMDA Interface</span></span>

<span data-ttu-id="2adf4-104">表示托管调试助手 (MDA) 消息。</span><span class="sxs-lookup"><span data-stu-id="2adf4-104">Represents a managed debugging assistant (MDA) message.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2adf4-105">方法</span><span class="sxs-lookup"><span data-stu-id="2adf4-105">Methods</span></span>  
  
|<span data-ttu-id="2adf4-106">方法</span><span class="sxs-lookup"><span data-stu-id="2adf4-106">Method</span></span>|<span data-ttu-id="2adf4-107">说明</span><span class="sxs-lookup"><span data-stu-id="2adf4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2adf4-108">GetDescription 方法</span><span class="sxs-lookup"><span data-stu-id="2adf4-108">GetDescription Method</span></span>](icordebugmda-getdescription-method.md)|<span data-ttu-id="2adf4-109">获取一个字符串，该字符串包含此 MDA 的说明。</span><span class="sxs-lookup"><span data-stu-id="2adf4-109">Gets a string containing a description of this MDA.</span></span>|  
|[<span data-ttu-id="2adf4-110">GetFlags 方法</span><span class="sxs-lookup"><span data-stu-id="2adf4-110">GetFlags Method</span></span>](icordebugmda-getflags-method.md)|<span data-ttu-id="2adf4-111">获取与此 MDA 关联的标志。</span><span class="sxs-lookup"><span data-stu-id="2adf4-111">Gets the flags associated with this MDA.</span></span>|  
|[<span data-ttu-id="2adf4-112">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="2adf4-112">GetName Method</span></span>](icordebugmda-getname-method.md)|<span data-ttu-id="2adf4-113">获取包含此 MDA 的名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="2adf4-113">Gets a string containing the name of this MDA.</span></span>|  
|[<span data-ttu-id="2adf4-114">GetOSThreadId 方法</span><span class="sxs-lookup"><span data-stu-id="2adf4-114">GetOSThreadId Method</span></span>](icordebugmda-getosthreadid-method.md)|<span data-ttu-id="2adf4-115">获取要在其上执行此 MDA 的操作系统线程标识符。</span><span class="sxs-lookup"><span data-stu-id="2adf4-115">Gets the operating system thread identifier upon which this MDA is executing.</span></span>|  
|[<span data-ttu-id="2adf4-116">GetXML 方法</span><span class="sxs-lookup"><span data-stu-id="2adf4-116">GetXML Method</span></span>](icordebugmda-getxml-method.md)|<span data-ttu-id="2adf4-117">获取与此 MDA 关联的完整 XML 流。</span><span class="sxs-lookup"><span data-stu-id="2adf4-117">Gets the full XML stream associated with this MDA.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2adf4-118">备注</span><span class="sxs-lookup"><span data-stu-id="2adf4-118">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="2adf4-119">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="2adf4-119">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2adf4-120">要求</span><span class="sxs-lookup"><span data-stu-id="2adf4-120">Requirements</span></span>  

 <span data-ttu-id="2adf4-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2adf4-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2adf4-122">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2adf4-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2adf4-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2adf4-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2adf4-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2adf4-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2adf4-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="2adf4-125">See also</span></span>

- [<span data-ttu-id="2adf4-126">调试接口</span><span class="sxs-lookup"><span data-stu-id="2adf4-126">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="2adf4-127">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="2adf4-127">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
