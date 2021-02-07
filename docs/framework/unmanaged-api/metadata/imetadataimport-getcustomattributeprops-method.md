---
description: 了解详细信息： IMetaDataImport：： GetCustomAttributeProps 方法
title: IMetaDataImport::GetCustomAttributeProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetCustomAttributeProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetCustomAttributeProps
helpviewer_keywords:
- GetCustomAttributeProps method [.NET Framework metadata]
- IMetaDataImport::GetCustomAttributeProps method [.NET Framework metadata]
ms.assetid: 6eefb243-a281-41c1-bcdc-7e17513bc446
topic_type:
- apiref
ms.openlocfilehash: 9bd8e83301252d7ead225146e562d3a58feb244a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745358"
---
# <a name="imetadataimportgetcustomattributeprops-method"></a><span data-ttu-id="c95fd-103">IMetaDataImport::GetCustomAttributeProps 方法</span><span class="sxs-lookup"><span data-stu-id="c95fd-103">IMetaDataImport::GetCustomAttributeProps Method</span></span>

<span data-ttu-id="c95fd-104">获取给定元数据标记的自定义属性的值。</span><span class="sxs-lookup"><span data-stu-id="c95fd-104">Gets the value of the custom attribute, given its metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c95fd-105">语法</span><span class="sxs-lookup"><span data-stu-id="c95fd-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCustomAttributeProps (  
   [in]            mdCustomAttribute   cv,  
   [out, optional] mdToken             *ptkObj,  
   [out, optional] mdToken             *ptkType,  
   [out, optional] void const          **ppBlob,  
   [out, optional] ULONG               *pcbSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c95fd-106">参数</span><span class="sxs-lookup"><span data-stu-id="c95fd-106">Parameters</span></span>  

 `cv`  
 <span data-ttu-id="c95fd-107">[in] 表示要检索的自定义属性的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="c95fd-107">[in] A metadata token that represents the custom attribute to be retrieved.</span></span>  
  
 `ptkObj`  
 <span data-ttu-id="c95fd-108">[out, optional] 表示自定义属性修改的对象的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="c95fd-108">[out, optional] A metadata token representing the object that the custom attribute modifies.</span></span> <span data-ttu-id="c95fd-109">此值可为任何类型的元数据标记（`mdCustomAttribute` 除外）。</span><span class="sxs-lookup"><span data-stu-id="c95fd-109">This value can be any type of metadata token except `mdCustomAttribute`.</span></span>  
  
 `ptkType`  
 <span data-ttu-id="c95fd-110">[out, optional] 表示已返回自定义属性的 <xref:System.Type> 的 `mdMethodDef` 或 `mdMemberRef` 元数据标记。</span><span class="sxs-lookup"><span data-stu-id="c95fd-110">[out, optional] An `mdMethodDef` or `mdMemberRef` metadata token representing the <xref:System.Type> of the returned custom attribute.</span></span>  
  
 `ppBlob`  
 <span data-ttu-id="c95fd-111">[out, optional] 指向自定义属性的值的数据数组指针。</span><span class="sxs-lookup"><span data-stu-id="c95fd-111">[out, optional] A pointer to an array of data that is the value of the custom attribute.</span></span>  
  
 `pcbSize`  
 <span data-ttu-id="c95fd-112">[out, optional] \*`ppBlob` 中返回的数据大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c95fd-112">[out, optional] The size in bytes of the data returned in \*`ppBlob`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c95fd-113">备注</span><span class="sxs-lookup"><span data-stu-id="c95fd-113">Remarks</span></span>  

 <span data-ttu-id="c95fd-114">自定义属性以元数据引擎理解的格式存储为数据数组。</span><span class="sxs-lookup"><span data-stu-id="c95fd-114">A custom attribute is stored as an array of data, the format which is understood by the metadata engine.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c95fd-115">要求</span><span class="sxs-lookup"><span data-stu-id="c95fd-115">Requirements</span></span>  

 <span data-ttu-id="c95fd-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c95fd-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c95fd-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="c95fd-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c95fd-118">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c95fd-118">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c95fd-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c95fd-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c95fd-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="c95fd-120">See also</span></span>

- [<span data-ttu-id="c95fd-121">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="c95fd-121">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="c95fd-122">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="c95fd-122">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
