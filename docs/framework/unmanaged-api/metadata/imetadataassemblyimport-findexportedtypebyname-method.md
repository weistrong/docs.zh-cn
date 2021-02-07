---
description: 了解详细信息： IMetaDataAssemblyImport：： FindExportedTypeByName 方法
title: IMetaDataAssemblyImport::FindExportedTypeByName 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.FindExportedTypeByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::FindExportedTypeByName
helpviewer_keywords:
- FindExportedTypeByName method [.NET Framework metadata]
- IMetaDataAssemblyImport::FindExportedTypeByName method [.NET Framework metadata]
ms.assetid: 46264b2c-574d-4dde-aafc-77187a104fdd
topic_type:
- apiref
ms.openlocfilehash: 4a2dc2b65b7f7fe6d5f2e120c635214d457991bc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677979"
---
# <a name="imetadataassemblyimportfindexportedtypebyname-method"></a><span data-ttu-id="0223d-103">IMetaDataAssemblyImport::FindExportedTypeByName 方法</span><span class="sxs-lookup"><span data-stu-id="0223d-103">IMetaDataAssemblyImport::FindExportedTypeByName Method</span></span>

<span data-ttu-id="0223d-104">获取一个指针，该指针指向导出的类型（给定其名称和封闭类型）。</span><span class="sxs-lookup"><span data-stu-id="0223d-104">Gets a pointer to an exported type, given its name and enclosing type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0223d-105">语法</span><span class="sxs-lookup"><span data-stu-id="0223d-105">Syntax</span></span>  
  
```cpp  
HRESULT FindExportedTypeByName (  
    [in]  LPCWSTR           szName,
    [in]  mdToken           mdtExportedType,
    [out] mdExportedType    *ptkExportedType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0223d-106">参数</span><span class="sxs-lookup"><span data-stu-id="0223d-106">Parameters</span></span>  

 `szName`  
 <span data-ttu-id="0223d-107">中导出的类型的名称。</span><span class="sxs-lookup"><span data-stu-id="0223d-107">[in] The name of the exported type.</span></span>  
  
 `mdtExportedType`  
 <span data-ttu-id="0223d-108">中导出类型的封闭类的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="0223d-108">[in] The metadata token for the enclosing class of the exported type.</span></span> <span data-ttu-id="0223d-109">`mdExportedTypeNil`如果请求的导出类型不是嵌套类型，则此值为。</span><span class="sxs-lookup"><span data-stu-id="0223d-109">This value is `mdExportedTypeNil` if the requested exported type is not a nested type.</span></span>  
  
 `ptkExportedType`  
 <span data-ttu-id="0223d-110">弄一个指针，指向 `mdExportedType` 表示导出类型的标记。</span><span class="sxs-lookup"><span data-stu-id="0223d-110">[out] A pointer to the `mdExportedType` token that represents the exported type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0223d-111">备注</span><span class="sxs-lookup"><span data-stu-id="0223d-111">Remarks</span></span>  

 <span data-ttu-id="0223d-112">`FindExportedTypeByName`方法使用公共语言运行时所使用的标准规则来解析引用。</span><span class="sxs-lookup"><span data-stu-id="0223d-112">The `FindExportedTypeByName` method uses the standard rules employed by the common language runtime for resolving references.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0223d-113">要求</span><span class="sxs-lookup"><span data-stu-id="0223d-113">Requirements</span></span>  

 <span data-ttu-id="0223d-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0223d-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0223d-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="0223d-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0223d-116">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="0223d-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="0223d-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0223d-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0223d-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="0223d-118">See also</span></span>

- [<span data-ttu-id="0223d-119">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="0223d-119">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
- [<span data-ttu-id="0223d-120">运行时如何定位程序集</span><span class="sxs-lookup"><span data-stu-id="0223d-120">How the Runtime Locates Assemblies</span></span>](../../deployment/how-the-runtime-locates-assemblies.md)
