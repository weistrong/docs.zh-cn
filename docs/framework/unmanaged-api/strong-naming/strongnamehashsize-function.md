---
description: 了解详细信息： StrongNameHashSize 函数
title: StrongNameHashSize 函数
ms.date: 03/30/2017
api_name:
- StrongNameHashSize
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameHashSize
helpviewer_keywords:
- StrongNameHashSize function [.NET Framework strong naming]
ms.assetid: 738c98d7-a60c-45fe-a296-220af05e6991
topic_type:
- apiref
ms.openlocfilehash: 3e6700bfce3ba480814f3837011c5f8f7107bbd5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781228"
---
# <a name="strongnamehashsize-function"></a><span data-ttu-id="6e70a-103">StrongNameHashSize 函数</span><span class="sxs-lookup"><span data-stu-id="6e70a-103">StrongNameHashSize Function</span></span>

<span data-ttu-id="6e70a-104">使用指定的哈希算法获取哈希所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="6e70a-104">Gets the buffer size required for a hash, using the specified hash algorithm.</span></span>  
  
 <span data-ttu-id="6e70a-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="6e70a-105">This function has been deprecated.</span></span> <span data-ttu-id="6e70a-106">改为使用 [ICLRStrongName：： StrongNameHashSize](../hosting/iclrstrongname-strongnamehashsize-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6e70a-106">Use the [ICLRStrongName::StrongNameHashSize](../hosting/iclrstrongname-strongnamehashsize-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e70a-107">语法</span><span class="sxs-lookup"><span data-stu-id="6e70a-107">Syntax</span></span>  
  
```cpp  
BOOLEAN StrongNameHashSize (  
    [in]  ULONG   ulHashAlg,  
    [out] DWORD   *pcbSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6e70a-108">参数</span><span class="sxs-lookup"><span data-stu-id="6e70a-108">Parameters</span></span>  

 `ulHashAlg`  
 <span data-ttu-id="6e70a-109">中用于计算缓冲区大小的哈希算法。</span><span class="sxs-lookup"><span data-stu-id="6e70a-109">[in] The hash algorithm used to compute the buffer size.</span></span>  
  
 `pcbSize`  
 <span data-ttu-id="6e70a-110">弄返回的缓冲区大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="6e70a-110">[out] The returned buffer size, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6e70a-111">返回值</span><span class="sxs-lookup"><span data-stu-id="6e70a-111">Return Value</span></span>  

 <span data-ttu-id="6e70a-112">`true` 成功完成时;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="6e70a-112">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6e70a-113">备注</span><span class="sxs-lookup"><span data-stu-id="6e70a-113">Remarks</span></span>  

 <span data-ttu-id="6e70a-114">如果 `StrongNameHashSize` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。</span><span class="sxs-lookup"><span data-stu-id="6e70a-114">If the `StrongNameHashSize` function does not complete successfully, call the [StrongNameErrorInfo](strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6e70a-115">要求</span><span class="sxs-lookup"><span data-stu-id="6e70a-115">Requirements</span></span>  

 <span data-ttu-id="6e70a-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6e70a-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6e70a-117">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="6e70a-117">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="6e70a-118">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6e70a-118">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6e70a-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6e70a-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e70a-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="6e70a-120">See also</span></span>

- [<span data-ttu-id="6e70a-121">StrongNameHashSize 方法</span><span class="sxs-lookup"><span data-stu-id="6e70a-121">StrongNameHashSize Method</span></span>](../hosting/iclrstrongname-strongnamehashsize-method.md)
- [<span data-ttu-id="6e70a-122">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="6e70a-122">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
