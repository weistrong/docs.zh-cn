---
description: 了解详细信息： IMetaDataEmit：:D efineUserString 方法
title: IMetaDataEmit::DefineUserString 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineUserString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineUserString
helpviewer_keywords:
- DefineUserString method [.NET Framework metadata]
- IMetaDataEmit::DefineUserString method [.NET Framework metadata]
ms.assetid: 88fb7ef3-bbdf-429c-b678-c9c153456461
topic_type:
- apiref
ms.openlocfilehash: 0d1c376e3f121d35cb9f6c08d7013a3913a8bd49
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783997"
---
# <a name="imetadataemitdefineuserstring-method"></a><span data-ttu-id="67693-103">IMetaDataEmit::DefineUserString 方法</span><span class="sxs-lookup"><span data-stu-id="67693-103">IMetaDataEmit::DefineUserString Method</span></span>

<span data-ttu-id="67693-104">获取指定文本字符串的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="67693-104">Gets a metadata token for the specified literal string.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="67693-105">语法</span><span class="sxs-lookup"><span data-stu-id="67693-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineUserString (
    [in]  LPCWSTR     szString,
    [in]  ULONG       cchString,
    [out] mdString    *pstk
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="67693-106">参数</span><span class="sxs-lookup"><span data-stu-id="67693-106">Parameters</span></span>  

 `szString`  
 <span data-ttu-id="67693-107">中要存储的用户字符串。</span><span class="sxs-lookup"><span data-stu-id="67693-107">[in] The user string to store.</span></span>  
  
 `cchString`  
 <span data-ttu-id="67693-108">中中的宽字符数 `szString` 。</span><span class="sxs-lookup"><span data-stu-id="67693-108">[in] The count of wide characters in `szString`.</span></span>  
  
 `pstk`  
 <span data-ttu-id="67693-109">弄分配的字符串标记。</span><span class="sxs-lookup"><span data-stu-id="67693-109">[out] The string token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="67693-110">要求</span><span class="sxs-lookup"><span data-stu-id="67693-110">Requirements</span></span>  

 <span data-ttu-id="67693-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="67693-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="67693-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="67693-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="67693-113">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="67693-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="67693-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="67693-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="67693-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="67693-115">See also</span></span>

- [<span data-ttu-id="67693-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="67693-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="67693-117">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="67693-117">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
