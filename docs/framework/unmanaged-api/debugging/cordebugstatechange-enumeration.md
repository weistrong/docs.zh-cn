---
description: 了解详细信息： CorDebugStateChange 枚举
title: “Cor调试状态已更改”枚举
ms.date: 02/07/2019
api_name:
- CorDebugStateChange
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 1d4424ab-5143-4e50-a84a-ceeb4ddf3bba
topic_type:
- apiref
ms.openlocfilehash: 1900baa77432daa10d0f1a32dd9cb25198b86ed1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661809"
---
# <a name="cordebugstatechange-enumeration"></a><span data-ttu-id="a4e1a-103">“Cor调试状态已更改”枚举</span><span class="sxs-lookup"><span data-stu-id="a4e1a-103">CorDebugStateChange Enumeration</span></span>

<span data-ttu-id="a4e1a-104">描述基于进程变化必须删除的缓存数据数量。</span><span class="sxs-lookup"><span data-stu-id="a4e1a-104">Describes the amount of cached data that must be discarded based on changes to the process.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e1a-105">语法</span><span class="sxs-lookup"><span data-stu-id="a4e1a-105">Syntax</span></span>

```cpp
typedef enum CorDebugStateChange
{
    PROCESS_RUNNING = 0x0000001,
    FLUSH_ALL       = 0x0000002,
} CorDebugStateChange;
```

## <a name="members"></a><span data-ttu-id="a4e1a-106">成员</span><span class="sxs-lookup"><span data-stu-id="a4e1a-106">Members</span></span>

| <span data-ttu-id="a4e1a-107">成员</span><span class="sxs-lookup"><span data-stu-id="a4e1a-107">Member</span></span>            | <span data-ttu-id="a4e1a-108">说明</span><span class="sxs-lookup"><span data-stu-id="a4e1a-108">Description</span></span>                                                              |
| ----------------- | ------------------------------------------------------------------------ |
| `PROCESS_RUNNING` | <span data-ttu-id="a4e1a-109">该进程向前执行，达到了一种新的内存状态。</span><span class="sxs-lookup"><span data-stu-id="a4e1a-109">The process reached a new memory state via forward execution.</span></span>            |
| `FLUSH_ALL`       | <span data-ttu-id="a4e1a-110">进程的内存可能与以往截然不同。</span><span class="sxs-lookup"><span data-stu-id="a4e1a-110">The process' memory may be arbitrarily different than it was previously.</span></span> |

## <a name="remarks"></a><span data-ttu-id="a4e1a-111">备注</span><span class="sxs-lookup"><span data-stu-id="a4e1a-111">Remarks</span></span>

 <span data-ttu-id="a4e1a-112">`CorDebugStateChange`当调试器 `ProcessStateChanged` 使用[ICorDebugProcess4：:P rocessstatechanged](icordebugprocess4-processstatechanged-method.md)或[ICorDebugProcess6：:P rocessstatechanged](icordebugprocess6-processstatechanged-method.md)调用方法时，枚举的成员作为参数提供。</span><span class="sxs-lookup"><span data-stu-id="a4e1a-112">A member of the `CorDebugStateChange` enumeration is provided as an argument when the debugger calls the `ProcessStateChanged` method either with [ICorDebugProcess4::ProcessStateChanged](icordebugprocess4-processstatechanged-method.md) or [ICorDebugProcess6::ProcessStateChanged](icordebugprocess6-processstatechanged-method.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e1a-113">要求</span><span class="sxs-lookup"><span data-stu-id="a4e1a-113">Requirements</span></span>

 <span data-ttu-id="a4e1a-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a4e1a-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

 <span data-ttu-id="a4e1a-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a4e1a-115">**Header:** CorDebug.idl, CorDebug.h</span></span>

 <span data-ttu-id="a4e1a-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a4e1a-116">**Library:** CorGuids.lib</span></span>

 <span data-ttu-id="a4e1a-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a4e1a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="a4e1a-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="a4e1a-118">See also</span></span>

- [<span data-ttu-id="a4e1a-119">调试枚举</span><span class="sxs-lookup"><span data-stu-id="a4e1a-119">Debugging Enumerations</span></span>](debugging-enumerations.md)
- [<span data-ttu-id="a4e1a-120">调试</span><span class="sxs-lookup"><span data-stu-id="a4e1a-120">Debugging</span></span>](index.md)
