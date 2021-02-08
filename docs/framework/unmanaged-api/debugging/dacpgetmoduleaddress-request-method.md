---
description: 了解详细信息： DacpGetModuleAddress：： Request 方法
title: DacpGetModuleAddress::Request 方法
ms.date: 01/16/2019
api.name:
- DacpGetModuleAddress::Request Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpGetModuleAddress::Request Method
helpviewer.keywords:
- DacpGetModuleAddress::Request Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 4cdec9cf6b9bd818ce1137fb5b2c691532fab94e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801496"
---
# <a name="dacpgetmoduleaddressrequest-method"></a><span data-ttu-id="d2687-103">DacpGetModuleAddress::Request 方法</span><span class="sxs-lookup"><span data-stu-id="d2687-103">DacpGetModuleAddress::Request Method</span></span>

<span data-ttu-id="d2687-104">执行从给定的运行时结构填充结构的请求。</span><span class="sxs-lookup"><span data-stu-id="d2687-104">Performs a request to populate the structure from the given runtime structure.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="d2687-105">语法</span><span class="sxs-lookup"><span data-stu-id="d2687-105">Syntax</span></span>

```cpp
HRESULT Request(
    [in] IXCLRDataModule* pDataModule
);
```

## <a name="parameters"></a><span data-ttu-id="d2687-106">参数</span><span class="sxs-lookup"><span data-stu-id="d2687-106">Parameters</span></span>

`pDataModule`\
<span data-ttu-id="d2687-107">中指向种子数据模块的指针。</span><span class="sxs-lookup"><span data-stu-id="d2687-107">[in] A pointer to the seed data module.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2687-108">备注</span><span class="sxs-lookup"><span data-stu-id="d2687-108">Remarks</span></span>

<span data-ttu-id="d2687-109">此结构存在于运行时中，并且不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="d2687-109">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="d2687-110">若要使用它，最简单的方法是模拟实现：</span><span class="sxs-lookup"><span data-stu-id="d2687-110">To use it, the easiest way is to mimic the implementation:</span></span>

- <span data-ttu-id="d2687-111">返回通过在参数上调用方法获取的值 `Request` ，该方法 `IXCLRDataModule*` 具有以下参数： `((uint32) 0xf0000000, 0, 0, (uint32) sizeof(*this), (uint8*) this)`</span><span class="sxs-lookup"><span data-stu-id="d2687-111">Return the value obtained from calling the `Request` method on the `IXCLRDataModule*` parameter with the following parameters: `((uint32) 0xf0000000, 0, 0, (uint32) sizeof(*this), (uint8*) this)`</span></span>

## <a name="requirements"></a><span data-ttu-id="d2687-112">要求</span><span class="sxs-lookup"><span data-stu-id="d2687-112">Requirements</span></span>

<span data-ttu-id="d2687-113">**平台：** 查看 [系统要求](../../get-started/system-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="d2687-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md)</span></span>\
<span data-ttu-id="d2687-114">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="d2687-114">**Header:** None\</span></span>
<span data-ttu-id="d2687-115">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="d2687-115">**Library:** None\</span></span>
<span data-ttu-id="d2687-116">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d2687-116">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="d2687-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="d2687-117">See also</span></span>

- [<span data-ttu-id="d2687-118">调试</span><span class="sxs-lookup"><span data-stu-id="d2687-118">Debugging</span></span>](index.md)
- [<span data-ttu-id="d2687-119">DacpGetModuleAddress 结构</span><span class="sxs-lookup"><span data-stu-id="d2687-119">DacpGetModuleAddress structure</span></span>](dacpgetmoduleaddress-structure.md)
