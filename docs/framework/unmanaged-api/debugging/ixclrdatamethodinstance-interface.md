---
description: 了解详细信息： IXCLRDataMethodInstance 接口
title: IXCLRDataMethodInstance 接口
ms.date: 02/01/2019
api.name:
- IXCLRDataMethodInstance Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodInstance Interface
helpviewer.keywords:
- IXCLRDataMethodInstance Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 4e9ad57988420ff14b297c693c31c0dc5b3b181c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800781"
---
# <a name="ixclrdatamethodinstance-interface"></a><span data-ttu-id="fe68c-103">IXCLRDataMethodInstance 接口</span><span class="sxs-lookup"><span data-stu-id="fe68c-103">IXCLRDataMethodInstance Interface</span></span>

<span data-ttu-id="fe68c-104">提供用于查询有关方法实例的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="fe68c-104">Provides methods for querying information about a method instance.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="fe68c-105">方法</span><span class="sxs-lookup"><span data-stu-id="fe68c-105">Methods</span></span>

| <span data-ttu-id="fe68c-106">方法</span><span class="sxs-lookup"><span data-stu-id="fe68c-106">Method</span></span>                                                                                                                  | <span data-ttu-id="fe68c-107">说明</span><span class="sxs-lookup"><span data-stu-id="fe68c-107">Description</span></span>                                 |
| ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| [<span data-ttu-id="fe68c-108">GetILAddressMap</span><span class="sxs-lookup"><span data-stu-id="fe68c-108">GetILAddressMap</span></span>](ixclrdatamethodinstance-getiladdressmap-method.md) | <span data-ttu-id="fe68c-109">获取用于寻址映射信息的 IL。</span><span class="sxs-lookup"><span data-stu-id="fe68c-109">Gets the IL to address mapping information.</span></span> |
| [<span data-ttu-id="fe68c-110">GetRepresentativeEntryAddress</span><span class="sxs-lookup"><span data-stu-id="fe68c-110">GetRepresentativeEntryAddress</span></span>](ixclrdatamethodinstance-getrepresentativeentryaddress-method.md) | <span data-ttu-id="fe68c-111">获取方法的所有可能入口点的本机编译的最具代表性的入口点地址。</span><span class="sxs-lookup"><span data-stu-id="fe68c-111">Gets the most representative entry point address for the native compilation of all the possible entry points for a method.</span></span> |

## <a name="remarks"></a><span data-ttu-id="fe68c-112">备注</span><span class="sxs-lookup"><span data-stu-id="fe68c-112">Remarks</span></span>

<span data-ttu-id="fe68c-113">此接口在运行时中存在，不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="fe68c-113">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="fe68c-114">但是，它是从使用 GUID 派生的 COM 接口， `IUnknown` `ECD73800-22CA-4b0d-AB55-E9BA7E6318A5` 该接口可通过常用的 COM 机制获得。</span><span class="sxs-lookup"><span data-stu-id="fe68c-114">However, it's a COM interface that derives from `IUnknown` with GUID `ECD73800-22CA-4b0d-AB55-E9BA7E6318A5` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe68c-115">要求</span><span class="sxs-lookup"><span data-stu-id="fe68c-115">Requirements</span></span>

<span data-ttu-id="fe68c-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fe68c-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="fe68c-117">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="fe68c-117">**Header:** None</span></span>  
<span data-ttu-id="fe68c-118">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="fe68c-118">**Library:** None</span></span>  
<span data-ttu-id="fe68c-119">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="fe68c-119">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="fe68c-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="fe68c-120">See also</span></span>

- [<span data-ttu-id="fe68c-121">调试</span><span class="sxs-lookup"><span data-stu-id="fe68c-121">Debugging</span></span>](index.md)
- [<span data-ttu-id="fe68c-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="fe68c-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
