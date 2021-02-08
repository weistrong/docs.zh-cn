---
description: 了解详细信息： IMetaDataImport：： FindField 方法
title: IMetaDataImport::FindField 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.FindField
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::FindField
helpviewer_keywords:
- IMetaDataImport::FindField method [.NET Framework metadata]
- FindField method [.NET Framework metadata]
ms.assetid: 38cd4e16-fbb2-471c-aa73-ac51a1931ad2
topic_type:
- apiref
ms.openlocfilehash: b8041a37b91f22722a05aec99c92c4f17c2b0610
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799299"
---
# <a name="imetadataimportfindfield-method"></a><span data-ttu-id="b73b7-103">IMetaDataImport::FindField 方法</span><span class="sxs-lookup"><span data-stu-id="b73b7-103">IMetaDataImport::FindField Method</span></span>

<span data-ttu-id="b73b7-104">获取一个指针，该指针指向由指定的括起来 <xref:System.Type> 且具有指定名称和元数据签名的字段的 FieldDef 标记。</span><span class="sxs-lookup"><span data-stu-id="b73b7-104">Gets a pointer to the FieldDef token for the field that is enclosed by the specified <xref:System.Type> and that has the specified name and metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b73b7-105">语法</span><span class="sxs-lookup"><span data-stu-id="b73b7-105">Syntax</span></span>  
  
```cpp  
HRESULT FindField (  
   [in]  mdTypeDef         td,  
   [in]  LPCWSTR           szName,  
   [in]  PCCOR_SIGNATURE   pvSigBlob,  
   [in]  ULONG             cbSigBlob,  
   [out] mdFieldDef        *pmb  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b73b7-106">参数</span><span class="sxs-lookup"><span data-stu-id="b73b7-106">Parameters</span></span>  

 `td`  
 <span data-ttu-id="b73b7-107">中包含要搜索的字段的类或接口的 TypeDef 标记。</span><span class="sxs-lookup"><span data-stu-id="b73b7-107">[in] The TypeDef token for the class or interface that encloses the field to search for.</span></span> <span data-ttu-id="b73b7-108">如果此值为 `mdTokenNil` ，则对全局变量执行查找。</span><span class="sxs-lookup"><span data-stu-id="b73b7-108">If this value is `mdTokenNil`, the lookup is done for a global variable.</span></span>  
  
 `szName`  
 <span data-ttu-id="b73b7-109">中要搜索的字段的名称。</span><span class="sxs-lookup"><span data-stu-id="b73b7-109">[in] The name of the field to search for.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="b73b7-110">中指向字段的二进制元数据签名的指针。</span><span class="sxs-lookup"><span data-stu-id="b73b7-110">[in] A pointer to the binary metadata signature of the field.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="b73b7-111">中的大小（以字节为单位） `pvSigBlob` 。</span><span class="sxs-lookup"><span data-stu-id="b73b7-111">[in] The size in bytes of `pvSigBlob`.</span></span>  
  
 `pmb`  
 <span data-ttu-id="b73b7-112">弄指向匹配的 FieldDef 标记的指针。</span><span class="sxs-lookup"><span data-stu-id="b73b7-112">[out] A pointer to the matching FieldDef token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b73b7-113">备注</span><span class="sxs-lookup"><span data-stu-id="b73b7-113">Remarks</span></span>  

 <span data-ttu-id="b73b7-114">您可以使用其封闭类或接口指定字段 (`td`) ，其名称 (`szName`) ，还可以指定其签名 (`pvSigBlob`) 。</span><span class="sxs-lookup"><span data-stu-id="b73b7-114">You specify the field using its enclosing class or interface (`td`), its name (`szName`), and optionally its signature (`pvSigBlob`).</span></span>  
  
 <span data-ttu-id="b73b7-115">传递给的签名 `FindField` 必须已在当前范围内生成，因为签名将绑定到特定范围。</span><span class="sxs-lookup"><span data-stu-id="b73b7-115">The signature passed to `FindField` must have been generated in the current scope, because signatures are bound to a particular scope.</span></span> <span data-ttu-id="b73b7-116">签名可以嵌入标识封闭类或值类型的标记。</span><span class="sxs-lookup"><span data-stu-id="b73b7-116">A signature can embed a token that identifies the enclosing class or value type.</span></span> <span data-ttu-id="b73b7-117"> (令牌是) 本地 TypeDef 表中的索引。</span><span class="sxs-lookup"><span data-stu-id="b73b7-117">(The token is an index into the local TypeDef table).</span></span> <span data-ttu-id="b73b7-118">不能在当前范围的上下文之外生成运行时签名，并将该签名用作的输入 `FindField` 。</span><span class="sxs-lookup"><span data-stu-id="b73b7-118">You cannot build a run-time signature outside the context of the current scope and use that signature as input to `FindField`.</span></span>  
  
 <span data-ttu-id="b73b7-119">`FindField` 仅查找直接在类或接口中定义的字段;它不会找到继承的字段。</span><span class="sxs-lookup"><span data-stu-id="b73b7-119">`FindField` finds only fields that were defined directly in the class or interface; it does not find inherited fields.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b73b7-120">要求</span><span class="sxs-lookup"><span data-stu-id="b73b7-120">Requirements</span></span>  

 <span data-ttu-id="b73b7-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b73b7-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b73b7-122">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="b73b7-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b73b7-123">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b73b7-123">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b73b7-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b73b7-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b73b7-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="b73b7-125">See also</span></span>

- [<span data-ttu-id="b73b7-126">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="b73b7-126">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="b73b7-127">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="b73b7-127">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
