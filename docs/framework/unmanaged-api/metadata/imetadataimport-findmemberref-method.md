---
description: 了解详细信息： IMetaDataImport：： FindMemberRef 方法
title: IMetaDataImport::FindMemberRef 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.FindMemberRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::FindMemberRef
helpviewer_keywords:
- IMetaDataImport::FindMemberRef method [.NET Framework metadata]
- FindMemberRef method [.NET Framework metadata]
ms.assetid: 1ccda329-d752-4d89-abe8-511af3c3f4c9
topic_type:
- apiref
ms.openlocfilehash: 301d4dc88b36ca2284ca3b8d70444820befdc0aa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745575"
---
# <a name="imetadataimportfindmemberref-method"></a><span data-ttu-id="f9d6f-103">IMetaDataImport::FindMemberRef 方法</span><span class="sxs-lookup"><span data-stu-id="f9d6f-103">IMetaDataImport::FindMemberRef Method</span></span>

<span data-ttu-id="f9d6f-104">获取一个指针，该指针指向成员引用的 MemberRef 标记，该成员引用由指定的括起来并 <xref:System.Type> 具有指定的名称和元数据签名。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-104">Gets a pointer to the MemberRef token for the member reference that is enclosed by the specified <xref:System.Type> and that has the specified name and metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f9d6f-105">语法</span><span class="sxs-lookup"><span data-stu-id="f9d6f-105">Syntax</span></span>  
  
```cpp  
HRESULT FindMemberRef (  
   [in]  mdTypeRef          td,  
   [in]  LPCWSTR            szName,
   [in]  PCCOR_SIGNATURE    pvSigBlob,
   [in]  ULONG              cbSigBlob,
   [out] mdMemberRef        *pmr  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f9d6f-106">参数</span><span class="sxs-lookup"><span data-stu-id="f9d6f-106">Parameters</span></span>  

 `td`  
 <span data-ttu-id="f9d6f-107">中类或接口的 TypeRef 标记，其中包含要搜索的成员引用。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-107">[in] The TypeRef token for the class or interface that encloses the member reference to search for.</span></span> <span data-ttu-id="f9d6f-108">如果此值为 `mdTokenNil` ，则对全局变量或全局函数引用执行查找。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-108">If this value is `mdTokenNil`, the lookup is done for a global variable or a global-function reference.</span></span>  
  
 `szName`  
 <span data-ttu-id="f9d6f-109">中要搜索的成员引用的名称。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-109">[in] The name of the member reference to search for.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="f9d6f-110">中指向成员引用的二进制元数据签名的指针。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-110">[in] A pointer to the binary metadata signature of the member reference.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="f9d6f-111">中的大小（以字节为单位） `pvSigBlob` 。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-111">[in] The size in bytes of `pvSigBlob`.</span></span>  
  
 `pmr`  
 <span data-ttu-id="f9d6f-112">弄指向匹配的 MemberRef 标记的指针。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-112">[out] A pointer to the matching MemberRef token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f9d6f-113">备注</span><span class="sxs-lookup"><span data-stu-id="f9d6f-113">Remarks</span></span>  

 <span data-ttu-id="f9d6f-114">你使用其封闭类或接口指定成员 (`td`) ，其名称 (`szName`) ，还可以指定其签名 (`pvSigBlob`) 。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-114">You specify the member using its enclosing class or interface (`td`), its name (`szName`), and optionally its signature (`pvSigBlob`).</span></span>  
  
 <span data-ttu-id="f9d6f-115">传递给的签名 `FindMemberRef` 必须已在当前范围内生成，因为签名将绑定到特定范围。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-115">The signature passed to `FindMemberRef` must have been generated in the current scope, because signatures are bound to a particular scope.</span></span> <span data-ttu-id="f9d6f-116">签名可以嵌入标识封闭类或值类型的标记。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-116">A signature can embed a token that identifies the enclosing class or value type.</span></span> <span data-ttu-id="f9d6f-117">该令牌是本地 TypeDef 表中的索引。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-117">The token is an index into the local TypeDef table.</span></span> <span data-ttu-id="f9d6f-118">不能在当前范围的上下文之外生成运行时签名，并将该签名用作的输入 `FindMemberRef` 。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-118">You cannot build a run-time signature outside the context of the current scope and use that signature as input to `FindMemberRef`.</span></span>  
  
 <span data-ttu-id="f9d6f-119">`FindMemberRef` 仅查找直接在类或接口中定义的成员引用;它不会查找继承成员引用。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-119">`FindMemberRef` finds only member references that were defined directly in the class or interface; it does not find inherited member references.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f9d6f-120">要求</span><span class="sxs-lookup"><span data-stu-id="f9d6f-120">Requirements</span></span>  

 <span data-ttu-id="f9d6f-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d6f-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f9d6f-122">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f9d6f-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f9d6f-123">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f9d6f-123">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f9d6f-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f9d6f-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f9d6f-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="f9d6f-125">See also</span></span>

- [<span data-ttu-id="f9d6f-126">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="f9d6f-126">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="f9d6f-127">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="f9d6f-127">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
