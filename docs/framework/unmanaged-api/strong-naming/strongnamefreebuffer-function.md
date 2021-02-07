---
description: 了解详细信息： StrongNameFreeBuffer 函数
title: StrongNameFreeBuffer 函数
ms.date: 03/30/2017
api_name:
- StrongNameFreeBuffer
api_location:
- mscoree.dll
- mscorsn.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameFreeBuffer
helpviewer_keywords:
- StrongNameFreeBuffer function [.NET Framework strong naming]
ms.assetid: eda21ecf-4734-4f92-aaba-9f34884385db
topic_type:
- apiref
ms.openlocfilehash: fa1b1d7710a981c5284ee79d551cbf51ede285db
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736448"
---
# <a name="strongnamefreebuffer-function"></a><span data-ttu-id="6f298-103">StrongNameFreeBuffer 函数</span><span class="sxs-lookup"><span data-stu-id="6f298-103">StrongNameFreeBuffer Function</span></span>

<span data-ttu-id="6f298-104">释放先前调用 [StrongNameGetPublicKey](strongnamegetpublickey-function.md)、[StrongNameTokenFromPublicKey](strongnametokenfrompublickey-function.md) 或 [StrongNameSignatureGeneration](strongnamesignaturegeneration-function.md) 强名称函数分配的内存。</span><span class="sxs-lookup"><span data-stu-id="6f298-104">Frees memory that was allocated with a previous call to a strong name function such as [StrongNameGetPublicKey](strongnamegetpublickey-function.md), [StrongNameTokenFromPublicKey](strongnametokenfrompublickey-function.md), or [StrongNameSignatureGeneration](strongnamesignaturegeneration-function.md).</span></span>  
  
 <span data-ttu-id="6f298-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="6f298-105">This function has been deprecated.</span></span> <span data-ttu-id="6f298-106">改为使用 [ICLRStrongName：： StrongNameFreeBuffer](../hosting/iclrstrongname-strongnamefreebuffer-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6f298-106">Use the [ICLRStrongName::StrongNameFreeBuffer](../hosting/iclrstrongname-strongnamefreebuffer-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6f298-107">语法</span><span class="sxs-lookup"><span data-stu-id="6f298-107">Syntax</span></span>  
  
```cpp  
VOID StrongNameFreeBuffer (
   [in] BYTE   *pbMemory  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6f298-108">参数</span><span class="sxs-lookup"><span data-stu-id="6f298-108">Parameters</span></span>  

 `pbMemory`  
 <span data-ttu-id="6f298-109">中指向要释放的内存的指针。</span><span class="sxs-lookup"><span data-stu-id="6f298-109">[in] A pointer to the memory to free.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6f298-110">要求</span><span class="sxs-lookup"><span data-stu-id="6f298-110">Requirements</span></span>  

 <span data-ttu-id="6f298-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6f298-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6f298-112">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="6f298-112">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="6f298-113">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6f298-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6f298-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6f298-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f298-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="6f298-115">See also</span></span>

- [<span data-ttu-id="6f298-116">StrongNameFreeBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="6f298-116">StrongNameFreeBuffer Method</span></span>](../hosting/iclrstrongname-strongnamefreebuffer-method.md)
- [<span data-ttu-id="6f298-117">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="6f298-117">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
