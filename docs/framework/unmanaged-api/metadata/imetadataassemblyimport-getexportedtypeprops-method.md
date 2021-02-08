---
description: 了解详细信息： IMetaDataAssemblyImport：： GetExportedTypeProps 方法
title: IMetaDataAssemblyImport::GetExportedTypeProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetExportedTypeProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetExportedTypeProps
helpviewer_keywords:
- GetExportedTypeProps method [.NET Framework metadata]
- IMetaDataAssemblyImport::GetExportedTypeProps method [.NET Framework metadata]
ms.assetid: 25ca7623-5a55-4f09-b44a-36b03d142278
topic_type:
- apiref
ms.openlocfilehash: 894fb65fb6de76a218489b2a85a2d3c20c572789
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784114"
---
# <a name="imetadataassemblyimportgetexportedtypeprops-method"></a><span data-ttu-id="2aa51-103">IMetaDataAssemblyImport::GetExportedTypeProps 方法</span><span class="sxs-lookup"><span data-stu-id="2aa51-103">IMetaDataAssemblyImport::GetExportedTypeProps Method</span></span>

<span data-ttu-id="2aa51-104">获取具有指定元数据签名的导出类型的属性集。</span><span class="sxs-lookup"><span data-stu-id="2aa51-104">Gets the set of properties of the exported type with the specified metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2aa51-105">语法</span><span class="sxs-lookup"><span data-stu-id="2aa51-105">Syntax</span></span>  
  
```cpp  
HRESULT GetExportedTypeProps (  
    [in]  mdExportedType    mdct,
    [out] LPWSTR            szName,
    [in]  ULONG             cchName,
    [out] ULONG             *pchName,
    [out] mdToken           *ptkImplementation,
    [out] mdTypeDef         *ptkTypeDef,
    [out] DWORD             *pdwExportedTypeFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2aa51-106">参数</span><span class="sxs-lookup"><span data-stu-id="2aa51-106">Parameters</span></span>  

 `mdct`  
 <span data-ttu-id="2aa51-107">中 `mdExportedType` 表示导出类型的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="2aa51-107">[in] An `mdExportedType` metadata token that represents the exported type.</span></span>  
  
 `szName`  
 <span data-ttu-id="2aa51-108">弄导出的类型的名称。</span><span class="sxs-lookup"><span data-stu-id="2aa51-108">[out] The name of the exported type.</span></span>  
  
 `cchName`  
 <span data-ttu-id="2aa51-109">中的大小（宽字符） `szName` 。</span><span class="sxs-lookup"><span data-stu-id="2aa51-109">[in] The size, in wide characters, of `szName`.</span></span>  
  
 `pchName`  
 <span data-ttu-id="2aa51-110">弄实际返回的宽字符数 `szName`</span><span class="sxs-lookup"><span data-stu-id="2aa51-110">[out] The number of wide characters actually returned in `szName`</span></span>  
  
 `ptkImplementation`  
 <span data-ttu-id="2aa51-111">弄 `mdFile`、或 `mdAssemblyRef` `mdExportedType` 元数据标记，其中包含或允许访问导出的类型的属性。</span><span class="sxs-lookup"><span data-stu-id="2aa51-111">[out] An `mdFile`, `mdAssemblyRef`, or `mdExportedType` metadata token that contains or allows access to the properties of the exported type.</span></span>  
  
 `ptkTypeDef`  
 <span data-ttu-id="2aa51-112">弄一个指针，指向 `mdTypeDef` 表示文件中的类型的标记。</span><span class="sxs-lookup"><span data-stu-id="2aa51-112">[out] A pointer to an `mdTypeDef` token that represents a type in the file.</span></span>  
  
 `pdwExportedTypeFlags`  
 <span data-ttu-id="2aa51-113">弄一个指针，指向用于描述应用于导出类型的元数据的标志。</span><span class="sxs-lookup"><span data-stu-id="2aa51-113">[out] A pointer to the flags that describe the metadata applied to the exported type.</span></span> <span data-ttu-id="2aa51-114">Flags 值可以是一个或多个 [CorTypeAttr](cortypeattr-enumeration.md) 值。</span><span class="sxs-lookup"><span data-stu-id="2aa51-114">The flags value can be one or more [CorTypeAttr](cortypeattr-enumeration.md) values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2aa51-115">要求</span><span class="sxs-lookup"><span data-stu-id="2aa51-115">Requirements</span></span>  

 <span data-ttu-id="2aa51-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2aa51-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2aa51-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="2aa51-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="2aa51-118">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="2aa51-118">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="2aa51-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2aa51-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2aa51-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="2aa51-120">See also</span></span>

- [<span data-ttu-id="2aa51-121">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="2aa51-121">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
