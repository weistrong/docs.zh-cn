---
description: 了解详细信息： StrongNameKeyDelete 函数
title: StrongNameKeyDelete 函数
ms.date: 03/30/2017
api_name:
- StrongNameKeyDelete
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameKeyDelete
helpviewer_keywords:
- StrongNameKeyDelete function [.NET Framework strong naming]
ms.assetid: 313e71e4-1790-4d2f-b68b-5040ebd1c149
topic_type:
- apiref
ms.openlocfilehash: 9314d961f79e673925125c2362308f9ab4533e75
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781202"
---
# <a name="strongnamekeydelete-function"></a><span data-ttu-id="37615-103">StrongNameKeyDelete 函数</span><span class="sxs-lookup"><span data-stu-id="37615-103">StrongNameKeyDelete Function</span></span>

<span data-ttu-id="37615-104">删除指定的密钥容器。</span><span class="sxs-lookup"><span data-stu-id="37615-104">Deletes the specified key container.</span></span>

<span data-ttu-id="37615-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="37615-105">This function has been deprecated.</span></span> <span data-ttu-id="37615-106">改为使用 [ICLRStrongName：： StrongNameKeyDelete](../hosting/iclrstrongname-strongnamekeydelete-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="37615-106">Use the [ICLRStrongName::StrongNameKeyDelete](../hosting/iclrstrongname-strongnamekeydelete-method.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="37615-107">语法</span><span class="sxs-lookup"><span data-stu-id="37615-107">Syntax</span></span>

```cpp
BOOLEAN StrongNameKeyDelete (
    [in]  LPCWSTR   wszKeyContainer
);
```

## <a name="parameters"></a><span data-ttu-id="37615-108">参数</span><span class="sxs-lookup"><span data-stu-id="37615-108">Parameters</span></span>

`wszKeyContainer`\
<span data-ttu-id="37615-109">中要删除的密钥容器的名称。</span><span class="sxs-lookup"><span data-stu-id="37615-109">[in] The name of the key container to delete.</span></span>

## <a name="return-value"></a><span data-ttu-id="37615-110">返回值</span><span class="sxs-lookup"><span data-stu-id="37615-110">Return Value</span></span>

<span data-ttu-id="37615-111">`true` 成功完成时;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="37615-111">`true` on successful completion; otherwise, `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="37615-112">备注</span><span class="sxs-lookup"><span data-stu-id="37615-112">Remarks</span></span>

<span data-ttu-id="37615-113">使用 [StrongNameKeyInstall](strongnamekeyinstall-function.md) 函数将公钥/私钥对导入到容器中。</span><span class="sxs-lookup"><span data-stu-id="37615-113">Use the [StrongNameKeyInstall](strongnamekeyinstall-function.md) function to import a public/private key pair into a container.</span></span>

<span data-ttu-id="37615-114">如果 `StrongNameKeyDelete` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。</span><span class="sxs-lookup"><span data-stu-id="37615-114">If the `StrongNameKeyDelete` function does not complete successfully, call the [StrongNameErrorInfo](strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>

## <a name="requirements"></a><span data-ttu-id="37615-115">要求</span><span class="sxs-lookup"><span data-stu-id="37615-115">Requirements</span></span>

<span data-ttu-id="37615-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="37615-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="37615-117">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="37615-117">**Header:** StrongName.h</span></span>

<span data-ttu-id="37615-118">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="37615-118">**Library:** Included as a resource in MsCorEE.dll</span></span>

<span data-ttu-id="37615-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="37615-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="37615-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="37615-120">See also</span></span>

- [<span data-ttu-id="37615-121">StrongNameKeyDelete 方法</span><span class="sxs-lookup"><span data-stu-id="37615-121">StrongNameKeyDelete Method</span></span>](../hosting/iclrstrongname-strongnamekeydelete-method.md)
- [<span data-ttu-id="37615-122">StrongNameKeyInstall 方法</span><span class="sxs-lookup"><span data-stu-id="37615-122">StrongNameKeyInstall Method</span></span>](../hosting/iclrstrongname-strongnamekeyinstall-method.md)
- [<span data-ttu-id="37615-123">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="37615-123">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
