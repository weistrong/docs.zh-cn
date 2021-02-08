---
description: 了解详细信息： DacpReJitData 结构
title: DacpReJitData 结构
ms.date: 02/01/2019
api.name:
- DacpReJitData Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpReJitData Structure
helpviewer.keywords:
- DacpReJitData Structure [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 8e8d506856dbc6579ac6ea0eee2b2088a980a315
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801431"
---
# <a name="dacprejitdata-structure"></a><span data-ttu-id="e493a-103">DacpReJitData 结构</span><span class="sxs-lookup"><span data-stu-id="e493a-103">DacpReJitData Structure</span></span>

<span data-ttu-id="e493a-104">定义有关给定探查器检测到的方法的基本信息。</span><span class="sxs-lookup"><span data-stu-id="e493a-104">Defines the basic information about a given profiler-instrumented method.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="e493a-105">语法</span><span class="sxs-lookup"><span data-stu-id="e493a-105">Syntax</span></span>

```cpp
struct MSLAYOUT DacpReJitData
{
    enum Flags
    {
        kUnknown,
        kRequested,
        kActive,
        kReverted,
    };

    CLRDATA_ADDRESS                 rejitID;
    Flags                           flags;
    CLRDATA_ADDRESS                 NativeCodeAddr;
};
```

## <a name="members"></a><span data-ttu-id="e493a-106">成员</span><span class="sxs-lookup"><span data-stu-id="e493a-106">Members</span></span>

| <span data-ttu-id="e493a-107">成员</span><span class="sxs-lookup"><span data-stu-id="e493a-107">Member</span></span>           | <span data-ttu-id="e493a-108">说明</span><span class="sxs-lookup"><span data-stu-id="e493a-108">Description</span></span>                                                                                      |
| ---------------- | ------------------------------------------------------------------------------------------------ |
| `rejitID`        | <span data-ttu-id="e493a-109">方法的 ReJit 修订号。</span><span class="sxs-lookup"><span data-stu-id="e493a-109">The ReJit revision number for a method.</span></span>                                                          |
| `flags`          | <span data-ttu-id="e493a-110">一个标志，指示给定版本的该方法的 ReJit 检测的当前状态。</span><span class="sxs-lookup"><span data-stu-id="e493a-110">A flag indicating the current state of the method's ReJit instrumentation for the given version.</span></span> |
| `NativeCodeAddr` | <span data-ttu-id="e493a-111">该方法的 rejitted 实现的基址。</span><span class="sxs-lookup"><span data-stu-id="e493a-111">The base address of the method's rejitted implementation.</span></span>                                         |

## <a name="remarks"></a><span data-ttu-id="e493a-112">备注</span><span class="sxs-lookup"><span data-stu-id="e493a-112">Remarks</span></span>

<span data-ttu-id="e493a-113">此结构存在于运行时中，并且不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="e493a-113">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="e493a-114">若要使用它，请定义上面指定的结构。</span><span class="sxs-lookup"><span data-stu-id="e493a-114">To use it, define the structure as specified above.</span></span> <span data-ttu-id="e493a-115">如果不使用 Microsoft 编译器，还必须使用打包来定义结构 `ms_struct` 。</span><span class="sxs-lookup"><span data-stu-id="e493a-115">The structure must also be defined using `ms_struct` packing if not using the Microsoft compilers.</span></span>

## <a name="requirements"></a><span data-ttu-id="e493a-116">要求</span><span class="sxs-lookup"><span data-stu-id="e493a-116">Requirements</span></span>

<span data-ttu-id="e493a-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e493a-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="e493a-118">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="e493a-118">**Header:** None</span></span>  
<span data-ttu-id="e493a-119">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="e493a-119">**Library:** None</span></span>  
<span data-ttu-id="e493a-120">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="e493a-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="e493a-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="e493a-121">See also</span></span>

- [<span data-ttu-id="e493a-122">调试</span><span class="sxs-lookup"><span data-stu-id="e493a-122">Debugging</span></span>](index.md)
- [<span data-ttu-id="e493a-123">调试结构</span><span class="sxs-lookup"><span data-stu-id="e493a-123">Debugging Structures</span></span>](debugging-structures.md)
