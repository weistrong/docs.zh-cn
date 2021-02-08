---
description: 了解详细信息： IXCLRDataModule：： GetVersionId 方法
title: IXCLRDataModule：： GetVersionId 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataModule::GetVersionId Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule::GetVersionId Method
helpviewer.keywords:
- IXCLRDataModule::GetVersionId Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 1b924757f43d106df555ea028270ac873f8f4558
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800755"
---
# <a name="ixclrdatamodulegetversionid-method"></a><span data-ttu-id="cd8cc-103">IXCLRDataModule：： GetVersionId 方法</span><span class="sxs-lookup"><span data-stu-id="cd8cc-103">IXCLRDataModule::GetVersionId Method</span></span>

<span data-ttu-id="cd8cc-104">获取模块的版本标识符。</span><span class="sxs-lookup"><span data-stu-id="cd8cc-104">Gets the module's version identifier.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="cd8cc-105">语法</span><span class="sxs-lookup"><span data-stu-id="cd8cc-105">Syntax</span></span>

```cpp
HRESULT GetVersionId(
    [out] GUID* vid
);
```

## <a name="parameters"></a><span data-ttu-id="cd8cc-106">参数</span><span class="sxs-lookup"><span data-stu-id="cd8cc-106">Parameters</span></span>

`vid`\
<span data-ttu-id="cd8cc-107">弄模块的版本标识符。</span><span class="sxs-lookup"><span data-stu-id="cd8cc-107">[out] The module's version identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd8cc-108">备注</span><span class="sxs-lookup"><span data-stu-id="cd8cc-108">Remarks</span></span>

<span data-ttu-id="cd8cc-109">提供的方法是接口的一部分 `IXCLRDataModule` ，并且对应于虚拟方法表的第41届槽。</span><span class="sxs-lookup"><span data-stu-id="cd8cc-109">The provided method is part of the `IXCLRDataModule` interface and corresponds to the 41st slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd8cc-110">要求</span><span class="sxs-lookup"><span data-stu-id="cd8cc-110">Requirements</span></span>

<span data-ttu-id="cd8cc-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cd8cc-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="cd8cc-112">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="cd8cc-112">**Header:** None</span></span>  
<span data-ttu-id="cd8cc-113">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="cd8cc-113">**Library:** None</span></span>  
<span data-ttu-id="cd8cc-114">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="cd8cc-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="cd8cc-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="cd8cc-115">See also</span></span>

- [<span data-ttu-id="cd8cc-116">调试</span><span class="sxs-lookup"><span data-stu-id="cd8cc-116">Debugging</span></span>](index.md)
- [<span data-ttu-id="cd8cc-117">IXCLRDataModule 接口</span><span class="sxs-lookup"><span data-stu-id="cd8cc-117">IXCLRDataModule Interface</span></span>](ixclrdatamodule-interface.md)
