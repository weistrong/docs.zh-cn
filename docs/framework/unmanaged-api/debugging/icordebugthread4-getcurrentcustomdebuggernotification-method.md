---
description: 了解详细信息： ICorDebugThread4：： GetCurrentCustomDebuggerNotification 方法
title: ICorDebugThread4::GetCurrentCustomDebuggerNotification 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread4.GetCurrentCustomDebuggerNotification Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread4::GetCurrentCustomDebuggerNotification
helpviewer_keywords:
- GetCurrentCustomDebuggerNotification method [.NET Framework debugging]
- ICorDebugThread4::GetCurrentCustomDebuggerNotification method [.NET Framework debugging]
ms.assetid: 57e0f2d2-5f0e-4e2d-99ec-3f26632eb693
topic_type:
- apiref
ms.openlocfilehash: 20d9449e98b9ab91dbdec84ba026e91514d5b3cc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800937"
---
# <a name="icordebugthread4getcurrentcustomdebuggernotification-method"></a><span data-ttu-id="3947b-103">ICorDebugThread4::GetCurrentCustomDebuggerNotification 方法</span><span class="sxs-lookup"><span data-stu-id="3947b-103">ICorDebugThread4::GetCurrentCustomDebuggerNotification Method</span></span>

<span data-ttu-id="3947b-104">获取当前线程上的当前 [ICorDebugManagedCallback3：： CustomNotification](icordebugmanagedcallback3-customnotification-method.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="3947b-104">Gets the current [ICorDebugManagedCallback3::CustomNotification](icordebugmanagedcallback3-customnotification-method.md) object on the current thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="3947b-105">语法</span><span class="sxs-lookup"><span data-stu-id="3947b-105">Syntax</span></span>

```cpp
HRESULT GetCurrentCustomDebuggerNotification(
    [out] ICorDebugValue **ppNotificationObject
    );
```

## <a name="parameters"></a><span data-ttu-id="3947b-106">参数</span><span class="sxs-lookup"><span data-stu-id="3947b-106">Parameters</span></span>

`ppNotificationObject`\
<span data-ttu-id="3947b-107">弄指向 `ICorDebugManagedCallback3::CustomNotification` 当前线程上的当前对象的指针。</span><span class="sxs-lookup"><span data-stu-id="3947b-107">[out] A pointer to the current `ICorDebugManagedCallback3::CustomNotification` object on the current thread.</span></span>

## <a name="remarks"></a><span data-ttu-id="3947b-108">备注</span><span class="sxs-lookup"><span data-stu-id="3947b-108">Remarks</span></span>

<span data-ttu-id="3947b-109">`ppNotificationObject`如果未从回调内调用方法 `ICorDebugManagedCallback3::CustomNotification` ，或者如果不存在当前通知对象，则的值为 null。</span><span class="sxs-lookup"><span data-stu-id="3947b-109">The value of `ppNotificationObject` is null if the method is not called from within a `ICorDebugManagedCallback3::CustomNotification` callback, or if no current notification object exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="3947b-110">要求</span><span class="sxs-lookup"><span data-stu-id="3947b-110">Requirements</span></span>

<span data-ttu-id="3947b-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3947b-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="3947b-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3947b-112">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="3947b-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3947b-113">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="3947b-114">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3947b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="3947b-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="3947b-115">See also</span></span>

- [<span data-ttu-id="3947b-116">ICorDebugThread4 接口</span><span class="sxs-lookup"><span data-stu-id="3947b-116">ICorDebugThread4 Interface</span></span>](icordebugthread4-interface.md)
- [<span data-ttu-id="3947b-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="3947b-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="3947b-118">调试</span><span class="sxs-lookup"><span data-stu-id="3947b-118">Debugging</span></span>](index.md)
