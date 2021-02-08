---
description: 了解详细信息： ISOSDacInterface：： GetMethodDescPtrFromIP 方法
title: ISOSDacInterface：： GetMethodDescPtrFromIP 方法
ms.date: 02/01/2019
api.name:
- ISOSDacInterface::GetMethodDescPtrFromIP Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetMethodDescPtrFromIP Method
helpviewer.keywords:
- ISOSDacInterface::GetMethodDescPtrFromIP Method [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 8d7c7071b7b3fc520faea71c8d7792317745cfde
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790407"
---
# <a name="isosdacinterfacegetmethoddescptrfromip-method"></a><span data-ttu-id="f4c77-103">ISOSDacInterface：： GetMethodDescPtrFromIP 方法</span><span class="sxs-lookup"><span data-stu-id="f4c77-103">ISOSDacInterface::GetMethodDescPtrFromIP Method</span></span>

<span data-ttu-id="f4c77-104">检索与包含给定本机指令地址的方法相对应的 MethodDesc 的指针。</span><span class="sxs-lookup"><span data-stu-id="f4c77-104">Retrieves the pointer of the MethodDesc corresponding the method containing the given native instruction address.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="f4c77-105">语法</span><span class="sxs-lookup"><span data-stu-id="f4c77-105">Syntax</span></span>

```cpp
HRESULT GetMethodDescPtrFromIP(
    CLRDATA_ADDRESS ip,
    CLRDATA_ADDRESS * ppMD
);
```

## <a name="parameters"></a><span data-ttu-id="f4c77-106">参数</span><span class="sxs-lookup"><span data-stu-id="f4c77-106">Parameters</span></span>

`ip`\
<span data-ttu-id="f4c77-107">中运行时方法中的地址。</span><span class="sxs-lookup"><span data-stu-id="f4c77-107">[in] An address within the method at runtime.</span></span>

`ppMD`\
<span data-ttu-id="f4c77-108">弄特定方法的地址 `MethodDesc` 。</span><span class="sxs-lookup"><span data-stu-id="f4c77-108">[out] The address of the `MethodDesc` for the particular method.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4c77-109">备注</span><span class="sxs-lookup"><span data-stu-id="f4c77-109">Remarks</span></span>

<span data-ttu-id="f4c77-110">提供的方法是[ `ISOSDacInterface` 接口](isosdacinterface-interface.md)的一部分，并且对应于虚拟方法表的22日槽。</span><span class="sxs-lookup"><span data-stu-id="f4c77-110">The provided method is part of the [`ISOSDacInterface` interface](isosdacinterface-interface.md) and corresponds to the 22nd slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4c77-111">要求</span><span class="sxs-lookup"><span data-stu-id="f4c77-111">Requirements</span></span>

<span data-ttu-id="f4c77-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f4c77-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="f4c77-113">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="f4c77-113">**Header:** None</span></span>  
<span data-ttu-id="f4c77-114">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="f4c77-114">**Library:** None</span></span>  
<span data-ttu-id="f4c77-115">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="f4c77-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="f4c77-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="f4c77-116">See also</span></span>

- [<span data-ttu-id="f4c77-117">调试</span><span class="sxs-lookup"><span data-stu-id="f4c77-117">Debugging</span></span>](index.md)
- [<span data-ttu-id="f4c77-118">ISOSDacInterface 接口</span><span class="sxs-lookup"><span data-stu-id="f4c77-118">ISOSDacInterface Interface</span></span>](isosdacinterface-interface.md)
