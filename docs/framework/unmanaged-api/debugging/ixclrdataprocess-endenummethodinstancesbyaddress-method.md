---
description: 了解详细信息： IXCLRDataProcess：： EndEnumMethodInstancesByAddress 方法
title: IXCLRDataProcess：： EndEnumMethodInstancesByAddress 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EndEnumMethodInstancesByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EndEnumMethodInstancesByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::EndEnumMethodInstancesByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 2e01fe0737319a7b336d9f6992bf81b2c57f9e70
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800716"
---
# <a name="ixclrdataprocessendenummethodinstancesbyaddress-method"></a><span data-ttu-id="2acf1-103">IXCLRDataProcess：： EndEnumMethodInstancesByAddress 方法</span><span class="sxs-lookup"><span data-stu-id="2acf1-103">IXCLRDataProcess::EndEnumMethodInstancesByAddress Method</span></span>

<span data-ttu-id="2acf1-104">释放实例枚举期间使用的内部迭代器所使用的资源。</span><span class="sxs-lookup"><span data-stu-id="2acf1-104">Releases the resources used by internal iterators used during instance enumeration.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="2acf1-105">语法</span><span class="sxs-lookup"><span data-stu-id="2acf1-105">Syntax</span></span>

```cpp
HRESULT EndEnumMethodInstancesByAddress(
    [in] CLRDATA_ENUM handle
);
```

## <a name="parameters"></a><span data-ttu-id="2acf1-106">参数</span><span class="sxs-lookup"><span data-stu-id="2acf1-106">Parameters</span></span>

`handle`\
<span data-ttu-id="2acf1-107">弄枚举方法实例的句柄。</span><span class="sxs-lookup"><span data-stu-id="2acf1-107">[out] A handle for enumerating the method instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="2acf1-108">备注</span><span class="sxs-lookup"><span data-stu-id="2acf1-108">Remarks</span></span>

<span data-ttu-id="2acf1-109">提供的方法是接口的一部分 `IXCLRDataProcess` ，并且对应于虚拟方法表的第30个槽。</span><span class="sxs-lookup"><span data-stu-id="2acf1-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 30th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="2acf1-110">要求</span><span class="sxs-lookup"><span data-stu-id="2acf1-110">Requirements</span></span>

<span data-ttu-id="2acf1-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2acf1-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="2acf1-112">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="2acf1-112">**Header:** None</span></span>  
<span data-ttu-id="2acf1-113">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="2acf1-113">**Library:** None</span></span>  
<span data-ttu-id="2acf1-114">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="2acf1-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="2acf1-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="2acf1-115">See also</span></span>

- [<span data-ttu-id="2acf1-116">CLRDataSourceType 枚举</span><span class="sxs-lookup"><span data-stu-id="2acf1-116">CLRDataSourceType Enumeration</span></span>](clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="2acf1-117">调试</span><span class="sxs-lookup"><span data-stu-id="2acf1-117">Debugging</span></span>](index.md)
- [<span data-ttu-id="2acf1-118">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="2acf1-118">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
