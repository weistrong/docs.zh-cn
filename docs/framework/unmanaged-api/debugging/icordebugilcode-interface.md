---
description: 了解详细信息： ICorDebugILCode 接口
title: ICorDebugILCode 接口
ms.date: 03/30/2017
api_name:
- ICorDebugILCode
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 51c4de0c-3813-4142-be25-a85bb84efb90
topic_type:
- apiref
ms.openlocfilehash: 7bf01195f38fd6e046f89e496de3e91e7f8acb33
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803628"
---
# <a name="icordebugilcode-interface"></a><span data-ttu-id="df3e8-103">ICorDebugILCode 接口</span><span class="sxs-lookup"><span data-stu-id="df3e8-103">ICorDebugILCode Interface</span></span>

<span data-ttu-id="df3e8-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="df3e8-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="df3e8-105">表示中间语言 (IL) 代码段。</span><span class="sxs-lookup"><span data-stu-id="df3e8-105">Represents a segment of intermediate language (IL) code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="df3e8-106">方法</span><span class="sxs-lookup"><span data-stu-id="df3e8-106">Methods</span></span>  
  
|<span data-ttu-id="df3e8-107">方法</span><span class="sxs-lookup"><span data-stu-id="df3e8-107">Method</span></span>|<span data-ttu-id="df3e8-108">说明</span><span class="sxs-lookup"><span data-stu-id="df3e8-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="df3e8-109">GetEHClauses 方法</span><span class="sxs-lookup"><span data-stu-id="df3e8-109">GetEHClauses Method</span></span>](icordebugilcode-getehclauses-method.md)|<span data-ttu-id="df3e8-110">返回指向为此 IL 定义的异常处理 (EH) 子句列表的指针。</span><span class="sxs-lookup"><span data-stu-id="df3e8-110">Returns a pointer to a list of exception handling (EH) clauses that are defined for this IL.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="df3e8-111">要求</span><span class="sxs-lookup"><span data-stu-id="df3e8-111">Requirements</span></span>  

 <span data-ttu-id="df3e8-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="df3e8-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="df3e8-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="df3e8-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="df3e8-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="df3e8-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="df3e8-115">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="df3e8-115">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df3e8-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="df3e8-116">See also</span></span>

- [<span data-ttu-id="df3e8-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="df3e8-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="df3e8-118">调试</span><span class="sxs-lookup"><span data-stu-id="df3e8-118">Debugging</span></span>](index.md)
