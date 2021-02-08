---
description: 了解详细信息： IXCLRDataProcess：： GetRuntimeNameByAddress 方法
title: IXCLRDataProcess：： GetRuntimeNameByAddress 方法
ms.date: 4/27/2020
api.name:
- IXCLRDataProcess::GetRuntimeNameByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::GetRuntimeNameByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::GetRuntimeNameByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: tommcdon
ms.author: tommcdon
ms.openlocfilehash: 62d9ae73c216748cc8eb02aedd41cf19f475d071
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800651"
---
# <a name="ixclrdataprocessgetruntimenamebyaddress-method"></a><span data-ttu-id="e3480-103">IXCLRDataProcess：： GetRuntimeNameByAddress 方法</span><span class="sxs-lookup"><span data-stu-id="e3480-103">IXCLRDataProcess::GetRuntimeNameByAddress Method</span></span>

<span data-ttu-id="e3480-104">获取给定地址的名称。</span><span class="sxs-lookup"><span data-stu-id="e3480-104">Gets a name for the given address.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="e3480-105">语法</span><span class="sxs-lookup"><span data-stu-id="e3480-105">Syntax</span></span>

```cpp
HRESULT GetRuntimeNameByAddress(
    [in] CLRDATA_ADDRESS address,
    [in] ULONG32 flags,
    [in] ULONG32 bufLen,
    [out] ULONG32 *nameLen,
    [out, size_is(bufLen)] WCHAR nameBuf[],
    [out] CLRDATA_ADDRESS* displacement
);
```

## <a name="parameters"></a><span data-ttu-id="e3480-106">参数</span><span class="sxs-lookup"><span data-stu-id="e3480-106">Parameters</span></span>

`address`\
<span data-ttu-id="e3480-107">中一个 `CLRDATA_ADDRESS` 表示代码地址的值。</span><span class="sxs-lookup"><span data-stu-id="e3480-107">[in] A `CLRDATA_ADDRESS` value that represents a code address.</span></span>

`flags`\
<span data-ttu-id="e3480-108">中设置为 "0"。</span><span class="sxs-lookup"><span data-stu-id="e3480-108">[in] Set to '0'.</span></span>

`bufLen`\
<span data-ttu-id="e3480-109">中缓冲区的长度。</span><span class="sxs-lookup"><span data-stu-id="e3480-109">[in] The length of the buffer.</span></span>

`namLen`\
<span data-ttu-id="e3480-110">弄一个指针，指向返回的字符数。</span><span class="sxs-lookup"><span data-stu-id="e3480-110">[out] A pointer to the number of characters returned.</span></span>

`namBuf`\
<span data-ttu-id="e3480-111">[out，size_is (`bufLen`) ] `bufLen` 存储运行时名称的长度的输入缓冲区。</span><span class="sxs-lookup"><span data-stu-id="e3480-111">[out, size_is(`bufLen`)] The input buffer of length `bufLen` that stores the runtime name.</span></span>

`displacement`\
<span data-ttu-id="e3480-112">弄 `CLRDATA_ADDRESS` 指向返回符号的代码偏移量的指针。</span><span class="sxs-lookup"><span data-stu-id="e3480-112">[out] A `CLRDATA_ADDRESS` pointer to the code offset of the returned symbol.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3480-113">备注</span><span class="sxs-lookup"><span data-stu-id="e3480-113">Remarks</span></span>

<span data-ttu-id="e3480-114">提供的方法是接口的一部分 `IXCLRDataProcess` ，并且对应于虚拟方法表的第16个槽。</span><span class="sxs-lookup"><span data-stu-id="e3480-114">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 16th slot of the virtual-method table.</span></span>

> [!NOTE]
> <span data-ttu-id="e3480-115">如果缓冲区不够大，则此方法返回， `S_FALSE` 并将设置 `nameLen` 为所需的缓冲区长度。</span><span class="sxs-lookup"><span data-stu-id="e3480-115">If the buffer is not large enough for the name, this method returns `S_FALSE` and sets `nameLen` to the required buffer length.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3480-116">要求</span><span class="sxs-lookup"><span data-stu-id="e3480-116">Requirements</span></span>

<span data-ttu-id="e3480-117">**平台：** 查看 [系统要求](../../get-started/system-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="e3480-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md)</span></span>\
<span data-ttu-id="e3480-118">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="e3480-118">**Header:** None\</span></span>
<span data-ttu-id="e3480-119">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="e3480-119">**Library:** None\</span></span>
<span data-ttu-id="e3480-120">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="e3480-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="e3480-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="e3480-121">See also</span></span>

- [<span data-ttu-id="e3480-122">调试</span><span class="sxs-lookup"><span data-stu-id="e3480-122">Debugging</span></span>](index.md)
- [<span data-ttu-id="e3480-123">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="e3480-123">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
