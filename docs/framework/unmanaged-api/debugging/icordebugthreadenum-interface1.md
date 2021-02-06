---
description: 了解详细信息： ICorDebugThreadEnum 接口
title: ICorDebugThreadEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugThreadEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThreadEnum
helpviewer_keywords:
- ICorDebugThreadEnum interface [.NET Framework debugging]
ms.assetid: 796de687-7dd4-4b7b-a10b-8bf22dc7779f
topic_type:
- apiref
ms.openlocfilehash: 088b9bd56ae0049ad5f287b07cd2857f70a496c3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658472"
---
# <a name="icordebugthreadenum-interface"></a><span data-ttu-id="e2363-103">ICorDebugThreadEnum 接口</span><span class="sxs-lookup"><span data-stu-id="e2363-103">ICorDebugThreadEnum Interface</span></span>

<span data-ttu-id="e2363-104">实现 ICorDebugEnum 方法并枚举 ICorDebugThread 数组。</span><span class="sxs-lookup"><span data-stu-id="e2363-104">Implements ICorDebugEnum methods and enumerates ICorDebugThread arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e2363-105">方法</span><span class="sxs-lookup"><span data-stu-id="e2363-105">Methods</span></span>  
  
|<span data-ttu-id="e2363-106">方法</span><span class="sxs-lookup"><span data-stu-id="e2363-106">Method</span></span>|<span data-ttu-id="e2363-107">说明</span><span class="sxs-lookup"><span data-stu-id="e2363-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e2363-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="e2363-108">Next Method</span></span>](icordebugthreadenum-next-method.md)|<span data-ttu-id="e2363-109">`ICorDebugThread`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="e2363-109">Gets the specified number of `ICorDebugThread` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e2363-110">备注</span><span class="sxs-lookup"><span data-stu-id="e2363-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="e2363-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="e2363-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e2363-112">要求</span><span class="sxs-lookup"><span data-stu-id="e2363-112">Requirements</span></span>  

 <span data-ttu-id="e2363-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e2363-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e2363-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e2363-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e2363-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e2363-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e2363-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e2363-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2363-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="e2363-117">See also</span></span>

- [<span data-ttu-id="e2363-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="e2363-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
