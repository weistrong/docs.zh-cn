---
description: 了解详细信息： ICorDebugManagedCallback：： Break 方法
title: ICorDebugManagedCallback::Break 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.Break
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::Break
helpviewer_keywords:
- Break method [.NET Framework debugging]
- ICorDebugManagedCallback::Break method [.NET Framework debugging]
ms.assetid: 7d78a301-82b3-43b2-9d65-3cda3285ae97
topic_type:
- apiref
ms.openlocfilehash: 2ef273a693291685c4c3a0ce2b20ed45613e3376
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801210"
---
# <a name="icordebugmanagedcallbackbreak-method"></a><span data-ttu-id="e9470-103">ICorDebugManagedCallback::Break 方法</span><span class="sxs-lookup"><span data-stu-id="e9470-103">ICorDebugManagedCallback::Break Method</span></span>

<span data-ttu-id="e9470-104">当 <xref:System.Reflection.Emit.OpCodes.Break> 执行代码流中的指令时，通知调试器。</span><span class="sxs-lookup"><span data-stu-id="e9470-104">Notifies the debugger when a <xref:System.Reflection.Emit.OpCodes.Break> instruction in the code stream is executed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9470-105">语法</span><span class="sxs-lookup"><span data-stu-id="e9470-105">Syntax</span></span>

```cpp
HRESULT Break (
    [in] ICorDebugAppDomain *pAppDomain,
    [in] ICorDebugThread    *thread
);
```

## <a name="parameters"></a><span data-ttu-id="e9470-106">参数</span><span class="sxs-lookup"><span data-stu-id="e9470-106">Parameters</span></span>

`pAppDomain`\
<span data-ttu-id="e9470-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含中断指令的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="e9470-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contains the break instruction.</span></span>

`thread`\
<span data-ttu-id="e9470-108">中指向 ICorDebugThread 对象的指针，该对象表示包含中断指令的线程。</span><span class="sxs-lookup"><span data-stu-id="e9470-108">[in] A pointer to an ICorDebugThread object that represents the thread that contains the break instruction.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9470-109">要求</span><span class="sxs-lookup"><span data-stu-id="e9470-109">Requirements</span></span>

<span data-ttu-id="e9470-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e9470-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="e9470-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e9470-111">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="e9470-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e9470-112">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="e9470-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e9470-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="e9470-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="e9470-114">See also</span></span>

- [<span data-ttu-id="e9470-115">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="e9470-115">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
