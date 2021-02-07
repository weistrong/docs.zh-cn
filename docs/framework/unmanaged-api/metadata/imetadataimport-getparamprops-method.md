---
description: 了解详细信息： IMetaDataImport：： GetParamProps 方法
title: IMetaDataImport::GetParamProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetParamProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetParamProps
helpviewer_keywords:
- IMetaDataImport::GetParamProps method [.NET Framework metadata]
- GetParamProps method [.NET Framework metadata]
ms.assetid: 4d5e5f00-bcab-4f41-b191-176511a186a7
topic_type:
- apiref
ms.openlocfilehash: 2c48215836dfb3ae44edc9a2bf10d4028fd82bb3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728114"
---
# <a name="imetadataimportgetparamprops-method"></a><span data-ttu-id="ccdb0-103">IMetaDataImport::GetParamProps 方法</span><span class="sxs-lookup"><span data-stu-id="ccdb0-103">IMetaDataImport::GetParamProps Method</span></span>

<span data-ttu-id="ccdb0-104">获取指定的 ParamDef 标记所引用的参数的元数据值。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-104">Gets metadata values for the parameter referenced by the specified ParamDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ccdb0-105">语法</span><span class="sxs-lookup"><span data-stu-id="ccdb0-105">Syntax</span></span>  
  
```cpp  
HRESULT GetParamProps (  
   [in]  mdParamDef      tk,  
   [out] mdMethodDef     *pmd,  
   [out] ULONG           *pulSequence,  
   [out] LPWSTR          szName,  
   [in]  ULONG           cchName,  
   [out] ULONG           *pchName,  
   [out] DWORD           *pdwAttr,  
   [out] DWORD           *pdwCPlusTypeFlag,  
   [out] UVCP_CONSTANT   *ppValue,  
   [out] ULONG           *pcchValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ccdb0-106">参数</span><span class="sxs-lookup"><span data-stu-id="ccdb0-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="ccdb0-107">中一个 ParamDef 标记，它表示要为其返回元数据的参数。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-107">[in] A ParamDef token that represents the parameter to return metadata for.</span></span>  
  
 `pmd`  
 <span data-ttu-id="ccdb0-108">弄指向 MethodDef 标记的指针，该标记表示采用参数的方法。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-108">[out] A pointer to a MethodDef token representing the method that takes the parameter.</span></span>  
  
 `pulSequence`  
 <span data-ttu-id="ccdb0-109">弄参数在方法自变量列表中的序号位置。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-109">[out] The ordinal position of the parameter in the method argument list.</span></span>  
  
 `szName`  
 <span data-ttu-id="ccdb0-110">弄用于保存参数名称的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-110">[out] A buffer to hold the name of the parameter.</span></span>  
  
 `cchName`  
 <span data-ttu-id="ccdb0-111">中请求的大小（以宽字符为大小） `szName` 。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-111">[in] The requested size in wide characters of `szName`.</span></span>  
  
 `pchName`  
 <span data-ttu-id="ccdb0-112">弄返回的宽字符大小 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-112">[out] The returned size in wide characters of `szName`.</span></span>  
  
 `pdwAttr`  
 <span data-ttu-id="ccdb0-113">弄指向与参数关联的任何特性标志的指针。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-113">[out] A pointer to any attribute flags associated with the parameter.</span></span> <span data-ttu-id="ccdb0-114">这是一个值的位掩码 `CorParamAttr` 。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-114">This is a bitmask of `CorParamAttr` values.</span></span>  
  
 `pdwCPlusTypeFlag`  
 <span data-ttu-id="ccdb0-115">弄指向标志的指针，该标志指定参数为 <xref:System.ValueType> 。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-115">[out] A pointer to a flag specifying that the parameter is a <xref:System.ValueType>.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="ccdb0-116">弄指向参数返回的常量字符串的指针。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-116">[out] A pointer to a constant string returned by the parameter.</span></span>  
  
 `pcchValue`  
 <span data-ttu-id="ccdb0-117">弄以宽字符为大小的大小 `ppValue` ; 如果不包含字符串，则为零 `ppValue` 。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-117">[out] The size of `ppValue` in wide characters, or zero if `ppValue` does not hold a string.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ccdb0-118">备注</span><span class="sxs-lookup"><span data-stu-id="ccdb0-118">Remarks</span></span>

<span data-ttu-id="ccdb0-119">参数的序列值 `pulSequence` 从1开始。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-119">The sequence values in `pulSequence` begin with 1 for parameters.</span></span> <span data-ttu-id="ccdb0-120">返回值的序列号为0。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-120">A return value has a sequence number of 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccdb0-121">要求</span><span class="sxs-lookup"><span data-stu-id="ccdb0-121">Requirements</span></span>  

 <span data-ttu-id="ccdb0-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ccdb0-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ccdb0-123">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="ccdb0-123">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ccdb0-124">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ccdb0-124">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ccdb0-125">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ccdb0-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ccdb0-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="ccdb0-126">See also</span></span>

- [<span data-ttu-id="ccdb0-127">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="ccdb0-127">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="ccdb0-128">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="ccdb0-128">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
