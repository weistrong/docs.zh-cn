---
description: 了解详细信息： IMetaDataAssemblyImport：： EnumFiles 方法
title: IMetaDataAssemblyImport::EnumFiles 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.EnumFiles
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::EnumFiles
helpviewer_keywords:
- IMetaDataAssemblyImport::EnumFiles method [.NET Framework metadata]
- EnumFiles method [.NET Framework metadata]
ms.assetid: f0d721e2-b946-426d-8e20-9124bd04e4cb
topic_type:
- apiref
ms.openlocfilehash: 25282edd081e937e4c84334f9f004e201b9db46f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671017"
---
# <a name="imetadataassemblyimportenumfiles-method"></a><span data-ttu-id="5fbee-103">IMetaDataAssemblyImport::EnumFiles 方法</span><span class="sxs-lookup"><span data-stu-id="5fbee-103">IMetaDataAssemblyImport::EnumFiles Method</span></span>

<span data-ttu-id="5fbee-104">枚举当前程序集清单中引用的文件。</span><span class="sxs-lookup"><span data-stu-id="5fbee-104">Enumerates the files referenced in the current assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5fbee-105">语法</span><span class="sxs-lookup"><span data-stu-id="5fbee-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumFiles (  
    [in, out] HCORENUM    *phEnum,
    [out] mdFile          rFiles[],
    [in]  ULONG           cMax,
    [out] ULONG           *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5fbee-106">参数</span><span class="sxs-lookup"><span data-stu-id="5fbee-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="5fbee-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="5fbee-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="5fbee-108">第一次调用此方法时，此值必须为 null 值。</span><span class="sxs-lookup"><span data-stu-id="5fbee-108">This must be a null value for the first call of this method.</span></span>  
  
 `rFiles`  
 <span data-ttu-id="5fbee-109">弄用于存储 `mdFile` 元数据标记的数组。</span><span class="sxs-lookup"><span data-stu-id="5fbee-109">[out] The array used to store the `mdFile` metadata tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="5fbee-110">中可以放入的标记的最大数目 `mdFile` `rFiles` 。</span><span class="sxs-lookup"><span data-stu-id="5fbee-110">[in] The maximum number of `mdFile` tokens that can be placed in `rFiles`.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="5fbee-111">弄 `mdFile` 实际置于中的标记数 `rFiles` 。</span><span class="sxs-lookup"><span data-stu-id="5fbee-111">[out] The number of `mdFile` tokens actually placed in `rFiles`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5fbee-112">返回值</span><span class="sxs-lookup"><span data-stu-id="5fbee-112">Return Value</span></span>  
  
|<span data-ttu-id="5fbee-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="5fbee-113">HRESULT</span></span>|<span data-ttu-id="5fbee-114">说明</span><span class="sxs-lookup"><span data-stu-id="5fbee-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="5fbee-115">`EnumFiles` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="5fbee-115">`EnumFiles` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="5fbee-116">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="5fbee-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="5fbee-117">在这种情况下， `pcTokens` 设置为零。</span><span class="sxs-lookup"><span data-stu-id="5fbee-117">In this case, `pcTokens` is set to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5fbee-118">要求</span><span class="sxs-lookup"><span data-stu-id="5fbee-118">Requirements</span></span>  

 <span data-ttu-id="5fbee-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5fbee-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5fbee-120">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="5fbee-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5fbee-121">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="5fbee-121">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="5fbee-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5fbee-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5fbee-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="5fbee-123">See also</span></span>

- [<span data-ttu-id="5fbee-124">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="5fbee-124">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
