---
description: 了解详细信息： IXCLRDataMethodDefinition：： StartEnumInstances 方法
title: IXCLRDataMethodDefinition：： StartEnumInstances 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition::StartEnumInstances Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition::StartEnumInstances Method
helpviewer.keywords:
- IXCLRDataMethodDefinition::StartEnumInstances Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 74de6360c90766cfec17e6b88a495fe2a70858b4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800820"
---
# <a name="ixclrdatamethoddefinitionstartenuminstances-method"></a><span data-ttu-id="6722b-103">IXCLRDataMethodDefinition：： StartEnumInstances 方法</span><span class="sxs-lookup"><span data-stu-id="6722b-103">IXCLRDataMethodDefinition::StartEnumInstances Method</span></span>

<span data-ttu-id="6722b-104">为给定的的方法实例枚举提供句柄 `IXCLRDataAppDomain` 。</span><span class="sxs-lookup"><span data-stu-id="6722b-104">Provides a handle for the enumeration of method instances for a given `IXCLRDataAppDomain`.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="6722b-105">语法</span><span class="sxs-lookup"><span data-stu-id="6722b-105">Syntax</span></span>

```cpp
HRESULT StartEnumInstances(
    [in] IXCLRDataAppDomain* appDomain,
    [out] CLRDATA_ENUM *handle
);
```

## <a name="parameters"></a><span data-ttu-id="6722b-106">参数</span><span class="sxs-lookup"><span data-stu-id="6722b-106">Parameters</span></span>

`appDomain`\
<span data-ttu-id="6722b-107">中枚举的 AppDomain。</span><span class="sxs-lookup"><span data-stu-id="6722b-107">[in] An AppDomain for the enumeration.</span></span>

`handle`\
<span data-ttu-id="6722b-108">弄用于枚举实例的句柄。</span><span class="sxs-lookup"><span data-stu-id="6722b-108">[out] A handle for enumerating the instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="6722b-109">备注</span><span class="sxs-lookup"><span data-stu-id="6722b-109">Remarks</span></span>

<span data-ttu-id="6722b-110">提供的方法是接口的一部分 `IXCLRDataMethodDefinition` ，并且对应于虚拟方法表的第5个槽。</span><span class="sxs-lookup"><span data-stu-id="6722b-110">The provided method is part of the `IXCLRDataMethodDefinition` interface and corresponds to the 5th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="6722b-111">要求</span><span class="sxs-lookup"><span data-stu-id="6722b-111">Requirements</span></span>

<span data-ttu-id="6722b-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6722b-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="6722b-113">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="6722b-113">**Header:** None</span></span>  
<span data-ttu-id="6722b-114">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="6722b-114">**Library:** None</span></span>  
<span data-ttu-id="6722b-115">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="6722b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="6722b-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="6722b-116">See also</span></span>

- [<span data-ttu-id="6722b-117">CLRDataSourceType 枚举</span><span class="sxs-lookup"><span data-stu-id="6722b-117">CLRDataSourceType Enumeration</span></span>](clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="6722b-118">调试</span><span class="sxs-lookup"><span data-stu-id="6722b-118">Debugging</span></span>](index.md)
- [<span data-ttu-id="6722b-119">IXCLRDataMethodDefinition 接口</span><span class="sxs-lookup"><span data-stu-id="6722b-119">IXCLRDataMethodDefinition Interface</span></span>](ixclrdatamethoddefinition-interface.md)
