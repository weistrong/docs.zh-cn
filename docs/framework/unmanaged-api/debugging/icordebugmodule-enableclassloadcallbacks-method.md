---
description: 了解详细信息： ICorDebugModule：： EnableClassLoadCallbacks 方法
title: ICorDebugModule::EnableClassLoadCallbacks 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.EnableClassLoadCallbacks
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::EnableClassLoadCallbacks
helpviewer_keywords:
- ICorDebugModule::EnableClassLoadCallbacks method [.NET Framework debugging]
- EnableClassLoadCallbacks method [.NET Framework debugging]
ms.assetid: 78dad5e4-8e2e-400f-bec3-92ff0205cd82
topic_type:
- apiref
ms.openlocfilehash: 16516cceae9a10288f8660fa69d8e0c018953777
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801080"
---
# <a name="icordebugmoduleenableclassloadcallbacks-method"></a><span data-ttu-id="f0ed4-103">ICorDebugModule::EnableClassLoadCallbacks 方法</span><span class="sxs-lookup"><span data-stu-id="f0ed4-103">ICorDebugModule::EnableClassLoadCallbacks Method</span></span>

<span data-ttu-id="f0ed4-104">控制是否为此模块调用 [ICorDebugManagedCallback：： LoadClass](icordebugmanagedcallback-loadclass-method.md) 和 [ICorDebugManagedCallback：： UnloadClass](icordebugmanagedcallback-unloadclass-method.md) 回调。</span><span class="sxs-lookup"><span data-stu-id="f0ed4-104">Controls whether the [ICorDebugManagedCallback::LoadClass](icordebugmanagedcallback-loadclass-method.md) and [ICorDebugManagedCallback::UnloadClass](icordebugmanagedcallback-unloadclass-method.md) callbacks are called for this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0ed4-105">语法</span><span class="sxs-lookup"><span data-stu-id="f0ed4-105">Syntax</span></span>  
  
```cpp  
HRESULT EnableClassLoadCallbacks(  
    [in] BOOL bClassLoadCallbacks  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f0ed4-106">参数</span><span class="sxs-lookup"><span data-stu-id="f0ed4-106">Parameters</span></span>  

 `bClassLoadCallbacks`  
 <span data-ttu-id="f0ed4-107">中将此值设置为 `true` ，以使公共语言运行时 (CLR) `ICorDebugManagedCallback::LoadClass` `ICorDebugManagedCallback::UnloadClass` 在其关联事件发生时调用和方法。</span><span class="sxs-lookup"><span data-stu-id="f0ed4-107">[in] Set this value to `true` to enable the common language runtime (CLR) to call the `ICorDebugManagedCallback::LoadClass` and `ICorDebugManagedCallback::UnloadClass` methods when their associated events occur.</span></span>  
  
 <span data-ttu-id="f0ed4-108">默认值为 `false` 非动态模块。</span><span class="sxs-lookup"><span data-stu-id="f0ed4-108">The default value is `false` for non-dynamic modules.</span></span> <span data-ttu-id="f0ed4-109">`true`对于动态模块，值始终为，且不能更改。</span><span class="sxs-lookup"><span data-stu-id="f0ed4-109">The value is always `true` for dynamic modules and cannot be changed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f0ed4-110">备注</span><span class="sxs-lookup"><span data-stu-id="f0ed4-110">Remarks</span></span>  

 <span data-ttu-id="f0ed4-111">`ICorDebugManagedCallback::LoadClass`和 `ICorDebugManagedCallback::UnloadClass` 回调对于动态模块始终处于启用状态，并且不能禁用。</span><span class="sxs-lookup"><span data-stu-id="f0ed4-111">The `ICorDebugManagedCallback::LoadClass` and `ICorDebugManagedCallback::UnloadClass` callbacks are always enabled for dynamic modules and cannot be disabled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0ed4-112">要求</span><span class="sxs-lookup"><span data-stu-id="f0ed4-112">Requirements</span></span>  

 <span data-ttu-id="f0ed4-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f0ed4-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0ed4-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f0ed4-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f0ed4-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f0ed4-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f0ed4-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0ed4-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0ed4-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="f0ed4-117">See also</span></span>
