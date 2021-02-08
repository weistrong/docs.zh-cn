---
description: 了解详细信息： IMetaDataImport：： GetTypeDefProps 方法
title: IMetaDataImport::GetTypeDefProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetTypeDefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetTypeDefProps
helpviewer_keywords:
- GetTypeDefProps method [.NET Framework metadata]
- IMetaDataImport::GetTypeDefProps method [.NET Framework metadata]
ms.assetid: 00061a25-ba05-47a7-b984-fd916b06b149
topic_type:
- apiref
ms.openlocfilehash: da5c6117f636098ed0cfeddc541979d235729d63
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799263"
---
# <a name="imetadataimportgettypedefprops-method"></a><span data-ttu-id="c7268-103">IMetaDataImport::GetTypeDefProps 方法</span><span class="sxs-lookup"><span data-stu-id="c7268-103">IMetaDataImport::GetTypeDefProps Method</span></span>

<span data-ttu-id="c7268-104">返回 <xref:System.Type> 由指定的 TypeDef 标记所表示的的元数据信息。</span><span class="sxs-lookup"><span data-stu-id="c7268-104">Returns metadata information for the <xref:System.Type> represented by the specified TypeDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7268-105">语法</span><span class="sxs-lookup"><span data-stu-id="c7268-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTypeDefProps (  
   [in]  mdTypeDef   td,  
   [out] LPWSTR      szTypeDef,  
   [in]  ULONG       cchTypeDef,  
   [out] ULONG       *pchTypeDef,  
   [out] DWORD       *pdwTypeDefFlags,  
   [out] mdToken     *ptkExtends  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c7268-106">参数</span><span class="sxs-lookup"><span data-stu-id="c7268-106">Parameters</span></span>  

 `td`  
 <span data-ttu-id="c7268-107">中TypeDef 标记，它表示要为其返回元数据的类型。</span><span class="sxs-lookup"><span data-stu-id="c7268-107">[in] The TypeDef token that represents the type to return metadata for.</span></span>  
  
 `szTypeDef`  
 <span data-ttu-id="c7268-108">弄包含类型名称的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="c7268-108">[out] A buffer containing the type name.</span></span>  
  
 `cchTypeDef`  
 <span data-ttu-id="c7268-109">中的大小（以宽字符为大小） `szTypeDef` 。</span><span class="sxs-lookup"><span data-stu-id="c7268-109">[in] The size in wide characters of `szTypeDef`.</span></span>  
  
 `pchTypeDef`  
 <span data-ttu-id="c7268-110">弄返回的宽字符数 `szTypeDef` 。</span><span class="sxs-lookup"><span data-stu-id="c7268-110">[out] The number of wide characters returned in `szTypeDef`.</span></span>  
  
 `pdwTypeDefFlags`  
 <span data-ttu-id="c7268-111">弄指向修改类型定义的任何标志的指针。</span><span class="sxs-lookup"><span data-stu-id="c7268-111">[out] A pointer to any flags that modify the type definition.</span></span> <span data-ttu-id="c7268-112">此值是 [CorTypeAttr](cortypeattr-enumeration.md) 枚举中的位掩码。</span><span class="sxs-lookup"><span data-stu-id="c7268-112">This value is a bitmask from the [CorTypeAttr](cortypeattr-enumeration.md) enumeration.</span></span>  
  
 `ptkExtends`  
 <span data-ttu-id="c7268-113">弄一个 TypeDef 或 TypeRef 元数据标记，它表示所请求类型的基类型。</span><span class="sxs-lookup"><span data-stu-id="c7268-113">[out] A TypeDef or TypeRef metadata token that represents the base type of the requested type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c7268-114">要求</span><span class="sxs-lookup"><span data-stu-id="c7268-114">Requirements</span></span>  

 <span data-ttu-id="c7268-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c7268-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7268-116">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="c7268-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c7268-117">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c7268-117">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c7268-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7268-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7268-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="c7268-119">See also</span></span>

- [<span data-ttu-id="c7268-120">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="c7268-120">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="c7268-121">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="c7268-121">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
