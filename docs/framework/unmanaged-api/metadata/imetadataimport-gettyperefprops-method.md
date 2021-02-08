---
description: 了解详细信息： IMetaDataImport：： GetTypeRefProps 方法
title: IMetaDataImport::GetTypeRefProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetTypeRefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetTypeRefProps
helpviewer_keywords:
- IMetaDataImport::GetTypeRefProps method [.NET Framework metadata]
- GetTypeRefProps method [.NET Framework metadata]
ms.assetid: 01837955-ce1e-4068-b338-fd473bd77d1d
topic_type:
- apiref
ms.openlocfilehash: 8d4741ca2d04aaa4af48fee2cf6485de3403a525
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789120"
---
# <a name="imetadataimportgettyperefprops-method"></a><span data-ttu-id="0c1ac-103">IMetaDataImport::GetTypeRefProps 方法</span><span class="sxs-lookup"><span data-stu-id="0c1ac-103">IMetaDataImport::GetTypeRefProps Method</span></span>

<span data-ttu-id="0c1ac-104">获取与指定的 TypeRef 标记所引用的关联的元数据 <xref:System.Type> 。</span><span class="sxs-lookup"><span data-stu-id="0c1ac-104">Gets the metadata associated with the <xref:System.Type> referenced by the specified TypeRef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c1ac-105">语法</span><span class="sxs-lookup"><span data-stu-id="0c1ac-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTypeRefProps (  
   [in]  mdTypeRef   tr,  
   [out] mdToken     *ptkResolutionScope,  
   [out] LPWSTR      szName,  
   [in]  ULONG       cchName,  
   [out] ULONG       *pchName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0c1ac-106">参数</span><span class="sxs-lookup"><span data-stu-id="0c1ac-106">Parameters</span></span>  

 `tr`  
 <span data-ttu-id="0c1ac-107">中TypeRef 标记，它表示要为其返回元数据的类型。</span><span class="sxs-lookup"><span data-stu-id="0c1ac-107">[in] The TypeRef token that represents the type to return metadata for.</span></span>  
  
 `ptkResolutionScope`  
 <span data-ttu-id="0c1ac-108">弄指向在其中进行引用的范围的指针。</span><span class="sxs-lookup"><span data-stu-id="0c1ac-108">[out] A pointer to the scope in which the reference is made.</span></span> <span data-ttu-id="0c1ac-109">此值为 AssemblyRef 或 ModuleRef 标记。</span><span class="sxs-lookup"><span data-stu-id="0c1ac-109">This value is an AssemblyRef or ModuleRef token.</span></span>  
  
 `szName`  
 <span data-ttu-id="0c1ac-110">弄包含类型名称的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="0c1ac-110">[out] A buffer containing the type name.</span></span>  
  
 `cchName`  
 <span data-ttu-id="0c1ac-111">中请求的大小（以宽字符为大小） `szName` 。</span><span class="sxs-lookup"><span data-stu-id="0c1ac-111">[in] The requested size in wide characters of `szName`.</span></span>  
  
 `pchName`  
 <span data-ttu-id="0c1ac-112">弄返回的宽字符大小 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="0c1ac-112">[out] The returned size in wide characters of `szName`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c1ac-113">要求</span><span class="sxs-lookup"><span data-stu-id="0c1ac-113">Requirements</span></span>  

 <span data-ttu-id="0c1ac-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0c1ac-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c1ac-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="0c1ac-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0c1ac-116">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0c1ac-116">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="0c1ac-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c1ac-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c1ac-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="0c1ac-118">See also</span></span>

- [<span data-ttu-id="0c1ac-119">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="0c1ac-119">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="0c1ac-120">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="0c1ac-120">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
