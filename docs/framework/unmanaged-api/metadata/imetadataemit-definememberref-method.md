---
description: 了解详细信息： IMetaDataEmit：:D efineMemberRef 方法
title: IMetaDataEmit::DefineMemberRef 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineMemberRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineMemberRef
helpviewer_keywords:
- DefineMemberRef method [.NET Framework metadata]
- IMetaDataEmit::DefineMemberRef method [.NET Framework metadata]
ms.assetid: 21b5bcb8-ea75-4962-8acc-ad17584061e5
topic_type:
- apiref
ms.openlocfilehash: 1d88294cea14369c8a8f16b6048f96472fbb9502
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753414"
---
# <a name="imetadataemitdefinememberref-method"></a><span data-ttu-id="c5624-103">IMetaDataEmit::DefineMemberRef 方法</span><span class="sxs-lookup"><span data-stu-id="c5624-103">IMetaDataEmit::DefineMemberRef Method</span></span>

<span data-ttu-id="c5624-104">定义对当前范围之外的模块成员的引用，并获取该引用定义的标记。</span><span class="sxs-lookup"><span data-stu-id="c5624-104">Defines a reference to a member of a module outside the current scope, and gets a token to that reference definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c5624-105">语法</span><span class="sxs-lookup"><span data-stu-id="c5624-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineMemberRef (
    [in]  mdToken           tkImport,
    [in]  LPCWSTR           szName,
    [in]  PCCOR_SIGNATURE   pvSigBlob,
    [in]  ULONG             cbSigBlob,
    [out] mdMemberRef       *pmr
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c5624-106">参数</span><span class="sxs-lookup"><span data-stu-id="c5624-106">Parameters</span></span>  

 `tkImport`  
 <span data-ttu-id="c5624-107">中目标成员的类或接口的标记（如果成员不是全局成员）;如果成员是全局成员，则 `mdModuleRef` 为该其他文件的标记。</span><span class="sxs-lookup"><span data-stu-id="c5624-107">[in] Token for the target member's class or interface, if the member is not global; if the member is global, the `mdModuleRef` token for that other file.</span></span>  
  
 `szName`  
 <span data-ttu-id="c5624-108">中目标成员的名称。</span><span class="sxs-lookup"><span data-stu-id="c5624-108">[in] The name of the target member.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="c5624-109">中目标成员的签名。</span><span class="sxs-lookup"><span data-stu-id="c5624-109">[in] The signature of the target member.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="c5624-110">中中的字节数 `pvSigBlob` 。</span><span class="sxs-lookup"><span data-stu-id="c5624-110">[in] The count of bytes in `pvSigBlob`.</span></span>  
  
 `pmr`  
 <span data-ttu-id="c5624-111">弄 `mdMemberRef` 分配的令牌。</span><span class="sxs-lookup"><span data-stu-id="c5624-111">[out] The `mdMemberRef` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c5624-112">要求</span><span class="sxs-lookup"><span data-stu-id="c5624-112">Requirements</span></span>  

 <span data-ttu-id="c5624-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c5624-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c5624-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="c5624-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c5624-115">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="c5624-115">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c5624-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c5624-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5624-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="c5624-117">See also</span></span>

- [<span data-ttu-id="c5624-118">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="c5624-118">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="c5624-119">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="c5624-119">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
