---
description: 了解详细信息： ICorDebugBlockingObjectEnum 接口
title: ICorDebugBlockingObjectEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugBlockingObjectEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBlockingObjectEnum
helpviewer_keywords:
- ICorDebugBlockingObjectEnum interface [.NET Framework debugging]
ms.assetid: 208e5c2d-3f3f-404e-8b3c-7cccc14ddb16
topic_type:
- apiref
ms.openlocfilehash: 4f28039cb8a9bdcb376a9acf22572d29e41a2adf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754064"
---
# <a name="icordebugblockingobjectenum-interface"></a><span data-ttu-id="3c016-103">ICorDebugBlockingObjectEnum 接口</span><span class="sxs-lookup"><span data-stu-id="3c016-103">ICorDebugBlockingObjectEnum Interface</span></span>

<span data-ttu-id="3c016-104">为 [CorDebugBlockingObject](cordebugblockingobject-structure.md) 结构的列表提供枚举器。</span><span class="sxs-lookup"><span data-stu-id="3c016-104">Provides an enumerator for a list of [CorDebugBlockingObject](cordebugblockingobject-structure.md) structures.</span></span> <span data-ttu-id="3c016-105">此接口是 ICorDebugEnum 接口的子类。</span><span class="sxs-lookup"><span data-stu-id="3c016-105">This interface is a subclass of the ICorDebugEnum interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3c016-106">方法</span><span class="sxs-lookup"><span data-stu-id="3c016-106">Methods</span></span>  
  
|<span data-ttu-id="3c016-107">方法</span><span class="sxs-lookup"><span data-stu-id="3c016-107">Method</span></span>|<span data-ttu-id="3c016-108">说明</span><span class="sxs-lookup"><span data-stu-id="3c016-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3c016-109">下一方法</span><span class="sxs-lookup"><span data-stu-id="3c016-109">Next Method</span></span>](icordebugblockingobjectenum-next-method.md)|<span data-ttu-id="3c016-110">枚举 [CorDebugBlockingObject](cordebugblockingobject-structure.md) 结构的列表。</span><span class="sxs-lookup"><span data-stu-id="3c016-110">Enumerates through a list of [CorDebugBlockingObject](cordebugblockingobject-structure.md) structures.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3c016-111">备注</span><span class="sxs-lookup"><span data-stu-id="3c016-111">Remarks</span></span>  

 <span data-ttu-id="3c016-112">每个 `CorDebugBlockingObject` 结构均表示一个阻塞线程的对象。</span><span class="sxs-lookup"><span data-stu-id="3c016-112">Each `CorDebugBlockingObject` structure represents an object that is blocking a thread.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3c016-113">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="3c016-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c016-114">要求</span><span class="sxs-lookup"><span data-stu-id="3c016-114">Requirements</span></span>  

 <span data-ttu-id="3c016-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3c016-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c016-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3c016-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3c016-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3c016-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3c016-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c016-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c016-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="3c016-119">See also</span></span>

- [<span data-ttu-id="3c016-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="3c016-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="3c016-121">调试</span><span class="sxs-lookup"><span data-stu-id="3c016-121">Debugging</span></span>](index.md)
