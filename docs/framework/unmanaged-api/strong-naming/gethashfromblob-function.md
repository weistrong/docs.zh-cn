---
description: 了解详细信息： GetHashFromBlob 函数
title: GetHashFromBlob 函数
ms.date: 03/30/2017
api_name:
- GetHashFromBlob
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromBlob
helpviewer_keywords:
- GetHashFromBlob function [.NET Framework strong naming]
ms.assetid: b712d862-f2d0-4b55-87d4-65bbeadef982
topic_type:
- apiref
ms.openlocfilehash: dc5039e44440afa7a000bc61167faec0e5b6cc84
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736604"
---
# <a name="gethashfromblob-function"></a><span data-ttu-id="c1ac8-103">GetHashFromBlob 函数</span><span class="sxs-lookup"><span data-stu-id="c1ac8-103">GetHashFromBlob Function</span></span>

<span data-ttu-id="c1ac8-104">使用指定的哈希算法获取指定内存地址处的程序集的哈希。</span><span class="sxs-lookup"><span data-stu-id="c1ac8-104">Gets a hash of the assembly at the specified memory address, using the specified hash algorithm.</span></span>

<span data-ttu-id="c1ac8-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="c1ac8-105">This function has been deprecated.</span></span> <span data-ttu-id="c1ac8-106">改为使用 [ICLRStrongName：： GetHashFromBlob](../hosting/iclrstrongname-gethashfromblob-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c1ac8-106">Use the [ICLRStrongName::GetHashFromBlob](../hosting/iclrstrongname-gethashfromblob-method.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1ac8-107">语法</span><span class="sxs-lookup"><span data-stu-id="c1ac8-107">Syntax</span></span>

```cpp
HRESULT GetHashFromBlob (
    [in]  BYTE    *pbBlob,
    [in]  DWORD   cchBlob,
    [in, out] unsigned int   *piHashAlg,
    [out] BYTE    *pbHash,
    [in]  DWORD   cchHash,
    [out] DWORD   *pchHash
);
```

## <a name="parameters"></a><span data-ttu-id="c1ac8-108">参数</span><span class="sxs-lookup"><span data-stu-id="c1ac8-108">Parameters</span></span>

`pbBlob`\
<span data-ttu-id="c1ac8-109">中一个指针，指向要进行哈希处理的内存块的地址。</span><span class="sxs-lookup"><span data-stu-id="c1ac8-109">[in] A pointer to the address of the memory block to be hashed.</span></span>

`cchBlob`\
<span data-ttu-id="c1ac8-110">中内存块的长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c1ac8-110">[in] The length, in bytes, of the memory block.</span></span>

`piHashAlg`\
<span data-ttu-id="c1ac8-111">[in，out]指定哈希算法的常量。</span><span class="sxs-lookup"><span data-stu-id="c1ac8-111">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="c1ac8-112">对于默认算法，使用零。</span><span class="sxs-lookup"><span data-stu-id="c1ac8-112">Use zero for the default algorithm.</span></span>

`pbHash`\
<span data-ttu-id="c1ac8-113">弄返回的哈希缓冲区。</span><span class="sxs-lookup"><span data-stu-id="c1ac8-113">[out] The returned hash buffer.</span></span>

`cchHash`\
<span data-ttu-id="c1ac8-114">中请求的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="c1ac8-114">[in] The requested maximum size of `pbHash`.</span></span>

`pchHash`\
<span data-ttu-id="c1ac8-115">弄返回的的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="c1ac8-115">[out] The size, in bytes, of the returned `pbHash`.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1ac8-116">要求</span><span class="sxs-lookup"><span data-stu-id="c1ac8-116">Requirements</span></span>

<span data-ttu-id="c1ac8-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c1ac8-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="c1ac8-118">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="c1ac8-118">**Header:** StrongName.h</span></span>

<span data-ttu-id="c1ac8-119">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c1ac8-119">**Library:** Included as a resource in MsCorEE.dll</span></span>

<span data-ttu-id="c1ac8-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c1ac8-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="c1ac8-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="c1ac8-121">See also</span></span>

- [<span data-ttu-id="c1ac8-122">GetHashFromBlob 方法</span><span class="sxs-lookup"><span data-stu-id="c1ac8-122">GetHashFromBlob Method</span></span>](../hosting/iclrstrongname-gethashfromblob-method.md)
- [<span data-ttu-id="c1ac8-123">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="c1ac8-123">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
