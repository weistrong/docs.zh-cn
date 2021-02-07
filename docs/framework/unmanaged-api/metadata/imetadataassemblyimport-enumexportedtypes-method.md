---
description: 了解详细信息： IMetaDataAssemblyImport：： EnumExportedTypes 方法
title: IMetaDataAssemblyImport::EnumExportedTypes 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.EnumExportedTypes
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::EnumExportedTypes
helpviewer_keywords:
- EnumExportedTypes method [.NET Framework metadata]
- IMetaDataAssemblyImport::EnumExportedTypes method [.NET Framework metadata]
ms.assetid: e5912ed8-e4ce-438b-8ea3-d9e4c288d109
topic_type:
- apiref
ms.openlocfilehash: ecddcbd87586f5f61c57f8c04ea3bd68dc652839
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678024"
---
# <a name="imetadataassemblyimportenumexportedtypes-method"></a><span data-ttu-id="d1fcc-103">IMetaDataAssemblyImport::EnumExportedTypes 方法</span><span class="sxs-lookup"><span data-stu-id="d1fcc-103">IMetaDataAssemblyImport::EnumExportedTypes Method</span></span>

<span data-ttu-id="d1fcc-104">枚举当前元数据范围内的程序集清单中引用的导出类型。</span><span class="sxs-lookup"><span data-stu-id="d1fcc-104">Enumerates the exported types referenced in the assembly manifest in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1fcc-105">语法</span><span class="sxs-lookup"><span data-stu-id="d1fcc-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumExportedTypes (  
    [in, out] HCORENUM     *phEnum,
    [out] mdExportedType   rExportedTypes[],
    [in]  ULONG            cMax,
    [out] ULONG            *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d1fcc-106">参数</span><span class="sxs-lookup"><span data-stu-id="d1fcc-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="d1fcc-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="d1fcc-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="d1fcc-108">第一次调用方法时，此值必须为 null 值 `EnumExportedTypes` 。</span><span class="sxs-lookup"><span data-stu-id="d1fcc-108">This must be a null value when the `EnumExportedTypes` method is called for the first time.</span></span>  
  
 `rExportedTypes`  
 <span data-ttu-id="d1fcc-109">弄 `mdExportedType` 元数据标记的枚举。</span><span class="sxs-lookup"><span data-stu-id="d1fcc-109">[out] The enumeration of `mdExportedType` metadata tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="d1fcc-110">中 `mdExportedType` 可置于数组中的最大标记数 `rExportedTypes` 。</span><span class="sxs-lookup"><span data-stu-id="d1fcc-110">[in] The maximum number of `mdExportedType` tokens that can be placed in the `rExportedTypes` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="d1fcc-111">弄 `mdExportedType` 实际置于中的标记数 `rExportedTypes` 。</span><span class="sxs-lookup"><span data-stu-id="d1fcc-111">[out] The number of `mdExportedType` tokens actually placed in `rExportedTypes`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d1fcc-112">返回值</span><span class="sxs-lookup"><span data-stu-id="d1fcc-112">Return Value</span></span>  
  
|<span data-ttu-id="d1fcc-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d1fcc-113">HRESULT</span></span>|<span data-ttu-id="d1fcc-114">说明</span><span class="sxs-lookup"><span data-stu-id="d1fcc-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="d1fcc-115">`EnumExportedTypes` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="d1fcc-115">`EnumExportedTypes` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="d1fcc-116">没有要枚举的令牌。</span><span class="sxs-lookup"><span data-stu-id="d1fcc-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="d1fcc-117">在这种情况下， `pcTokens` 设置为零。</span><span class="sxs-lookup"><span data-stu-id="d1fcc-117">In this case, `pcTokens` is set to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d1fcc-118">要求</span><span class="sxs-lookup"><span data-stu-id="d1fcc-118">Requirements</span></span>  

 <span data-ttu-id="d1fcc-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d1fcc-119">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d1fcc-120">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="d1fcc-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d1fcc-121">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="d1fcc-121">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d1fcc-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d1fcc-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1fcc-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="d1fcc-123">See also</span></span>

- [<span data-ttu-id="d1fcc-124">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="d1fcc-124">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
