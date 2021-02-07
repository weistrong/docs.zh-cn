---
description: 了解详细信息： StrongNameKeyInstall 函数
title: StrongNameKeyInstall 函数
ms.date: 03/30/2017
api_name:
- StrongNameKeyInstall
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameKeyInstall
helpviewer_keywords:
- StrongNameKeyInstall function [.NET Framework strong naming]
ms.assetid: e32fd546-7757-4681-be3d-658e93281e50
topic_type:
- apiref
ms.openlocfilehash: 0a5d3971ac0927dda7066405adc01a5c80b7faca
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99670536"
---
# <a name="strongnamekeyinstall-function"></a><span data-ttu-id="02668-103">StrongNameKeyInstall 函数</span><span class="sxs-lookup"><span data-stu-id="02668-103">StrongNameKeyInstall Function</span></span>

<span data-ttu-id="02668-104">将公钥/私钥对导入容器。</span><span class="sxs-lookup"><span data-stu-id="02668-104">Imports a public/private key pair into a container.</span></span>

<span data-ttu-id="02668-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="02668-105">This function has been deprecated.</span></span> <span data-ttu-id="02668-106">改为使用 [ICLRStrongName：： StrongNameKeyInstall](../hosting/iclrstrongname-strongnamekeyinstall-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="02668-106">Use the [ICLRStrongName::StrongNameKeyInstall](../hosting/iclrstrongname-strongnamekeyinstall-method.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="02668-107">语法</span><span class="sxs-lookup"><span data-stu-id="02668-107">Syntax</span></span>

```cpp
BOOLEAN StrongNameKeyInstall (
    [in]  LPCWSTR   wszKeyContainer,
    [in]  BYTE      *pbKeyBlob,
    [in]  ULONG     cbKeyBlob
);
```

## <a name="parameters"></a><span data-ttu-id="02668-108">参数</span><span class="sxs-lookup"><span data-stu-id="02668-108">Parameters</span></span>

`wszKeyContainer`\
<span data-ttu-id="02668-109">中密钥容器的名称。</span><span class="sxs-lookup"><span data-stu-id="02668-109">[in] The name of the key container.</span></span> <span data-ttu-id="02668-110">`wszKeyContainer` 必须为非空字符串。</span><span class="sxs-lookup"><span data-stu-id="02668-110">`wszKeyContainer` must be a non-empty string.</span></span>

`pbKeyBlob`\
<span data-ttu-id="02668-111">中二进制密钥对。</span><span class="sxs-lookup"><span data-stu-id="02668-111">[in] The binary key pair.</span></span>

`cbKeyBlob`\
<span data-ttu-id="02668-112">中的大小（以字节为单位） `pbKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="02668-112">[in] The size, in bytes, of `pbKeyBlob`.</span></span>

## <a name="return-value"></a><span data-ttu-id="02668-113">返回值</span><span class="sxs-lookup"><span data-stu-id="02668-113">Return Value</span></span>

<span data-ttu-id="02668-114">`true` 成功完成时;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="02668-114">`true` on successful completion; otherwise, `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="02668-115">备注</span><span class="sxs-lookup"><span data-stu-id="02668-115">Remarks</span></span>

<span data-ttu-id="02668-116">使用 [StrongNameKeyDelete](strongnamekeydelete-function.md) 函数可删除密钥容器。</span><span class="sxs-lookup"><span data-stu-id="02668-116">Use the [StrongNameKeyDelete](strongnamekeydelete-function.md) function to delete the key container.</span></span>

<span data-ttu-id="02668-117">如果 `StrongNameKeyInstall` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。</span><span class="sxs-lookup"><span data-stu-id="02668-117">If the `StrongNameKeyInstall` function does not complete successfully, call the [StrongNameErrorInfo](strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>

## <a name="requirements"></a><span data-ttu-id="02668-118">要求</span><span class="sxs-lookup"><span data-stu-id="02668-118">Requirements</span></span>

<span data-ttu-id="02668-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="02668-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="02668-120">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="02668-120">**Header:** StrongName.h</span></span>

<span data-ttu-id="02668-121">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="02668-121">**Library:** Included as a resource in MsCorEE.dll</span></span>

<span data-ttu-id="02668-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="02668-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="02668-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="02668-123">See also</span></span>

- [<span data-ttu-id="02668-124">StrongNameKeyInstall 方法</span><span class="sxs-lookup"><span data-stu-id="02668-124">StrongNameKeyInstall Method</span></span>](../hosting/iclrstrongname-strongnamekeyinstall-method.md)
- [<span data-ttu-id="02668-125">StrongNameKeyDelete 方法</span><span class="sxs-lookup"><span data-stu-id="02668-125">StrongNameKeyDelete Method</span></span>](../hosting/iclrstrongname-strongnamekeydelete-method.md)
- [<span data-ttu-id="02668-126">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="02668-126">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
