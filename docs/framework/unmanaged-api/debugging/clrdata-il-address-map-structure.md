---
description: 了解详细信息： CLRDATA_IL_ADDRESS_MAP 结构
title: CLRDATA_IL_ADDRESS_MAP 结构
ms.date: 01/16/2019
api.name:
- CLRDATA_IL_ADDRESS_MAP Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- CLRDATA_IL_ADDRESS_MAP Structure
helpviewer.keywords:
- CLRDATA_IL_ADDRESS_MAP Structure [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 02ee14154de0c1609e58cf6a2ad1ca62710567f5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801847"
---
# <a name="clrdata_il_address_map-structure"></a><span data-ttu-id="4fc28-103">CLRDATA_IL_ADDRESS_MAP 结构</span><span class="sxs-lookup"><span data-stu-id="4fc28-103">CLRDATA_IL_ADDRESS_MAP Structure</span></span>

<span data-ttu-id="4fc28-104">定义用于寻址映射的 IL。</span><span class="sxs-lookup"><span data-stu-id="4fc28-104">Defines an IL to address mapping.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="4fc28-105">语法</span><span class="sxs-lookup"><span data-stu-id="4fc28-105">Syntax</span></span>

```cpp
typedef struct
{
    ULONG32 ilOffset;
    CLRDATA_ADDRESS startAddress;
    CLRDATA_ADDRESS endAddress;
    CLRDataSourceType type;
} CLRDATA_IL_ADDRESS_MAP;
```

## <a name="members"></a><span data-ttu-id="4fc28-106">成员</span><span class="sxs-lookup"><span data-stu-id="4fc28-106">Members</span></span>

| <span data-ttu-id="4fc28-107">成员</span><span class="sxs-lookup"><span data-stu-id="4fc28-107">Member</span></span>         | <span data-ttu-id="4fc28-108">说明</span><span class="sxs-lookup"><span data-stu-id="4fc28-108">Description</span></span>                                            |
| -------------- | ------------------------------------------------------ |
| `ilOffset`     | <span data-ttu-id="4fc28-109">所包含的地址范围的 IL 偏移量</span><span class="sxs-lookup"><span data-stu-id="4fc28-109">IL offset for the contained address range</span></span>              |
| `startAddress` | <span data-ttu-id="4fc28-110">范围的起始地址。</span><span class="sxs-lookup"><span data-stu-id="4fc28-110">The start address of the range.</span></span>                        |
| `endAddress`   | <span data-ttu-id="4fc28-111">范围的结束地址。</span><span class="sxs-lookup"><span data-stu-id="4fc28-111">The end address of the range.</span></span>                          |
| `type`         | <span data-ttu-id="4fc28-112">数据的类型。</span><span class="sxs-lookup"><span data-stu-id="4fc28-112">The type of the data.</span></span> <span data-ttu-id="4fc28-113">当前未使用此值</span><span class="sxs-lookup"><span data-stu-id="4fc28-113">This value is currently not used</span></span> |

## <a name="remarks"></a><span data-ttu-id="4fc28-114">备注</span><span class="sxs-lookup"><span data-stu-id="4fc28-114">Remarks</span></span>

<span data-ttu-id="4fc28-115">此结构存在于运行时中，并且不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="4fc28-115">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="4fc28-116">若要使用它，请定义上面指定的结构，其中 `CLRDATA_ADDRESS` 是一个64位无符号整数。</span><span class="sxs-lookup"><span data-stu-id="4fc28-116">To use it, define the structure as specified above, where `CLRDATA_ADDRESS` is a 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fc28-117">要求</span><span class="sxs-lookup"><span data-stu-id="4fc28-117">Requirements</span></span>

<span data-ttu-id="4fc28-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4fc28-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="4fc28-119">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="4fc28-119">**Header:** None</span></span>  
<span data-ttu-id="4fc28-120">**库：** 无 **.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="4fc28-120">**Library:** None **.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="4fc28-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="4fc28-121">See also</span></span>

- [<span data-ttu-id="4fc28-122">CLRDataSourceType 枚举</span><span class="sxs-lookup"><span data-stu-id="4fc28-122">CLRDataSourceType Enumeration</span></span>](clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="4fc28-123">调试</span><span class="sxs-lookup"><span data-stu-id="4fc28-123">Debugging</span></span>](index.md)
- [<span data-ttu-id="4fc28-124">调试结构</span><span class="sxs-lookup"><span data-stu-id="4fc28-124">Debugging Structures</span></span>](debugging-structures.md)
