---
description: 了解详细信息： IMetaDataImport：： FindTypeDefByName 方法
title: IMetaDataImport::FindTypeDefByName 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.FindTypeDefByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::FindTypeDefByName
helpviewer_keywords:
- FindTypeDefByName method [.NET Framework metadata]
- IMetaDataImport::FindTypeDefByName method [.NET Framework metadata]
ms.assetid: f4c2cd88-ac28-4bad-9ab1-2cf9d2de41e6
topic_type:
- apiref
ms.openlocfilehash: 083f786cc03b83cda54497937e376baa4a2cbee3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789224"
---
# <a name="imetadataimportfindtypedefbyname-method"></a><span data-ttu-id="8a4f0-103">IMetaDataImport::FindTypeDefByName 方法</span><span class="sxs-lookup"><span data-stu-id="8a4f0-103">IMetaDataImport::FindTypeDefByName Method</span></span>

<span data-ttu-id="8a4f0-104">获取一个指针，该指针指向具有指定名称的的 TypeDef 元数据标记 <xref:System.Type> 。</span><span class="sxs-lookup"><span data-stu-id="8a4f0-104">Gets a pointer to the TypeDef metadata token for the <xref:System.Type> with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a4f0-105">语法</span><span class="sxs-lookup"><span data-stu-id="8a4f0-105">Syntax</span></span>  
  
```cpp  
HRESULT FindTypeDefByName  
   [in]  LPCWSTR       szTypeDef,  
   [in]  mdToken       tkEnclosingClass,  
   [out] mdTypeDef     *ptd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8a4f0-106">参数</span><span class="sxs-lookup"><span data-stu-id="8a4f0-106">Parameters</span></span>  

 `szTypeDef`  
 <span data-ttu-id="8a4f0-107">中要为其获取 TypeDef 标记的类型的名称。</span><span class="sxs-lookup"><span data-stu-id="8a4f0-107">[in] The name of the type for which to get the TypeDef token.</span></span>  
  
 `tkEnclosingClass`  
 <span data-ttu-id="8a4f0-108">中表示封闭类的 TypeDef 或 TypeRef 标记。</span><span class="sxs-lookup"><span data-stu-id="8a4f0-108">[in] A TypeDef or TypeRef token representing the enclosing class.</span></span> <span data-ttu-id="8a4f0-109">如果要查找的类型不是嵌套类，请将此值设置为 NULL。</span><span class="sxs-lookup"><span data-stu-id="8a4f0-109">If the type to find is not a nested class, set this value to NULL.</span></span>  
  
 `ptd`  
 <span data-ttu-id="8a4f0-110">弄指向匹配的 TypeDef 标记的指针。</span><span class="sxs-lookup"><span data-stu-id="8a4f0-110">[out] A pointer to the matching TypeDef token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a4f0-111">要求</span><span class="sxs-lookup"><span data-stu-id="8a4f0-111">Requirements</span></span>  

 <span data-ttu-id="8a4f0-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8a4f0-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a4f0-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="8a4f0-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8a4f0-114">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8a4f0-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="8a4f0-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a4f0-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a4f0-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="8a4f0-116">See also</span></span>

- [<span data-ttu-id="8a4f0-117">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="8a4f0-117">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="8a4f0-118">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="8a4f0-118">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
