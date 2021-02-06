---
description: 了解详细信息： CLRDATA_ADDRESS_RANGE 结构
title: CLRDATA_ADDRESS_RANGE 结构
ms.date: 01/16/2019
api.name:
- CLRDATA_ADDRESS_RANGE Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- CLRDATA_ADDRESS_RANGE Structure
helpviewer.keywords:
- CLRDATA_ADDRESS_RANGE Structure [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 5d671a08064781b71756efc3c753468e6769d4ce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662333"
---
# <a name="clrdata_address_range-structure"></a><span data-ttu-id="a32a7-103">CLRDATA_ADDRESS_RANGE 结构</span><span class="sxs-lookup"><span data-stu-id="a32a7-103">CLRDATA_ADDRESS_RANGE Structure</span></span>

<span data-ttu-id="a32a7-104">定义地址范围。</span><span class="sxs-lookup"><span data-stu-id="a32a7-104">Defines an address range.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="a32a7-105">语法</span><span class="sxs-lookup"><span data-stu-id="a32a7-105">Syntax</span></span>

```cpp
typedef struct
{
    CLRDATA_ADDRESS startAddress;
    CLRDATA_ADDRESS endAddress;
} CLRDATA_ADDRESS_RANGE;
```

## <a name="members"></a><span data-ttu-id="a32a7-106">成员</span><span class="sxs-lookup"><span data-stu-id="a32a7-106">Members</span></span>

| <span data-ttu-id="a32a7-107">成员</span><span class="sxs-lookup"><span data-stu-id="a32a7-107">Member</span></span>         | <span data-ttu-id="a32a7-108">说明</span><span class="sxs-lookup"><span data-stu-id="a32a7-108">Description</span></span>                     |
| -------------- | ------------------------------- |
| `startAddress` | <span data-ttu-id="a32a7-109">范围的起始地址。</span><span class="sxs-lookup"><span data-stu-id="a32a7-109">The start address of the range.</span></span> |
| `endAddress`   | <span data-ttu-id="a32a7-110">范围的结束地址。</span><span class="sxs-lookup"><span data-stu-id="a32a7-110">The end address of the range.</span></span>   |

## <a name="remarks"></a><span data-ttu-id="a32a7-111">备注</span><span class="sxs-lookup"><span data-stu-id="a32a7-111">Remarks</span></span>

<span data-ttu-id="a32a7-112">此结构存在于运行时中，并且不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="a32a7-112">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="a32a7-113">若要使用它，请定义上面指定的结构，其中 `CLRDATA_ADDRESS` 是一个64位无符号整数。</span><span class="sxs-lookup"><span data-stu-id="a32a7-113">To use it, define the structure as specified above, where `CLRDATA_ADDRESS` is a 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="a32a7-114">要求</span><span class="sxs-lookup"><span data-stu-id="a32a7-114">Requirements</span></span>

<span data-ttu-id="a32a7-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a32a7-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="a32a7-116">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="a32a7-116">**Header:** None</span></span>  
<span data-ttu-id="a32a7-117">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="a32a7-117">**Library:** None</span></span>  
<span data-ttu-id="a32a7-118">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="a32a7-118">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="a32a7-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="a32a7-119">See also</span></span>

- [<span data-ttu-id="a32a7-120">调试</span><span class="sxs-lookup"><span data-stu-id="a32a7-120">Debugging</span></span>](index.md)
- [<span data-ttu-id="a32a7-121">调试结构</span><span class="sxs-lookup"><span data-stu-id="a32a7-121">Debugging Structures</span></span>](debugging-structures.md)
