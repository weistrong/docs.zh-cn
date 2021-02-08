---
description: 了解详细信息： IMetaDataEmit：： GetTokenFromSig 方法
title: IMetaDataEmit::GetTokenFromSig 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.GetTokenFromSig
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::GetTokenFromSig
helpviewer_keywords:
- IMetaDataEmit::GetTokenFromSig method [.NET Framework metadata]
- GetTokenFromSig method [.NET Framework metadata]
ms.assetid: 50a58a83-6287-40a4-b315-47823cea0a5c
topic_type:
- apiref
ms.openlocfilehash: 3b9b38389a2bf78a65baa2cf96e3a422c54d0bcb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783919"
---
# <a name="imetadataemitgettokenfromsig-method"></a><span data-ttu-id="f1ae7-103">IMetaDataEmit::GetTokenFromSig 方法</span><span class="sxs-lookup"><span data-stu-id="f1ae7-103">IMetaDataEmit::GetTokenFromSig Method</span></span>

<span data-ttu-id="f1ae7-104">获取指定元数据签名的令牌。</span><span class="sxs-lookup"><span data-stu-id="f1ae7-104">Gets a token for the specified metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1ae7-105">语法</span><span class="sxs-lookup"><span data-stu-id="f1ae7-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTokenFromSig (
    [in]  PCCOR_SIGNATURE pvSig,
    [in]  ULONG       cbSig,
    [out] mdSignature *pmsig
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f1ae7-106">参数</span><span class="sxs-lookup"><span data-stu-id="f1ae7-106">Parameters</span></span>  

 `pvSig`  
 <span data-ttu-id="f1ae7-107">中要保持和存储的签名。</span><span class="sxs-lookup"><span data-stu-id="f1ae7-107">[in] The signature to be persisted and stored.</span></span>  
  
 `cbSig`  
 <span data-ttu-id="f1ae7-108">中中的字节数 `pvSig` 。</span><span class="sxs-lookup"><span data-stu-id="f1ae7-108">[in] The count of bytes in `pvSig`.</span></span>  
  
 `pmsig`  
 <span data-ttu-id="f1ae7-109">弄 `mdSignature` 分配的令牌。</span><span class="sxs-lookup"><span data-stu-id="f1ae7-109">[out] The `mdSignature` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f1ae7-110">要求</span><span class="sxs-lookup"><span data-stu-id="f1ae7-110">Requirements</span></span>  

 <span data-ttu-id="f1ae7-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f1ae7-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f1ae7-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f1ae7-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f1ae7-113">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="f1ae7-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f1ae7-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f1ae7-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1ae7-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="f1ae7-115">See also</span></span>

- [<span data-ttu-id="f1ae7-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="f1ae7-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="f1ae7-117">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="f1ae7-117">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
