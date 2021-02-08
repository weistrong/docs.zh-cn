---
description: 了解详细信息： ICorDebugInternalFrame 接口
title: ICorDebugInternalFrame 接口
ms.date: 03/30/2017
api_name:
- ICorDebugInternalFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugInternalFrame
helpviewer_keywords:
- ICorDebugInternalFrame interface [.NET Framework debugging]
ms.assetid: bb4772ca-0d54-4185-b738-7a6ffe9ea85a
topic_type:
- apiref
ms.openlocfilehash: 7143f270b97e10fb9664aa7f7387749ddecbbcc5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791122"
---
# <a name="icordebuginternalframe-interface"></a><span data-ttu-id="f867e-103">ICorDebugInternalFrame 接口</span><span class="sxs-lookup"><span data-stu-id="f867e-103">ICorDebugInternalFrame Interface</span></span>

<span data-ttu-id="f867e-104">表示堆栈上的运行时内部帧。</span><span class="sxs-lookup"><span data-stu-id="f867e-104">Represents a runtime-internal frame on the stack.</span></span> <span data-ttu-id="f867e-105">此接口是 ICorDebugFrame 接口的子类。</span><span class="sxs-lookup"><span data-stu-id="f867e-105">This interface is a subclass of the ICorDebugFrame interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f867e-106">方法</span><span class="sxs-lookup"><span data-stu-id="f867e-106">Methods</span></span>  
  
|<span data-ttu-id="f867e-107">方法</span><span class="sxs-lookup"><span data-stu-id="f867e-107">Method</span></span>|<span data-ttu-id="f867e-108">说明</span><span class="sxs-lookup"><span data-stu-id="f867e-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f867e-109">GetFrameType 方法</span><span class="sxs-lookup"><span data-stu-id="f867e-109">GetFrameType Method</span></span>](icordebuginternalframe-getframetype-method.md)|<span data-ttu-id="f867e-110">获取此内部帧的类型。</span><span class="sxs-lookup"><span data-stu-id="f867e-110">Gets the type of this internal frame.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f867e-111">备注</span><span class="sxs-lookup"><span data-stu-id="f867e-111">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f867e-112">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="f867e-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f867e-113">要求</span><span class="sxs-lookup"><span data-stu-id="f867e-113">Requirements</span></span>  

 <span data-ttu-id="f867e-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f867e-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f867e-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f867e-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f867e-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f867e-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f867e-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f867e-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f867e-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="f867e-118">See also</span></span>

- [<span data-ttu-id="f867e-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="f867e-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
