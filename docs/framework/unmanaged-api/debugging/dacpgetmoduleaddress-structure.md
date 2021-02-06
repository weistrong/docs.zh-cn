---
description: 了解详细信息： DacpGetModuleAddress 结构
title: DacpGetModuleAddress 结构
ms.date: 01/16/2019
api.name:
- DacpGetModuleAddress Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpGetModuleAddress Structure
helpviewer.keywords:
- DacpGetModuleAddress Structure [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 3de76cc4f15bffd35d7a43ae25a313eb2fe59b82
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661592"
---
# <a name="dacpgetmoduleaddress-structure"></a><span data-ttu-id="d044f-103">DacpGetModuleAddress 结构</span><span class="sxs-lookup"><span data-stu-id="d044f-103">DacpGetModuleAddress Structure</span></span>

<span data-ttu-id="d044f-104">定义模块地址请求的容器。</span><span class="sxs-lookup"><span data-stu-id="d044f-104">Defines the container for a module address request.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="d044f-105">语法</span><span class="sxs-lookup"><span data-stu-id="d044f-105">Syntax</span></span>

```cpp
struct DacpGetModuleAddress
{
    CLRDATA_ADDRESS ModulePtr;
};
```

## <a name="members"></a><span data-ttu-id="d044f-106">成员</span><span class="sxs-lookup"><span data-stu-id="d044f-106">Members</span></span>

| <span data-ttu-id="d044f-107">成员</span><span class="sxs-lookup"><span data-stu-id="d044f-107">Member</span></span>      | <span data-ttu-id="d044f-108">说明</span><span class="sxs-lookup"><span data-stu-id="d044f-108">Description</span></span>                |
| ----------- | -------------------------- |
| `ModulePtr` | <span data-ttu-id="d044f-109">指向模块的指针。</span><span class="sxs-lookup"><span data-stu-id="d044f-109">The pointer to the module.</span></span> |

## <a name="methods"></a><span data-ttu-id="d044f-110">方法</span><span class="sxs-lookup"><span data-stu-id="d044f-110">Methods</span></span>

| <span data-ttu-id="d044f-111">方法</span><span class="sxs-lookup"><span data-stu-id="d044f-111">Method</span></span>                                                                                               | <span data-ttu-id="d044f-112">说明</span><span class="sxs-lookup"><span data-stu-id="d044f-112">Description</span></span>                                                                    |
| ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| [<span data-ttu-id="d044f-113">请求</span><span class="sxs-lookup"><span data-stu-id="d044f-113">Request</span></span>](dacpgetmoduleaddress-request-method.md) | <span data-ttu-id="d044f-114">执行从给定的运行时结构填充结构的请求。</span><span class="sxs-lookup"><span data-stu-id="d044f-114">Performs a request to populate the structure from the given runtime structure.</span></span> |

## <a name="remarks"></a><span data-ttu-id="d044f-115">备注</span><span class="sxs-lookup"><span data-stu-id="d044f-115">Remarks</span></span>

<span data-ttu-id="d044f-116">此结构存在于运行时中，并且不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="d044f-116">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="d044f-117">若要使用它，请定义上面指定的结构，其中 `CLRDATA_ADDRESS` 是一个64位无符号整数。</span><span class="sxs-lookup"><span data-stu-id="d044f-117">To use it, define the structure as specified above, where `CLRDATA_ADDRESS` is a 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d044f-118">要求</span><span class="sxs-lookup"><span data-stu-id="d044f-118">Requirements</span></span>

<span data-ttu-id="d044f-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d044f-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="d044f-120">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="d044f-120">**Header:** None</span></span>  
<span data-ttu-id="d044f-121">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="d044f-121">**Library:** None</span></span>  
<span data-ttu-id="d044f-122">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d044f-122">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="d044f-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="d044f-123">See also</span></span>

- [<span data-ttu-id="d044f-124">调试</span><span class="sxs-lookup"><span data-stu-id="d044f-124">Debugging</span></span>](index.md)
- [<span data-ttu-id="d044f-125">调试结构</span><span class="sxs-lookup"><span data-stu-id="d044f-125">Debugging Structures</span></span>](debugging-structures.md)
