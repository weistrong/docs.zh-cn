---
description: 了解详细信息： ICorDebugBoxValue 接口
title: ICorDebugBoxValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugBoxValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBoxValue
helpviewer_keywords:
- ICorDebugBoxValue interface [.NET Framework debugging]
ms.assetid: 3d3ae7e2-97d4-46de-a2c3-cb78f3490f9d
topic_type:
- apiref
ms.openlocfilehash: 86a985d3cbb8330efdef1d6636f91b64c3f78bc6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711929"
---
# <a name="icordebugboxvalue-interface"></a><span data-ttu-id="b55d1-103">ICorDebugBoxValue 接口</span><span class="sxs-lookup"><span data-stu-id="b55d1-103">ICorDebugBoxValue Interface</span></span>

<span data-ttu-id="b55d1-104">表示装箱值类对象的 "ICorDebugHeapValue" 的子类。</span><span class="sxs-lookup"><span data-stu-id="b55d1-104">A subclass of "ICorDebugHeapValue" that represents a boxed value class object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b55d1-105">方法</span><span class="sxs-lookup"><span data-stu-id="b55d1-105">Methods</span></span>  
  
|<span data-ttu-id="b55d1-106">方法</span><span class="sxs-lookup"><span data-stu-id="b55d1-106">Method</span></span>|<span data-ttu-id="b55d1-107">说明</span><span class="sxs-lookup"><span data-stu-id="b55d1-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b55d1-108">GetObject 方法</span><span class="sxs-lookup"><span data-stu-id="b55d1-108">GetObject Method</span></span>](icordebugboxvalue-getobject-method.md)|<span data-ttu-id="b55d1-109">获取指向装箱的 "ICorDebugObjectValue" 实例的接口指针。</span><span class="sxs-lookup"><span data-stu-id="b55d1-109">Gets an interface pointer to the boxed "ICorDebugObjectValue" instance.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b55d1-110">备注</span><span class="sxs-lookup"><span data-stu-id="b55d1-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b55d1-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="b55d1-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b55d1-112">要求</span><span class="sxs-lookup"><span data-stu-id="b55d1-112">Requirements</span></span>  

 <span data-ttu-id="b55d1-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b55d1-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b55d1-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b55d1-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b55d1-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b55d1-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b55d1-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b55d1-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b55d1-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="b55d1-117">See also</span></span>

- [<span data-ttu-id="b55d1-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="b55d1-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
