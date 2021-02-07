---
description: 了解详细信息： IMetaDataImport：： GetNestedClassProps 方法
title: IMetaDataImport::GetNestedClassProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetNestedClassProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetNestedClassProps
helpviewer_keywords:
- GetNestedClassProps method [.NET Framework metadata]
- IMetaDataImport::GetNestedClassProps method [.NET Framework metadata]
ms.assetid: 704d19f1-bdef-4745-af8c-6476eb246fb3
topic_type:
- apiref
ms.openlocfilehash: 5fd812bf9b7725d520b14284db400bb50e82c25b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677530"
---
# <a name="imetadataimportgetnestedclassprops-method"></a><span data-ttu-id="20c2e-103">IMetaDataImport::GetNestedClassProps 方法</span><span class="sxs-lookup"><span data-stu-id="20c2e-103">IMetaDataImport::GetNestedClassProps Method</span></span>

<span data-ttu-id="20c2e-104">获取指定嵌套类型的父级的 TypeDef 标记 <xref:System.Type> 。</span><span class="sxs-lookup"><span data-stu-id="20c2e-104">Gets the TypeDef token for the parent <xref:System.Type> of the specified nested type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20c2e-105">语法</span><span class="sxs-lookup"><span data-stu-id="20c2e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNestedClassProps (  
   [in]   mdTypeDef      tdNestedClass,  
   [out]  mdTypeDef      *ptdEnclosingClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="20c2e-106">参数</span><span class="sxs-lookup"><span data-stu-id="20c2e-106">Parameters</span></span>  

 `tdNestedClass`  
 <span data-ttu-id="20c2e-107">中一个 TypeDef 标记，它表示 <xref:System.Type> 要为其返回父类标记的。</span><span class="sxs-lookup"><span data-stu-id="20c2e-107">[in] A TypeDef token representing the <xref:System.Type> to return the parent class token for.</span></span>  
  
 `ptdEnclosingClass`  
 <span data-ttu-id="20c2e-108">弄一个指针，指向 <xref:System.Type> 嵌套在中的的 TypeDef 标记 `tdNestedClass` 。</span><span class="sxs-lookup"><span data-stu-id="20c2e-108">[out] A pointer to the TypeDef token for the <xref:System.Type> that `tdNestedClass` is nested in.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="20c2e-109">要求</span><span class="sxs-lookup"><span data-stu-id="20c2e-109">Requirements</span></span>  

 <span data-ttu-id="20c2e-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="20c2e-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20c2e-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="20c2e-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="20c2e-112">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="20c2e-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="20c2e-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="20c2e-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20c2e-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="20c2e-114">See also</span></span>

- [<span data-ttu-id="20c2e-115">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="20c2e-115">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="20c2e-116">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="20c2e-116">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
