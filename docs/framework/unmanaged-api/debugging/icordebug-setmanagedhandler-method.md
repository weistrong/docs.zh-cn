---
description: 了解详细信息： ICorDebug：： SetManagedHandler 方法
title: ICorDebug::SetManagedHandler 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.SetManagedHandler
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::SetManagedHandler
helpviewer_keywords:
- ICorDebug::SetManagedHandler method [.NET Framework debugging]
- SetManagedHandler method [.NET Framework debugging]
ms.assetid: d079131b-685b-4869-95be-826b88d28bd2
topic_type:
- apiref
ms.openlocfilehash: 5817bd39a2c4e7c71dc12ca8d2d9b1263d116ac8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754350"
---
# <a name="icordebugsetmanagedhandler-method"></a><span data-ttu-id="06fad-103">ICorDebug::SetManagedHandler 方法</span><span class="sxs-lookup"><span data-stu-id="06fad-103">ICorDebug::SetManagedHandler Method</span></span>

<span data-ttu-id="06fad-104">指定托管事件的事件处理程序对象。</span><span class="sxs-lookup"><span data-stu-id="06fad-104">Specifies the event handler object for managed events.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06fad-105">语法</span><span class="sxs-lookup"><span data-stu-id="06fad-105">Syntax</span></span>  
  
```cpp  
HRESULT SetManagedHandler (  
    [in] ICorDebugManagedCallback     *pCallback  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="06fad-106">参数</span><span class="sxs-lookup"><span data-stu-id="06fad-106">Parameters</span></span>  

 `pCallback`  
 <span data-ttu-id="06fad-107">中指向 [ICorDebugManagedCallback](icordebugmanagedcallback-interface.md) 对象的指针，该对象为事件处理程序对象。</span><span class="sxs-lookup"><span data-stu-id="06fad-107">[in] A pointer to an [ICorDebugManagedCallback](icordebugmanagedcallback-interface.md) object, which is the event handler object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="06fad-108">备注</span><span class="sxs-lookup"><span data-stu-id="06fad-108">Remarks</span></span>  

 <span data-ttu-id="06fad-109">`SetManagedHandler` 必须在创建时调用。</span><span class="sxs-lookup"><span data-stu-id="06fad-109">`SetManagedHandler` must be called at creation time.</span></span>  
  
 <span data-ttu-id="06fad-110">如果 `ICorDebugManagedCallback` 实现未包含足够的接口来处理要调试的应用程序的调试事件，则将 `SetManagedHandler` 返回 E_NOINTERFACE 的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="06fad-110">If the `ICorDebugManagedCallback` implementation does not contain sufficient interfaces to handle debugging events for the application that is being debugged, `SetManagedHandler` returns an HRESULT of E_NOINTERFACE.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="06fad-111">要求</span><span class="sxs-lookup"><span data-stu-id="06fad-111">Requirements</span></span>  

 <span data-ttu-id="06fad-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="06fad-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="06fad-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="06fad-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="06fad-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="06fad-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="06fad-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="06fad-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06fad-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="06fad-116">See also</span></span>

- [<span data-ttu-id="06fad-117">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="06fad-117">ICorDebug Interface</span></span>](icordebug-interface.md)
