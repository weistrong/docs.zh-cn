---
description: 了解详细信息： IMetaDataImport2：： GetGenericParamProps 方法
title: IMetaDataImport2::GetGenericParamProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetGenericParamProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetGenericParamProps
helpviewer_keywords:
- IMetaDataImport2::GetGenericParamProps method [.NET Framework metadata]
- GetGenericParamProps method [.NET Framework metadata]
ms.assetid: dbb21e67-712b-49e7-a27c-a1e73ffd46c5
topic_type:
- apiref
ms.openlocfilehash: 06b522531282b4a30cdc8ebf001c16438e8612ce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688723"
---
# <a name="imetadataimport2getgenericparamprops-method"></a><span data-ttu-id="881ca-103">IMetaDataImport2::GetGenericParamProps 方法</span><span class="sxs-lookup"><span data-stu-id="881ca-103">IMetaDataImport2::GetGenericParamProps Method</span></span>

<span data-ttu-id="881ca-104">获取与指定标记表示的泛型参数关联的元数据。</span><span class="sxs-lookup"><span data-stu-id="881ca-104">Gets the metadata associated with the generic parameter represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="881ca-105">语法</span><span class="sxs-lookup"><span data-stu-id="881ca-105">Syntax</span></span>  
  
```cpp  
HRESULT GetGenericParamProps (  
   [in]  mdGenericParam  gp,  
   [out] ULONG           *pulParamSeq,  
   [out] DWORD           *pdwParamFlags,  
   [out] mdToken         *ptOwner,  
   [out] DWORD           *reserved,  
   [out] LPWSTR          wzName,  
   [in]  ULONG           cchName,  
   [out] ULONG           *pchName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="881ca-106">参数</span><span class="sxs-lookup"><span data-stu-id="881ca-106">Parameters</span></span>  

 `gp`  
 <span data-ttu-id="881ca-107">中表示要为其返回元数据的泛型参数的标记。</span><span class="sxs-lookup"><span data-stu-id="881ca-107">[in] The token that represents the generic parameter for which to return metadata.</span></span>  
  
 `pulParamSeq`  
 <span data-ttu-id="881ca-108">弄 `Type` 参数在父构造函数或方法中的序号位置。</span><span class="sxs-lookup"><span data-stu-id="881ca-108">[out] The ordinal position of the `Type` parameter in the parent constructor or method.</span></span>  
  
 `pdwParamFlags`  
 <span data-ttu-id="881ca-109">弄用于描述泛型参数的的 [CorGenericParamAttr](corgenericparamattr-enumeration.md) 枚举的值 `Type` 。</span><span class="sxs-lookup"><span data-stu-id="881ca-109">[out] A value of the [CorGenericParamAttr](corgenericparamattr-enumeration.md) enumeration that describes the `Type` for the generic parameter.</span></span>  
  
 `ptOwner`  
 <span data-ttu-id="881ca-110">弄一个 TypeDef 或 MethodDef 标记，它表示参数的所有者。</span><span class="sxs-lookup"><span data-stu-id="881ca-110">[out] A TypeDef or MethodDef token that represents the owner of the parameter.</span></span>  
  
 `reserved`  
 <span data-ttu-id="881ca-111">弄保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="881ca-111">[out] Reserved for future extensibility.</span></span>  
  
 `wzName`  
 <span data-ttu-id="881ca-112">弄泛型参数的名称。</span><span class="sxs-lookup"><span data-stu-id="881ca-112">[out] The name of the generic parameter.</span></span>  
  
 `cchName`  
 <span data-ttu-id="881ca-113">中缓冲区的大小 `wzName` 。</span><span class="sxs-lookup"><span data-stu-id="881ca-113">[in] The size of the `wzName` buffer.</span></span>  
  
 `pchName`  
 <span data-ttu-id="881ca-114">弄以宽字符返回的名称的大小。</span><span class="sxs-lookup"><span data-stu-id="881ca-114">[out] The returned size of the name, in wide characters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="881ca-115">要求</span><span class="sxs-lookup"><span data-stu-id="881ca-115">Requirements</span></span>  

 <span data-ttu-id="881ca-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="881ca-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="881ca-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="881ca-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="881ca-118">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="881ca-118">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="881ca-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="881ca-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="881ca-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="881ca-120">See also</span></span>

- [<span data-ttu-id="881ca-121">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="881ca-121">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
- [<span data-ttu-id="881ca-122">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="881ca-122">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
