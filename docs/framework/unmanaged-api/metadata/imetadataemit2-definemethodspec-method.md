---
description: 了解详细信息： IMetaDataEmit2：:D efineMethodSpec 方法
title: IMetaDataEmit2::DefineMethodSpec 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.DefineMethodSpec
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::DefineMethodSpec
helpviewer_keywords:
- DefineMethodSpec method [.NET Framework metadata]
- IMetaDataEmit2::DefineMethodSpec method [.NET Framework metadata]
ms.assetid: 3c24e552-fc69-4971-b65a-a3e4b5f7f1e8
topic_type:
- apiref
ms.openlocfilehash: 4b5283375ba194a86a83b142b3b2bdc06bfd35da
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745731"
---
# <a name="imetadataemit2definemethodspec-method"></a><span data-ttu-id="96cb8-103">IMetaDataEmit2::DefineMethodSpec 方法</span><span class="sxs-lookup"><span data-stu-id="96cb8-103">IMetaDataEmit2::DefineMethodSpec Method</span></span>

<span data-ttu-id="96cb8-104">创建方法的泛型实例，并获取定义的标记。</span><span class="sxs-lookup"><span data-stu-id="96cb8-104">Creates a generic instance of a method, and gets a token to the definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96cb8-105">语法</span><span class="sxs-lookup"><span data-stu-id="96cb8-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineMethodSpec (  
    [in]  mdToken           tkParent,
    [in]  PCCOR_SIGNATURE   pvSigBlob,
    [in]  ULONG             cbSigBlob,
    [out] mdMethodSpec      *pmi  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="96cb8-106">参数</span><span class="sxs-lookup"><span data-stu-id="96cb8-106">Parameters</span></span>  

 `tkParent`  
 <span data-ttu-id="96cb8-107">中创建泛型实例的方法的标记。</span><span class="sxs-lookup"><span data-stu-id="96cb8-107">[in] A token for the method of which to create the generic instance.</span></span> <span data-ttu-id="96cb8-108">令牌的类型必须为 `mdMethodDef` 或 `mdMemberRef` 。</span><span class="sxs-lookup"><span data-stu-id="96cb8-108">The token must be of type `mdMethodDef` or `mdMemberRef`.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="96cb8-109">中指向方法的二进制 COM + 签名的指针。</span><span class="sxs-lookup"><span data-stu-id="96cb8-109">[in] A pointer to the binary COM+ signature of the method.</span></span>  
  
 `cbSibBlob`  
 <span data-ttu-id="96cb8-110">中的大小（以字节为单位） `pvSigBlob` 。</span><span class="sxs-lookup"><span data-stu-id="96cb8-110">[in] The size, in bytes, of `pvSigBlob`.</span></span>  
  
 `pmi`  
 <span data-ttu-id="96cb8-111">弄方法的元数据签名定义的标记。</span><span class="sxs-lookup"><span data-stu-id="96cb8-111">[out] A token to the metadata signature definition of the method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="96cb8-112">要求</span><span class="sxs-lookup"><span data-stu-id="96cb8-112">Requirements</span></span>  

 <span data-ttu-id="96cb8-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="96cb8-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="96cb8-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="96cb8-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="96cb8-115">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="96cb8-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="96cb8-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="96cb8-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="96cb8-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="96cb8-117">See also</span></span>

- [<span data-ttu-id="96cb8-118">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="96cb8-118">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
- [<span data-ttu-id="96cb8-119">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="96cb8-119">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
