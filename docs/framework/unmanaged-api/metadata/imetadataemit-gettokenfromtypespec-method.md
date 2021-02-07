---
description: 了解详细信息： IMetaDataEmit：： GetTokenFromTypeSpec 方法
title: IMetaDataEmit::GetTokenFromTypeSpec 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.GetTokenFromTypeSpec
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::GetTokenFromTypeSpec
helpviewer_keywords:
- GetTokenFromTypeSpec method [.NET Framework metadata]
- IMetaDataEmit::GetTokenFromTypeSpec method [.NET Framework metadata]
ms.assetid: 7de6447a-a751-49d8-87e2-951cee77b536
topic_type:
- apiref
ms.openlocfilehash: 09f7133af9b9d912b03cdc1c93744ee260c69169
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728231"
---
# <a name="imetadataemitgettokenfromtypespec-method"></a><span data-ttu-id="1021b-103">IMetaDataEmit::GetTokenFromTypeSpec 方法</span><span class="sxs-lookup"><span data-stu-id="1021b-103">IMetaDataEmit::GetTokenFromTypeSpec Method</span></span>

<span data-ttu-id="1021b-104">获取具有指定元数据签名的类型的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="1021b-104">Gets a metadata token for the type with the specified metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1021b-105">语法</span><span class="sxs-lookup"><span data-stu-id="1021b-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTokenFromTypeSpec (
    [in]  PCCOR_SIGNATURE       pvSig,
    [in]  ULONG                 cbSig,
    [out] mdTypeSpec            *ptypespec
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1021b-106">参数</span><span class="sxs-lookup"><span data-stu-id="1021b-106">Parameters</span></span>  

 `pvSig`  
 <span data-ttu-id="1021b-107">中要定义的签名。</span><span class="sxs-lookup"><span data-stu-id="1021b-107">[in] The signature being defined.</span></span>  
  
 `cbSig`  
 <span data-ttu-id="1021b-108">中中的字节数 `pvSig` 。</span><span class="sxs-lookup"><span data-stu-id="1021b-108">[in] The count of bytes in `pvSig`.</span></span>  
  
 `ptypespec`  
 <span data-ttu-id="1021b-109">弄 `mdTypeSpec` 分配的令牌。</span><span class="sxs-lookup"><span data-stu-id="1021b-109">[out] The `mdTypeSpec` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1021b-110">要求</span><span class="sxs-lookup"><span data-stu-id="1021b-110">Requirements</span></span>  

 <span data-ttu-id="1021b-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1021b-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1021b-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="1021b-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1021b-113">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="1021b-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1021b-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1021b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1021b-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="1021b-115">See also</span></span>

- [<span data-ttu-id="1021b-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="1021b-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="1021b-117">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="1021b-117">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
