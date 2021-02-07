---
description: 了解详细信息： ICorDebugObjectEnum 接口
title: ICorDebugObjectEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugObjectEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectEnum
helpviewer_keywords:
- ICorDebugObjectEnum interface [.NET Framework debugging]
ms.assetid: 9ffb4498-7719-49d3-8890-df2c22248a0c
topic_type:
- apiref
ms.openlocfilehash: d5cd8580bfa81af7d644c2fb11524a43a9062ddf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722225"
---
# <a name="icordebugobjectenum-interface"></a><span data-ttu-id="87ad6-103">ICorDebugObjectEnum 接口</span><span class="sxs-lookup"><span data-stu-id="87ad6-103">ICorDebugObjectEnum Interface</span></span>

<span data-ttu-id="87ad6-104">实现 ICorDebugEnum 方法，并按它们相对虚拟地址 (Rva) 来枚举对象数组。</span><span class="sxs-lookup"><span data-stu-id="87ad6-104">Implements ICorDebugEnum methods, and enumerates arrays of objects by their relative virtual addresses (RVAs).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="87ad6-105">方法</span><span class="sxs-lookup"><span data-stu-id="87ad6-105">Methods</span></span>  
  
|<span data-ttu-id="87ad6-106">方法</span><span class="sxs-lookup"><span data-stu-id="87ad6-106">Method</span></span>|<span data-ttu-id="87ad6-107">说明</span><span class="sxs-lookup"><span data-stu-id="87ad6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="87ad6-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="87ad6-108">Next Method</span></span>](icordebugobjectenum-next-method.md)|<span data-ttu-id="87ad6-109">从当前位置开始，获取枚举中指定数量的对象的 Rva。</span><span class="sxs-lookup"><span data-stu-id="87ad6-109">Gets the RVAs of the specified number of objects from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="87ad6-110">备注</span><span class="sxs-lookup"><span data-stu-id="87ad6-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="87ad6-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="87ad6-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="87ad6-112">要求</span><span class="sxs-lookup"><span data-stu-id="87ad6-112">Requirements</span></span>  

 <span data-ttu-id="87ad6-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="87ad6-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="87ad6-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="87ad6-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="87ad6-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="87ad6-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="87ad6-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="87ad6-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="87ad6-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="87ad6-117">See also</span></span>

- [<span data-ttu-id="87ad6-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="87ad6-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
