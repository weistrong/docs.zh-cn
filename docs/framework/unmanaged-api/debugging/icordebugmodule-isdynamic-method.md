---
description: 了解详细信息： ICorDebugModule：： IsDynamic 方法
title: ICorDebugModule::IsDynamic 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.IsDynamic
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::IsDynamic
helpviewer_keywords:
- IsDynamic method [.NET Framework debugging]
- ICorDebugModule::IsDynamic method [.NET Framework debugging]
ms.assetid: 5eefe716-5025-4a4c-970c-c823cdc7bb87
topic_type:
- apiref
ms.openlocfilehash: 06ecb7aaffbe73da29bbdbba9446839db54c58c3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660097"
---
# <a name="icordebugmoduleisdynamic-method"></a><span data-ttu-id="93ee7-103">ICorDebugModule::IsDynamic 方法</span><span class="sxs-lookup"><span data-stu-id="93ee7-103">ICorDebugModule::IsDynamic Method</span></span>

<span data-ttu-id="93ee7-104">获取一个值，该值指示此模块是否为动态模块。</span><span class="sxs-lookup"><span data-stu-id="93ee7-104">Gets a value that indicates whether this module is dynamic.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93ee7-105">语法</span><span class="sxs-lookup"><span data-stu-id="93ee7-105">Syntax</span></span>  
  
```cpp  
HRESULT IsDynamic(  
    [out] BOOL *pDynamic  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="93ee7-106">参数</span><span class="sxs-lookup"><span data-stu-id="93ee7-106">Parameters</span></span>  

 `pDynamic`  
 <span data-ttu-id="93ee7-107">[out] `true` 如果此模块是动态的，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="93ee7-107">[out] `true` if this module is dynamic; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="93ee7-108">备注</span><span class="sxs-lookup"><span data-stu-id="93ee7-108">Remarks</span></span>  

 <span data-ttu-id="93ee7-109">即使在模块加载后，动态模块也可以添加新类和删除现有类。</span><span class="sxs-lookup"><span data-stu-id="93ee7-109">A dynamic module can add new classes and delete existing classes even after the module has been loaded.</span></span> <span data-ttu-id="93ee7-110">添加或删除类时， [ICorDebugManagedCallback：： LoadClass](icordebugmanagedcallback-loadclass-method.md) 和 [ICorDebugManagedCallback：： UnloadClass](icordebugmanagedcallback-unloadclass-method.md) 回调会通知调试器。</span><span class="sxs-lookup"><span data-stu-id="93ee7-110">The [ICorDebugManagedCallback::LoadClass](icordebugmanagedcallback-loadclass-method.md) and [ICorDebugManagedCallback::UnloadClass](icordebugmanagedcallback-unloadclass-method.md) callbacks inform the debugger when a class has been added or deleted.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="93ee7-111">要求</span><span class="sxs-lookup"><span data-stu-id="93ee7-111">Requirements</span></span>  

 <span data-ttu-id="93ee7-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="93ee7-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="93ee7-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="93ee7-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="93ee7-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="93ee7-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="93ee7-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="93ee7-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
