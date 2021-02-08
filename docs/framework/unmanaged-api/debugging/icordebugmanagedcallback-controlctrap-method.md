---
description: 了解详细信息： ICorDebugManagedCallback：： ControlCTrap 方法
title: ICorDebugManagedCallback::ControlCTrap 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.ControlCTrap
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::ControlCTrap
helpviewer_keywords:
- ICorDebugManagedCallback::ControlCTrap method [.NET Framework debugging]
- ControlCTrap method [.NET Framework debugging]
ms.assetid: 0500854e-2121-43d9-a028-64312da35258
topic_type:
- apiref
ms.openlocfilehash: 9fa71dacb20ff6df21d8aabb687c2601f27643c7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791057"
---
# <a name="icordebugmanagedcallbackcontrolctrap-method"></a><span data-ttu-id="fd421-103">ICorDebugManagedCallback::ControlCTrap 方法</span><span class="sxs-lookup"><span data-stu-id="fd421-103">ICorDebugManagedCallback::ControlCTrap Method</span></span>

<span data-ttu-id="fd421-104">通知调试器在被调试的进程中捕获了 CTRL + C。</span><span class="sxs-lookup"><span data-stu-id="fd421-104">Notifies the debugger that a CTRL+C is trapped in the process that is being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd421-105">语法</span><span class="sxs-lookup"><span data-stu-id="fd421-105">Syntax</span></span>  
  
```cpp  
HRESULT ControlCTrap (  
    [in] ICorDebugProcess *pProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fd421-106">参数</span><span class="sxs-lookup"><span data-stu-id="fd421-106">Parameters</span></span>  

 `pProcess`  
 <span data-ttu-id="fd421-107">中指向 ICorDebugProcess 对象的指针，该对象表示在其中捕获 CTRL + C 的进程。</span><span class="sxs-lookup"><span data-stu-id="fd421-107">[in] A pointer to an ICorDebugProcess object that represents the process in which the CTRL+C is trapped.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fd421-108">返回值</span><span class="sxs-lookup"><span data-stu-id="fd421-108">Return Value</span></span>  
  
|<span data-ttu-id="fd421-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="fd421-109">HRESULT</span></span>|<span data-ttu-id="fd421-110">说明</span><span class="sxs-lookup"><span data-stu-id="fd421-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fd421-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd421-111">S_OK</span></span>|<span data-ttu-id="fd421-112">调试器将处理 CTRL + C 陷阱。</span><span class="sxs-lookup"><span data-stu-id="fd421-112">The debugger will handle the CTRL+C trap.</span></span>|  
|<span data-ttu-id="fd421-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="fd421-113">S_FALSE</span></span>|<span data-ttu-id="fd421-114">调试器将不会处理 CTRL + C 陷阱。</span><span class="sxs-lookup"><span data-stu-id="fd421-114">The debugger will not handle the CTRL+C trap.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fd421-115">备注</span><span class="sxs-lookup"><span data-stu-id="fd421-115">Remarks</span></span>  

 <span data-ttu-id="fd421-116">此回调的进程中的所有应用程序域都已停止。</span><span class="sxs-lookup"><span data-stu-id="fd421-116">All application domains within the process are stopped for this callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd421-117">要求</span><span class="sxs-lookup"><span data-stu-id="fd421-117">Requirements</span></span>  

 <span data-ttu-id="fd421-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fd421-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fd421-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fd421-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fd421-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fd421-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fd421-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd421-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd421-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="fd421-122">See also</span></span>

- [<span data-ttu-id="fd421-123">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="fd421-123">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
