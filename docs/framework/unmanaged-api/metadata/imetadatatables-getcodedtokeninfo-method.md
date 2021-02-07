---
description: 了解详细信息： IMetaDataTables：： GetCodedTokenInfo 方法
title: IMetaDataTables::GetCodedTokenInfo 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetCodedTokenInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetCodedTokenInfo
helpviewer_keywords:
- GetCodedTokenInfo method [.NET Framework metadata]
- IMetaDataTables::GetCodedTokenInfo method [.NET Framework metadata]
ms.assetid: 31214d3a-715e-49af-92b3-0fd11e4f218a
topic_type:
- apiref
ms.openlocfilehash: 982a13636d8b4572113038eaa658158e6c2ca966
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688281"
---
# <a name="imetadatatablesgetcodedtokeninfo-method"></a><span data-ttu-id="0fe01-103">IMetaDataTables::GetCodedTokenInfo 方法</span><span class="sxs-lookup"><span data-stu-id="0fe01-103">IMetaDataTables::GetCodedTokenInfo Method</span></span>

<span data-ttu-id="0fe01-104">获取一个指针，该指针指向与指定的行索引相关联的标记的数组。</span><span class="sxs-lookup"><span data-stu-id="0fe01-104">Gets a pointer to an array of tokens associated with the specified row index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0fe01-105">语法</span><span class="sxs-lookup"><span data-stu-id="0fe01-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCodedTokenInfo (
    [in]  ULONG       ixCdTkn,  
    [out] ULONG       *pcTokens,  
    [out] ULONG       **ppTokens,  
    [out] const char  **ppName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0fe01-106">参数</span><span class="sxs-lookup"><span data-stu-id="0fe01-106">Parameters</span></span>  

 `ixCdTkn`  
 <span data-ttu-id="0fe01-107">中要返回的编码标记的类型。</span><span class="sxs-lookup"><span data-stu-id="0fe01-107">[in] The kind of coded token to return.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="0fe01-108">弄指向的长度的指针 `ppTokens` 。</span><span class="sxs-lookup"><span data-stu-id="0fe01-108">[out] A pointer to the length of `ppTokens`.</span></span>  
  
 `ppTokens`  
 <span data-ttu-id="0fe01-109">弄指向数组的指针的指针，该数组包含返回的标记的列表。</span><span class="sxs-lookup"><span data-stu-id="0fe01-109">[out] A pointer to a pointer to an array that contains the list of returned tokens.</span></span>  
  
 `ppName`  
 <span data-ttu-id="0fe01-110">弄指向指向中的标记名称的指针的指针 `ixCdTkn` 。</span><span class="sxs-lookup"><span data-stu-id="0fe01-110">[out] A pointer to a pointer to the name of the token at `ixCdTkn`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0fe01-111">要求</span><span class="sxs-lookup"><span data-stu-id="0fe01-111">Requirements</span></span>  

 <span data-ttu-id="0fe01-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0fe01-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0fe01-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="0fe01-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0fe01-114">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="0fe01-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="0fe01-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0fe01-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fe01-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="0fe01-116">See also</span></span>

- [<span data-ttu-id="0fe01-117">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="0fe01-117">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="0fe01-118">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="0fe01-118">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
