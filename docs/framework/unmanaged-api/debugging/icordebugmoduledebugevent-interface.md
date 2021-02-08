---
description: 了解详细信息： ICorDebugModuleDebugEvent 接口
title: ICorDebugModuleDebugEvent 接口
ms.date: 03/30/2017
ms.assetid: 41950c52-1ac8-4212-b814-c77e20879f91
ms.openlocfilehash: 0c2d43d7b04caeea0407ede23f0df6e278d60c92
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801028"
---
# <a name="icordebugmoduledebugevent-interface"></a><span data-ttu-id="faa54-103">ICorDebugModuleDebugEvent 接口</span><span class="sxs-lookup"><span data-stu-id="faa54-103">ICorDebugModuleDebugEvent Interface</span></span>

<span data-ttu-id="faa54-104">扩展 [ICorDebugDebugEvent](icordebugdebugevent-interface.md) 接口以支持模块级事件。</span><span class="sxs-lookup"><span data-stu-id="faa54-104">Extends the [ICorDebugDebugEvent](icordebugdebugevent-interface.md) interface to support module-level events.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="faa54-105">方法</span><span class="sxs-lookup"><span data-stu-id="faa54-105">Methods</span></span>  
  
|<span data-ttu-id="faa54-106">方法</span><span class="sxs-lookup"><span data-stu-id="faa54-106">Method</span></span>|<span data-ttu-id="faa54-107">说明</span><span class="sxs-lookup"><span data-stu-id="faa54-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="faa54-108">GetModule 方法</span><span class="sxs-lookup"><span data-stu-id="faa54-108">GetModule Method</span></span>](icordebugmoduledebugevent-getmodule-method.md)|<span data-ttu-id="faa54-109">获取刚加载或卸载的合并模块。</span><span class="sxs-lookup"><span data-stu-id="faa54-109">Gets the merged module that was just loaded or unloaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="faa54-110">备注</span><span class="sxs-lookup"><span data-stu-id="faa54-110">Remarks</span></span>  

 <span data-ttu-id="faa54-111">[MODULE_LOADED](cordebugdebugeventkind-enumeration.md)和[MODULE_UNLOADED](cordebugdebugeventkind-enumeration.md)事件类型实现此接口。</span><span class="sxs-lookup"><span data-stu-id="faa54-111">The [MODULE_LOADED](cordebugdebugeventkind-enumeration.md) and [MODULE_UNLOADED](cordebugdebugeventkind-enumeration.md) event types implement this interface.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="faa54-112">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="faa54-112">The interface is available with .NET Native only.</span></span> <span data-ttu-id="faa54-113">尝试调用 `QueryInterface` 来检索接口指针会为 .NET Native 外部的 ICorDebug 方案返回 `E_NOINTERFACE`。</span><span class="sxs-lookup"><span data-stu-id="faa54-113">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="faa54-114">要求</span><span class="sxs-lookup"><span data-stu-id="faa54-114">Requirements</span></span>  

 <span data-ttu-id="faa54-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="faa54-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="faa54-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="faa54-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="faa54-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="faa54-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="faa54-118">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="faa54-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="faa54-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="faa54-119">See also</span></span>

- [<span data-ttu-id="faa54-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="faa54-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="faa54-121">调试</span><span class="sxs-lookup"><span data-stu-id="faa54-121">Debugging</span></span>](index.md)
