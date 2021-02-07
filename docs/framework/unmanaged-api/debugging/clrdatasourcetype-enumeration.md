---
description: 了解详细信息： CLRDataSourceType 枚举
title: CLRDataSourceType 枚举
ms.date: 01/16/2019
api.name:
- CLRDataSourceType Enumeration
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- CLRDataSourceType Enumeration
helpviewer.keywords:
- CLRDataSourceType Enumeration [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 06590e21aa4cdf6e89977a79da36a413d5ff4f1c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747236"
---
# <a name="clrdatasourcetype-enumeration"></a><span data-ttu-id="6dc4d-103">CLRDataSourceType 枚举</span><span class="sxs-lookup"><span data-stu-id="6dc4d-103">CLRDataSourceType Enumeration</span></span>

<span data-ttu-id="6dc4d-104">提供 CLRDATA_IL_ADDRESS_MAP 结构使用的值。</span><span class="sxs-lookup"><span data-stu-id="6dc4d-104">Provides values that are used by the CLRDATA_IL_ADDRESS_MAP structure.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="6dc4d-105">语法</span><span class="sxs-lookup"><span data-stu-id="6dc4d-105">Syntax</span></span>

```cpp
typedef enum
{
    CLRDATA_SOURCE_TYPE_INVALID        = 0x00, // To indicate that nothing else applies
} CLRDataSourceType;
```

## <a name="members"></a><span data-ttu-id="6dc4d-106">成员</span><span class="sxs-lookup"><span data-stu-id="6dc4d-106">Members</span></span>

| <span data-ttu-id="6dc4d-107">成员</span><span class="sxs-lookup"><span data-stu-id="6dc4d-107">Member</span></span>                        | <span data-ttu-id="6dc4d-108">说明</span><span class="sxs-lookup"><span data-stu-id="6dc4d-108">Description</span></span>                           |
| ----------------------------- | ------------------------------------- |
| `CLRDATA_SOURCE_TYPE_INVALID` | <span data-ttu-id="6dc4d-109">指示无其他应用</span><span class="sxs-lookup"><span data-stu-id="6dc4d-109">To indicate that nothing else applies</span></span> |

## <a name="remarks"></a><span data-ttu-id="6dc4d-110">备注</span><span class="sxs-lookup"><span data-stu-id="6dc4d-110">Remarks</span></span>

<span data-ttu-id="6dc4d-111">此枚举位于运行时中，并且不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="6dc4d-111">This enumeration lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="6dc4d-112">若要使用它，请在代码中定义上面定义的枚举。</span><span class="sxs-lookup"><span data-stu-id="6dc4d-112">To use it, define an enumeration as defined above in your code.</span></span> <span data-ttu-id="6dc4d-113">这也会化名为， `CLRDATA_ENUM` 如 [常用数据类型](../common-data-types-unmanaged-api-reference.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="6dc4d-113">This is also aliased to `CLRDATA_ENUM` as mentioned in [Common Data Types](../common-data-types-unmanaged-api-reference.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6dc4d-114">要求</span><span class="sxs-lookup"><span data-stu-id="6dc4d-114">Requirements</span></span>

<span data-ttu-id="6dc4d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6dc4d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="6dc4d-116">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="6dc4d-116">**Header:** None</span></span>  
<span data-ttu-id="6dc4d-117">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="6dc4d-117">**Library:** None</span></span>  
<span data-ttu-id="6dc4d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="6dc4d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="6dc4d-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="6dc4d-119">See also</span></span>

- [<span data-ttu-id="6dc4d-120">调试</span><span class="sxs-lookup"><span data-stu-id="6dc4d-120">Debugging</span></span>](index.md)
- [<span data-ttu-id="6dc4d-121">调试枚举</span><span class="sxs-lookup"><span data-stu-id="6dc4d-121">Debugging Enumerations</span></span>](debugging-enumerations.md)
