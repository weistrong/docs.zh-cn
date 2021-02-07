---
description: 了解详细信息： IMetaDataTables：： GetTableIndex 方法
title: IMetaDataTables::GetTableIndex 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetTableIndex
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetTableIndex
helpviewer_keywords:
- GetTableIndex method [.NET Framework metadata]
- IMetaDataTables::GetTableIndex method [.NET Framework metadata]
ms.assetid: c6ec3800-e0d9-4387-afb8-ddc0b818114c
topic_type:
- apiref
ms.openlocfilehash: d42a42a1a19a67fada17bbe1016f7e324cd1c287
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687722"
---
# <a name="imetadatatablesgettableindex-method"></a><span data-ttu-id="79ba7-103">IMetaDataTables::GetTableIndex 方法</span><span class="sxs-lookup"><span data-stu-id="79ba7-103">IMetaDataTables::GetTableIndex Method</span></span>

<span data-ttu-id="79ba7-104">获取指定的标记所引用的表的索引。</span><span class="sxs-lookup"><span data-stu-id="79ba7-104">Gets the index for the table referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79ba7-105">语法</span><span class="sxs-lookup"><span data-stu-id="79ba7-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTableIndex (  
    [in]  ULONG   token,  
    [out] ULONG   *pixTbl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="79ba7-106">参数</span><span class="sxs-lookup"><span data-stu-id="79ba7-106">Parameters</span></span>  

 `token`  
 <span data-ttu-id="79ba7-107">中引用该表的标记。</span><span class="sxs-lookup"><span data-stu-id="79ba7-107">[in] The token that references the table.</span></span>  
  
 `pixTbl`  
 <span data-ttu-id="79ba7-108">弄指向所引用表的返回索引的指针。</span><span class="sxs-lookup"><span data-stu-id="79ba7-108">[out] A pointer to the returned index for the referenced table.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="79ba7-109">备注</span><span class="sxs-lookup"><span data-stu-id="79ba7-109">Remarks</span></span>  

 <span data-ttu-id="79ba7-110">不建议使用此方法，因为它不返回一致的结果。</span><span class="sxs-lookup"><span data-stu-id="79ba7-110">We do not recommend the use of this method, because it does not return consistent results.</span></span> <span data-ttu-id="79ba7-111">有关 GUID 表的信息，请参阅公共语言基础结构 (CLI) 文档，尤其是 "第二部分：元数据定义和语义"。</span><span class="sxs-lookup"><span data-stu-id="79ba7-111">For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics".</span></span> <span data-ttu-id="79ba7-112">文档在线提供;请参阅 [ECMA c # 和公共语言基础结构标准](../../../standard/components.md#applicable-standards) 和 [标准 ECMA-335-公共语言基础结构 (CLI) ](http://www.ecma-international.org/publications/standards/Ecma-335.htm)。</span><span class="sxs-lookup"><span data-stu-id="79ba7-112">The documentation is available online; see [ECMA C# and Common Language Infrastructure Standards](../../../standard/components.md#applicable-standards) and [Standard ECMA-335 - Common Language Infrastructure (CLI)](http://www.ecma-international.org/publications/standards/Ecma-335.htm).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79ba7-113">要求</span><span class="sxs-lookup"><span data-stu-id="79ba7-113">Requirements</span></span>  

 <span data-ttu-id="79ba7-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="79ba7-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79ba7-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="79ba7-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="79ba7-116">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="79ba7-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="79ba7-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79ba7-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79ba7-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="79ba7-118">See also</span></span>

- [<span data-ttu-id="79ba7-119">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="79ba7-119">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="79ba7-120">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="79ba7-120">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
