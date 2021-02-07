---
description: 了解详细信息： IMetaDataImport：： FindTypeRef 方法
title: IMetaDataImport::FindTypeRef 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.FindTypeRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::FindTypeRef
helpviewer_keywords:
- IMetaDataImport::FindTypeRef method [.NET Framework metadata]
- FindTypeRef method [.NET Framework metadata]
ms.assetid: 1b2bbf3f-943e-412e-b66c-e802431b055c
topic_type:
- apiref
ms.openlocfilehash: 11e966256b5e75c1acff0bf1e6de0c96dc03e6aa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745562"
---
# <a name="imetadataimportfindtyperef-method"></a><span data-ttu-id="687a8-103">IMetaDataImport::FindTypeRef 方法</span><span class="sxs-lookup"><span data-stu-id="687a8-103">IMetaDataImport::FindTypeRef Method</span></span>

<span data-ttu-id="687a8-104">获取一个指针，该指针指向 <xref:System.Type> 指定范围内且具有指定名称的引用的 TypeRef 标记。</span><span class="sxs-lookup"><span data-stu-id="687a8-104">Gets a pointer to the TypeRef token for the <xref:System.Type> reference that is in the specified scope and that has the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="687a8-105">语法</span><span class="sxs-lookup"><span data-stu-id="687a8-105">Syntax</span></span>  
  
```cpp  
HRESULT FindTypeRef (  
   [in] mdToken        tkResolutionScope,  
   [in]  LPCWSTR       szName,  
   [out] mdTypeRef     *ptr  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="687a8-106">参数</span><span class="sxs-lookup"><span data-stu-id="687a8-106">Parameters</span></span>  

 `tkResolutionScope`  
 <span data-ttu-id="687a8-107">中一个 ModuleRef、AssemblyRef 或 TypeRef 标记，分别指定定义了类型引用的模块、程序集或类型。</span><span class="sxs-lookup"><span data-stu-id="687a8-107">[in] A ModuleRef, AssemblyRef, or TypeRef token that specifies the module, assembly, or type, respectively, in which the type reference is defined.</span></span>  
  
 `szName`  
 <span data-ttu-id="687a8-108">中要搜索的类型引用的名称。</span><span class="sxs-lookup"><span data-stu-id="687a8-108">[in] The name of the type reference to search for.</span></span>  
  
 `ptr`  
 <span data-ttu-id="687a8-109">弄指向匹配的 TypeRef 标记的指针。</span><span class="sxs-lookup"><span data-stu-id="687a8-109">[out] A pointer to the matching TypeRef token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="687a8-110">要求</span><span class="sxs-lookup"><span data-stu-id="687a8-110">Requirements</span></span>  

 <span data-ttu-id="687a8-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="687a8-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="687a8-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="687a8-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="687a8-113">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="687a8-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="687a8-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="687a8-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="687a8-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="687a8-115">See also</span></span>

- [<span data-ttu-id="687a8-116">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="687a8-116">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="687a8-117">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="687a8-117">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
