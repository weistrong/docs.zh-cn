---
description: 了解详细信息： IMetaDataTables：： GetRow 方法
title: IMetaDataTables::GetRow 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetRow
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetRow
helpviewer_keywords:
- IMetaDataTables::GetRow method [.NET Framework metadata]
- GetRow method [.NET Framework metadata]
ms.assetid: a7408d51-0bce-45a2-b58f-da4660bbc039
topic_type:
- apiref
ms.openlocfilehash: f3888bbb53339dc60eb0c2d36f2d7383e5f8c228
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687813"
---
# <a name="imetadatatablesgetrow-method"></a><span data-ttu-id="4b5a1-103">IMetaDataTables::GetRow 方法</span><span class="sxs-lookup"><span data-stu-id="4b5a1-103">IMetaDataTables::GetRow Method</span></span>

<span data-ttu-id="4b5a1-104">获取位于指定表索引处的表中指定行索引处的行。</span><span class="sxs-lookup"><span data-stu-id="4b5a1-104">Gets the row at the specified row index, in the table at the specified table index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b5a1-105">语法</span><span class="sxs-lookup"><span data-stu-id="4b5a1-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRow (
    [in]  ULONG   ixTbl,  
    [in]  ULONG   rid,  
    [out] void    **ppRow  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4b5a1-106">参数</span><span class="sxs-lookup"><span data-stu-id="4b5a1-106">Parameters</span></span>  

 `ixTbl`  
 <span data-ttu-id="4b5a1-107">中要从中检索行的表的索引。</span><span class="sxs-lookup"><span data-stu-id="4b5a1-107">[in] The index of the table from which the row will be retrieved.</span></span>  
  
 `rid`  
 <span data-ttu-id="4b5a1-108">中要获取的行的索引。</span><span class="sxs-lookup"><span data-stu-id="4b5a1-108">[in] The index of the row to get.</span></span>  
  
 `ppRow`  
 <span data-ttu-id="4b5a1-109">弄指向指向行的指针的指针。</span><span class="sxs-lookup"><span data-stu-id="4b5a1-109">[out] A pointer to a pointer to the row.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4b5a1-110">备注</span><span class="sxs-lookup"><span data-stu-id="4b5a1-110">Remarks</span></span>  

  <span data-ttu-id="4b5a1-111">不建议使用此方法，因为它不返回一致的结果。</span><span class="sxs-lookup"><span data-stu-id="4b5a1-111">We do not recommend the use of this method, because it does not return consistent results.</span></span> <span data-ttu-id="4b5a1-112">有关 GUID 表的信息，请参阅公共语言基础结构 (CLI) 文档，尤其是 "第二部分：元数据定义和语义"。</span><span class="sxs-lookup"><span data-stu-id="4b5a1-112">For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics".</span></span> <span data-ttu-id="4b5a1-113">文档在线提供;请参阅 [ECMA c # 和公共语言基础结构标准](../../../standard/components.md#applicable-standards) 和 [标准 ECMA-335-公共语言基础结构 (CLI) ](http://www.ecma-international.org/publications/standards/Ecma-335.htm)。</span><span class="sxs-lookup"><span data-stu-id="4b5a1-113">The documentation is available online; see [ECMA C# and Common Language Infrastructure Standards](../../../standard/components.md#applicable-standards) and [Standard ECMA-335 - Common Language Infrastructure (CLI)](http://www.ecma-international.org/publications/standards/Ecma-335.htm).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4b5a1-114">要求</span><span class="sxs-lookup"><span data-stu-id="4b5a1-114">Requirements</span></span>  

 <span data-ttu-id="4b5a1-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4b5a1-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4b5a1-116">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="4b5a1-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="4b5a1-117">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="4b5a1-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="4b5a1-118">**.NET Framework 版本**  [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4b5a1-118">**.NET Framework Versions**  [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b5a1-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="4b5a1-119">See also</span></span>

- [<span data-ttu-id="4b5a1-120">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="4b5a1-120">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="4b5a1-121">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="4b5a1-121">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
