---
description: 了解详细信息： ICorDebugChainEnum 接口
title: ICorDebugChainEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugChainEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChainEnum
helpviewer_keywords:
- ICorDebugChainEnum interface [.NET Framework debugging]
ms.assetid: 6639335c-48e1-4e74-a4f3-70a6a0f54af1
topic_type:
- apiref
ms.openlocfilehash: 948bca1e01a49e7cd2e3fbadca7e3957e5ce38c0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661150"
---
# <a name="icordebugchainenum-interface"></a><span data-ttu-id="6590f-103">ICorDebugChainEnum 接口</span><span class="sxs-lookup"><span data-stu-id="6590f-103">ICorDebugChainEnum Interface</span></span>

<span data-ttu-id="6590f-104">实现 ICorDebugEnum 方法，并枚举 ICorDebugChain 数组。</span><span class="sxs-lookup"><span data-stu-id="6590f-104">Implements ICorDebugEnum methods, and enumerates ICorDebugChain arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6590f-105">方法</span><span class="sxs-lookup"><span data-stu-id="6590f-105">Methods</span></span>  
  
|<span data-ttu-id="6590f-106">方法</span><span class="sxs-lookup"><span data-stu-id="6590f-106">Method</span></span>|<span data-ttu-id="6590f-107">说明</span><span class="sxs-lookup"><span data-stu-id="6590f-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6590f-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="6590f-108">Next Method</span></span>](icordebugchainenum-next-method.md)|<span data-ttu-id="6590f-109">`ICorDebugChain`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="6590f-109">Gets the specified number of `ICorDebugChain` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6590f-110">备注</span><span class="sxs-lookup"><span data-stu-id="6590f-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="6590f-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="6590f-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6590f-112">要求</span><span class="sxs-lookup"><span data-stu-id="6590f-112">Requirements</span></span>  

 <span data-ttu-id="6590f-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6590f-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6590f-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6590f-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6590f-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6590f-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6590f-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6590f-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6590f-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="6590f-117">See also</span></span>

- [<span data-ttu-id="6590f-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="6590f-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
