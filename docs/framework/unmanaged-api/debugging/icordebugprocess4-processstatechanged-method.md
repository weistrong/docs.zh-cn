---
description: 了解详细信息： ICorDebugProcess4：:P rocessStateChanged 方法
title: ICorDebugProcess4：:P rocessStateChanged 方法
ms.date: 02/07/2019
api_name:
- ICorDebugProcess4::ProcessStateChanged
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess4::ProcessStateChanged
helpviewer_keywords:
- ICorDebugProcess4::ProcessStateChanged method [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 35a76b3c6dd9b37d3f06f23bc2ffea82f125a29e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746446"
---
# <a name="icordebugprocess4processstatechanged-method"></a><span data-ttu-id="84758-103">ICorDebugProcess4：:P rocessStateChanged 方法</span><span class="sxs-lookup"><span data-stu-id="84758-103">ICorDebugProcess4::ProcessStateChanged Method</span></span>

<span data-ttu-id="84758-104">通知 ICorDebug 管道进程外调试器正在继续执行调试对象的执行。</span><span class="sxs-lookup"><span data-stu-id="84758-104">Notifies the ICorDebug pipeline that the out of process debugger is continuing the debugee's execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="84758-105">语法</span><span class="sxs-lookup"><span data-stu-id="84758-105">Syntax</span></span>

```cpp
HRESULT ProcessStateChanged(
    [in] CorDebugStateChange change
);
```

## <a name="parameters"></a><span data-ttu-id="84758-106">参数</span><span class="sxs-lookup"><span data-stu-id="84758-106">Parameters</span></span>

 `eChange`\
<span data-ttu-id="84758-107">中描述进程的执行状态更改的 [CorDebugStateChange 枚举](cordebugstatechange-enumeration.md) 的成员。</span><span class="sxs-lookup"><span data-stu-id="84758-107">[in] A member of the [CorDebugStateChange enumeration](cordebugstatechange-enumeration.md) describing a change in the process's execution state.</span></span>

## <a name="remarks"></a><span data-ttu-id="84758-108">备注</span><span class="sxs-lookup"><span data-stu-id="84758-108">Remarks</span></span>

<span data-ttu-id="84758-109">提供的方法是接口的一部分 `ICorDebugProcess4` ，并且对应于虚拟方法表的第四个槽。</span><span class="sxs-lookup"><span data-stu-id="84758-109">The provided method is part of the `ICorDebugProcess4` interface and corresponds to the fourth slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="84758-110">要求</span><span class="sxs-lookup"><span data-stu-id="84758-110">Requirements</span></span>

 <span data-ttu-id="84758-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="84758-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

 <span data-ttu-id="84758-112">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="84758-112">**Header:** None</span></span>

 <span data-ttu-id="84758-113">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="84758-113">**Library:** None</span></span>

 <span data-ttu-id="84758-114">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="84758-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="84758-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="84758-115">See also</span></span>

- [<span data-ttu-id="84758-116">ICorDebugProcess4 接口</span><span class="sxs-lookup"><span data-stu-id="84758-116">ICorDebugProcess4 Interface</span></span>](icordebugprocess4-interface.md)
- [<span data-ttu-id="84758-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="84758-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="84758-118">调试</span><span class="sxs-lookup"><span data-stu-id="84758-118">Debugging</span></span>](index.md)
