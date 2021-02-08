---
description: 了解详细信息： IXCLRDataModule：： GetMethodDefinitionByToken 方法
title: IXCLRDataModule：： GetMethodDefinitionByToken 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataModule::GetMethodDefinitionByToken Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule::GetMethodDefinitionByToken Method
helpviewer.keywords:
- IXCLRDataModule::GetMethodDefinitionByToken Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 1eb1187d09183bfff97324a8032d23cbf471f580
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800768"
---
# <a name="ixclrdatamodulegetmethoddefinitionbytoken-method"></a><span data-ttu-id="73d40-103">IXCLRDataModule：： GetMethodDefinitionByToken 方法</span><span class="sxs-lookup"><span data-stu-id="73d40-103">IXCLRDataModule::GetMethodDefinitionByToken Method</span></span>

<span data-ttu-id="73d40-104">获取对应于给定元数据标记的方法定义。</span><span class="sxs-lookup"><span data-stu-id="73d40-104">Gets the method definition corresponding to a given metadata token.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="73d40-105">语法</span><span class="sxs-lookup"><span data-stu-id="73d40-105">Syntax</span></span>

```cpp
HRESULT GetMethodDefinitionByToken(
    [in] mdMethodDef token,
    [out] IXCLRDataMethodDefinition** methodDefinition
);
```

## <a name="parameters"></a><span data-ttu-id="73d40-106">参数</span><span class="sxs-lookup"><span data-stu-id="73d40-106">Parameters</span></span>

`token`\
<span data-ttu-id="73d40-107">中方法标记。</span><span class="sxs-lookup"><span data-stu-id="73d40-107">[in] The method token.</span></span>

`methodDefinition`\
<span data-ttu-id="73d40-108">弄方法定义。</span><span class="sxs-lookup"><span data-stu-id="73d40-108">[out] The method definition.</span></span>

## <a name="remarks"></a><span data-ttu-id="73d40-109">备注</span><span class="sxs-lookup"><span data-stu-id="73d40-109">Remarks</span></span>

<span data-ttu-id="73d40-110">提供的方法是接口的一部分 `IXCLRDataModule` ，并且对应于虚拟方法表的26个槽。</span><span class="sxs-lookup"><span data-stu-id="73d40-110">The provided method is part of the `IXCLRDataModule` interface and corresponds to the 26th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="73d40-111">要求</span><span class="sxs-lookup"><span data-stu-id="73d40-111">Requirements</span></span>

<span data-ttu-id="73d40-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="73d40-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="73d40-113">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="73d40-113">**Header:** None</span></span>  
<span data-ttu-id="73d40-114">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="73d40-114">**Library:** None</span></span>  
<span data-ttu-id="73d40-115">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="73d40-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="73d40-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="73d40-116">See also</span></span>

- [<span data-ttu-id="73d40-117">调试</span><span class="sxs-lookup"><span data-stu-id="73d40-117">Debugging</span></span>](index.md)
- [<span data-ttu-id="73d40-118">IXCLRDataModule 接口</span><span class="sxs-lookup"><span data-stu-id="73d40-118">IXCLRDataModule Interface</span></span>](ixclrdatamodule-interface.md)
