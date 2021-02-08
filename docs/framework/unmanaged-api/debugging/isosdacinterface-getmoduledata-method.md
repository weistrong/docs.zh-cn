---
description: 了解详细信息： ISOSDacInterface：： GetModuleData 方法
title: ISOSDacInterface：： GetModuleData 方法
ms.date: 02/01/2019
api.name:
- ISOSDacInterface::GetModuleData Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetModuleData Method
helpviewer.keywords:
- ISOSDacInterface::GetModuleData Method [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: c01f55d55d5ee9082dee4b3adb3022bb17807aa2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790381"
---
# <a name="isosdacinterfacegetmoduledata-method"></a><span data-ttu-id="ba547-103">ISOSDacInterface：： GetModuleData 方法</span><span class="sxs-lookup"><span data-stu-id="ba547-103">ISOSDacInterface::GetModuleData Method</span></span>

<span data-ttu-id="ba547-104">提取与在给定地址加载的模块对应的数据。</span><span class="sxs-lookup"><span data-stu-id="ba547-104">Fetches the data corresponding to the module loaded at a given address.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="ba547-105">语法</span><span class="sxs-lookup"><span data-stu-id="ba547-105">Syntax</span></span>

```cpp
HRESULT GetModuleData(
    CLRDATA_ADDRESS moduleAddr,
    DacpModuleData *data
);
```

## <a name="parameters"></a><span data-ttu-id="ba547-106">参数</span><span class="sxs-lookup"><span data-stu-id="ba547-106">Parameters</span></span>

`moduleAddr`\
<span data-ttu-id="ba547-107">中要为其检索信息的模块的地址。</span><span class="sxs-lookup"><span data-stu-id="ba547-107">[in] The address of the module to retrieve information for.</span></span>

`data`\
<span data-ttu-id="ba547-108">弄用于保存已加载模块的信息的 [DacpModuleData 结构](dacpmoduledata-structure.md) 。</span><span class="sxs-lookup"><span data-stu-id="ba547-108">[out] The [DacpModuleData structure](dacpmoduledata-structure.md) to hold the information of the loaded module.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba547-109">备注</span><span class="sxs-lookup"><span data-stu-id="ba547-109">Remarks</span></span>

<span data-ttu-id="ba547-110">提供的方法是接口的一部分 `ISOSDacInterface` ，并且对应于虚拟方法表的第14个槽。</span><span class="sxs-lookup"><span data-stu-id="ba547-110">The provided method is part of the `ISOSDacInterface` interface and corresponds to the 14th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba547-111">要求</span><span class="sxs-lookup"><span data-stu-id="ba547-111">Requirements</span></span>

<span data-ttu-id="ba547-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ba547-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="ba547-113">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="ba547-113">**Header:** None</span></span>  
<span data-ttu-id="ba547-114">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="ba547-114">**Library:** None</span></span>  
<span data-ttu-id="ba547-115">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="ba547-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="ba547-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="ba547-116">See also</span></span>

- [<span data-ttu-id="ba547-117">调试</span><span class="sxs-lookup"><span data-stu-id="ba547-117">Debugging</span></span>](index.md)
- [<span data-ttu-id="ba547-118">ISOSDacInterface 接口</span><span class="sxs-lookup"><span data-stu-id="ba547-118">ISOSDacInterface Interface</span></span>](isosdacinterface-interface.md)
