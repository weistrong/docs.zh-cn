---
description: 了解详细信息： ICorDebugAssembly2 接口
title: ICorDebugAssembly2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly2
helpviewer_keywords:
- ICorDebugAssembly2 interface [.NET Framework debugging]
ms.assetid: c0766e29-e573-4f9a-a928-167d1de5aa7e
topic_type:
- apiref
ms.openlocfilehash: 2a2d035329ba66153bfee83daa9501581f32842f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754116"
---
# <a name="icordebugassembly2-interface"></a><span data-ttu-id="4b6eb-103">ICorDebugAssembly2 接口</span><span class="sxs-lookup"><span data-stu-id="4b6eb-103">ICorDebugAssembly2 Interface</span></span>

<span data-ttu-id="4b6eb-104">表示一个程序集。</span><span class="sxs-lookup"><span data-stu-id="4b6eb-104">Represents an assembly.</span></span> <span data-ttu-id="4b6eb-105">此接口是 ICorDebugAssembly 接口的扩展。</span><span class="sxs-lookup"><span data-stu-id="4b6eb-105">This interface is an extension of the ICorDebugAssembly interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4b6eb-106">方法</span><span class="sxs-lookup"><span data-stu-id="4b6eb-106">Methods</span></span>  
  
|<span data-ttu-id="4b6eb-107">方法</span><span class="sxs-lookup"><span data-stu-id="4b6eb-107">Method</span></span>|<span data-ttu-id="4b6eb-108">说明</span><span class="sxs-lookup"><span data-stu-id="4b6eb-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4b6eb-109">IsFullyTrusted 方法</span><span class="sxs-lookup"><span data-stu-id="4b6eb-109">IsFullyTrusted Method</span></span>](icordebugassembly2-isfullytrusted-method.md)|<span data-ttu-id="4b6eb-110">获取一个值，该值指示运行时安全系统是否已向程序集授予完全信任。</span><span class="sxs-lookup"><span data-stu-id="4b6eb-110">Gets a value that indicates whether the assembly has been granted full trust by the runtime security system.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4b6eb-111">备注</span><span class="sxs-lookup"><span data-stu-id="4b6eb-111">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="4b6eb-112">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="4b6eb-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4b6eb-113">要求</span><span class="sxs-lookup"><span data-stu-id="4b6eb-113">Requirements</span></span>  

 <span data-ttu-id="4b6eb-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4b6eb-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4b6eb-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4b6eb-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4b6eb-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4b6eb-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4b6eb-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4b6eb-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b6eb-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="4b6eb-118">See also</span></span>

- [<span data-ttu-id="4b6eb-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="4b6eb-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
