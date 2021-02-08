---
description: 了解详细信息： IXCLRDataMethodInstance：： GetILAddressMap 方法
title: IXCLRDataMethodInstance：： GetILAddressMap 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodInstance::GetILAddressMap Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodInstance::GetILAddressMap Method
helpviewer.keywords:
- IXCLRDataMethodInstance::GetILAddressMap Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: ddddf593c3c18f2b4cd1682b5d6f7c8ff1985ac6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800807"
---
# <a name="ixclrdatamethodinstancegetiladdressmap-method"></a><span data-ttu-id="368b0-103">IXCLRDataMethodInstance：： GetILAddressMap 方法</span><span class="sxs-lookup"><span data-stu-id="368b0-103">IXCLRDataMethodInstance::GetILAddressMap Method</span></span>

<span data-ttu-id="368b0-104">获取用于寻址映射信息的 IL。</span><span class="sxs-lookup"><span data-stu-id="368b0-104">Gets the IL to address mapping information.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="368b0-105">语法</span><span class="sxs-lookup"><span data-stu-id="368b0-105">Syntax</span></span>

```cpp
HRESULT GetILAddressMap(
    [in] ULONG32                                   mapLen,
    [out] ULONG32                                 *mapNeeded,
    [out, size_is(mapLen)] CLRDATA_IL_ADDRESS_MAP  maps[]
);
```

## <a name="parameters"></a><span data-ttu-id="368b0-106">参数</span><span class="sxs-lookup"><span data-stu-id="368b0-106">Parameters</span></span>

`mapLen`\
<span data-ttu-id="368b0-107">中所提供的映射数组的长度。</span><span class="sxs-lookup"><span data-stu-id="368b0-107">[in] The length of the provided maps array.</span></span>

`mapNeeded`\
<span data-ttu-id="368b0-108">弄该方法所需的映射项的数目。</span><span class="sxs-lookup"><span data-stu-id="368b0-108">[out] The number of map entries that the method needs.</span></span>

`maps`\
<span data-ttu-id="368b0-109">[out，size_is (mapLen) ]用于存储映射项的数组。</span><span class="sxs-lookup"><span data-stu-id="368b0-109">[out, size_is(mapLen)] The array for storing the map entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="368b0-110">备注</span><span class="sxs-lookup"><span data-stu-id="368b0-110">Remarks</span></span>

<span data-ttu-id="368b0-111">提供的方法是接口的一部分 `IXCLRDataMethodInstance` ，并且对应于虚拟方法表的第15个槽。</span><span class="sxs-lookup"><span data-stu-id="368b0-111">The provided method is part of the `IXCLRDataMethodInstance` interface and corresponds to the 15th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="368b0-112">要求</span><span class="sxs-lookup"><span data-stu-id="368b0-112">Requirements</span></span>

<span data-ttu-id="368b0-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="368b0-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="368b0-114">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="368b0-114">**Header:** None</span></span>  
<span data-ttu-id="368b0-115">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="368b0-115">**Library:** None</span></span>  
<span data-ttu-id="368b0-116">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="368b0-116">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="368b0-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="368b0-117">See also</span></span>

- [<span data-ttu-id="368b0-118">调试</span><span class="sxs-lookup"><span data-stu-id="368b0-118">Debugging</span></span>](index.md)
- [<span data-ttu-id="368b0-119">IXCLRDataMethodInstance 接口</span><span class="sxs-lookup"><span data-stu-id="368b0-119">IXCLRDataMethodInstance Interface</span></span>](ixclrdatamethodinstance-interface.md)
