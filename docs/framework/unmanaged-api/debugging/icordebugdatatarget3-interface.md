---
description: 了解详细信息： ICorDebugDataTarget3 接口
title: ICorDebugDataTarget3 接口
ms.date: 03/30/2017
ms.assetid: f477af85-994f-4df0-ae78-404ed252bf49
ms.openlocfilehash: fa786b920d1a2e72dc2a7918e0514773862a0e85
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710434"
---
# <a name="icordebugdatatarget3-interface"></a><span data-ttu-id="c7dcc-103">ICorDebugDataTarget3 接口</span><span class="sxs-lookup"><span data-stu-id="c7dcc-103">ICorDebugDataTarget3 Interface</span></span>

<span data-ttu-id="c7dcc-104">对 [ICorDebugDataTarget](icordebugdatatarget-interface.md) 接口进行逻辑扩展，以提供有关已加载模块的信息。</span><span class="sxs-lookup"><span data-stu-id="c7dcc-104">Logically extends the [ICorDebugDataTarget](icordebugdatatarget-interface.md) interface to provide information about loaded modules.</span></span>  
  
## <a name="method"></a><span data-ttu-id="c7dcc-105">方法</span><span class="sxs-lookup"><span data-stu-id="c7dcc-105">Method</span></span>  
  
|<span data-ttu-id="c7dcc-106">方法</span><span class="sxs-lookup"><span data-stu-id="c7dcc-106">Method</span></span>|<span data-ttu-id="c7dcc-107">说明</span><span class="sxs-lookup"><span data-stu-id="c7dcc-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c7dcc-108">GetLoadedModules 方法</span><span class="sxs-lookup"><span data-stu-id="c7dcc-108">GetLoadedModules Method</span></span>](icordebugdatatarget3-getloadedmodules-method.md)|<span data-ttu-id="c7dcc-109">获取到目前为止已加载的模块的列表。</span><span class="sxs-lookup"><span data-stu-id="c7dcc-109">Gets a list of the modules that have been loaded so far.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c7dcc-110">备注</span><span class="sxs-lookup"><span data-stu-id="c7dcc-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c7dcc-111">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="c7dcc-111">This interface is available with .NET Native only.</span></span> <span data-ttu-id="c7dcc-112">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="c7dcc-112">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c7dcc-113">要求</span><span class="sxs-lookup"><span data-stu-id="c7dcc-113">Requirements</span></span>  

 <span data-ttu-id="c7dcc-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c7dcc-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7dcc-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c7dcc-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c7dcc-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c7dcc-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c7dcc-117">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7dcc-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7dcc-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="c7dcc-118">See also</span></span>

- [<span data-ttu-id="c7dcc-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="c7dcc-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="c7dcc-120">调试</span><span class="sxs-lookup"><span data-stu-id="c7dcc-120">Debugging</span></span>](index.md)
