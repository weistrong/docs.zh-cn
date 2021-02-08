---
description: 了解详细信息： IXCLRDataMethodDefinition：： EndEnumInstances 方法
title: IXCLRDataMethodDefinition：： EndEnumInstances 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition::EndEnumInstances Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition::EndEnumInstances Method
helpviewer.keywords:
- IXCLRDataMethodDefinition::EndEnumInstances Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: bfdcb9046b4983e6686410bf2ceadf7119b89e74
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790368"
---
# <a name="ixclrdatamethoddefinitionendenuminstances-method"></a><span data-ttu-id="c3418-103">IXCLRDataMethodDefinition：： EndEnumInstances 方法</span><span class="sxs-lookup"><span data-stu-id="c3418-103">IXCLRDataMethodDefinition::EndEnumInstances Method</span></span>

<span data-ttu-id="c3418-104">释放实例枚举期间使用的内部迭代器所使用的资源。</span><span class="sxs-lookup"><span data-stu-id="c3418-104">Releases the resources used by internal iterators used during instance enumeration.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="c3418-105">语法</span><span class="sxs-lookup"><span data-stu-id="c3418-105">Syntax</span></span>

```cpp
HRESULT EndEnumInstances(
    [in] CLRDATA_ENUM handle
);
```

## <a name="parameters"></a><span data-ttu-id="c3418-106">参数</span><span class="sxs-lookup"><span data-stu-id="c3418-106">Parameters</span></span>

`handle`\
<span data-ttu-id="c3418-107">弄用于枚举实例的句柄。</span><span class="sxs-lookup"><span data-stu-id="c3418-107">[out] A handle for enumerating the instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3418-108">备注</span><span class="sxs-lookup"><span data-stu-id="c3418-108">Remarks</span></span>

<span data-ttu-id="c3418-109">提供的方法是接口的一部分 `IXCLRDataMethodDefinition` ，并且对应于虚拟方法表的第7个槽。</span><span class="sxs-lookup"><span data-stu-id="c3418-109">The provided method is part of the `IXCLRDataMethodDefinition` interface and corresponds to the 7th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3418-110">要求</span><span class="sxs-lookup"><span data-stu-id="c3418-110">Requirements</span></span>

<span data-ttu-id="c3418-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c3418-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="c3418-112">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="c3418-112">**Header:** None</span></span>  
<span data-ttu-id="c3418-113">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="c3418-113">**Library:** None</span></span>  
<span data-ttu-id="c3418-114">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="c3418-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="c3418-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="c3418-115">See also</span></span>

- [<span data-ttu-id="c3418-116">调试</span><span class="sxs-lookup"><span data-stu-id="c3418-116">Debugging</span></span>](index.md)
- [<span data-ttu-id="c3418-117">IXCLRDataMethodDefinition 接口</span><span class="sxs-lookup"><span data-stu-id="c3418-117">IXCLRDataMethodDefinition Interface</span></span>](ixclrdatamethoddefinition-interface.md)
