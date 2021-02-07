---
description: 了解详细信息： ICorDebugFunction3 接口
title: ICorDebugFunction3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugFunction3
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: b22717b9-ead5-4eea-887e-789b52d613dc
topic_type:
- apiref
ms.openlocfilehash: f6f3ce78fbb0ca7efb6ba6a95da20f8c698b923c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692064"
---
# <a name="icordebugfunction3-interface"></a><span data-ttu-id="ba88f-103">ICorDebugFunction3 接口</span><span class="sxs-lookup"><span data-stu-id="ba88f-103">ICorDebugFunction3 Interface</span></span>

<span data-ttu-id="ba88f-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="ba88f-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="ba88f-105">对 ICorDebugFunction 接口进行逻辑扩展，以提供对 ReJIT 请求中的代码的访问。</span><span class="sxs-lookup"><span data-stu-id="ba88f-105">Logically extends the ICorDebugFunction interface to provide access to code from a ReJIT request.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ba88f-106">方法</span><span class="sxs-lookup"><span data-stu-id="ba88f-106">Methods</span></span>  
  
|<span data-ttu-id="ba88f-107">方法</span><span class="sxs-lookup"><span data-stu-id="ba88f-107">Method</span></span>|<span data-ttu-id="ba88f-108">说明</span><span class="sxs-lookup"><span data-stu-id="ba88f-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ba88f-109">GetActiveReJitRequestILCode 方法</span><span class="sxs-lookup"><span data-stu-id="ba88f-109">GetActiveReJitRequestILCode Method</span></span>](icordebugfunction3-getactiverejitrequestilcode-method.md)|<span data-ttu-id="ba88f-110">获取一个接口指针，该指针指向包含活动 ReJIT 请求中的 IL 的 [ICorDebugILCode](icordebugilcode-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="ba88f-110">Gets an interface pointer to an [ICorDebugILCode](icordebugilcode-interface.md) that contains the IL from an active ReJIT request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ba88f-111">备注</span><span class="sxs-lookup"><span data-stu-id="ba88f-111">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ba88f-112">要求</span><span class="sxs-lookup"><span data-stu-id="ba88f-112">Requirements</span></span>  

 <span data-ttu-id="ba88f-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ba88f-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ba88f-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ba88f-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ba88f-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ba88f-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ba88f-116">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ba88f-116">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ba88f-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="ba88f-117">See also</span></span>

- [<span data-ttu-id="ba88f-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="ba88f-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="ba88f-119">调试</span><span class="sxs-lookup"><span data-stu-id="ba88f-119">Debugging</span></span>](index.md)
- [<span data-ttu-id="ba88f-120">ReJIT： How-To 指南</span><span class="sxs-lookup"><span data-stu-id="ba88f-120">ReJIT: A How-To Guide</span></span>](/archive/blogs/davbr/rejit-a-how-to-guide)
