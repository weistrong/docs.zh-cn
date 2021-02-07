---
description: 了解详细信息： IMetaDataTables：： GetNextUserString 方法
title: IMetaDataTables::GetNextUserString 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNextUserString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNextUserString
helpviewer_keywords:
- GetNextUserString method [.NET Framework metadata]
- IMetaDataTables::GetNextUserString method [.NET Framework metadata]
ms.assetid: b7cb40ee-67b7-4f4e-8dcc-ee7ac8bc986b
topic_type:
- apiref
ms.openlocfilehash: cba1fad18b4f697a5e48ad3b0676bf93f9c66e4e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687943"
---
# <a name="imetadatatablesgetnextuserstring-method"></a><span data-ttu-id="30077-103">IMetaDataTables::GetNextUserString 方法</span><span class="sxs-lookup"><span data-stu-id="30077-103">IMetaDataTables::GetNextUserString Method</span></span>

<span data-ttu-id="30077-104">获取包含当前表列中的下一个硬编码字符串的行的索引。</span><span class="sxs-lookup"><span data-stu-id="30077-104">Gets the index of the row that contains the next hard-coded string in the current table column.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30077-105">语法</span><span class="sxs-lookup"><span data-stu-id="30077-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNextUserString (  
    [in]  ULONG   ixUserString,  
    [out] ULONG   *pNext  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="30077-106">参数</span><span class="sxs-lookup"><span data-stu-id="30077-106">Parameters</span></span>  

 `ixUserString`  
 <span data-ttu-id="30077-107">中当前字符串列中的索引值。</span><span class="sxs-lookup"><span data-stu-id="30077-107">[in] An index value from the current string column.</span></span>  
  
 `pNext`  
 <span data-ttu-id="30077-108">弄指向列中下一个字符串的行索引的指针。</span><span class="sxs-lookup"><span data-stu-id="30077-108">[out] A pointer to the row index of the next string in the column.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="30077-109">备注</span><span class="sxs-lookup"><span data-stu-id="30077-109">Remarks</span></span>  

 <span data-ttu-id="30077-110">不建议使用此方法，因为它不返回一致的结果。</span><span class="sxs-lookup"><span data-stu-id="30077-110">We do not recommend the use of this method, because it does not return consistent results.</span></span> <span data-ttu-id="30077-111">有关 GUID 表的信息，请参阅公共语言基础结构 (CLI) 文档，尤其是 "第二部分：元数据定义和语义"。</span><span class="sxs-lookup"><span data-stu-id="30077-111">For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics".</span></span> <span data-ttu-id="30077-112">文档在线提供;请参阅 [ECMA c # 和公共语言基础结构标准](../../../standard/components.md#applicable-standards) 和 [标准 ECMA-335-公共语言基础结构 (CLI) ](http://www.ecma-international.org/publications/standards/Ecma-335.htm)。</span><span class="sxs-lookup"><span data-stu-id="30077-112">The documentation is available online; see [ECMA C# and Common Language Infrastructure Standards](../../../standard/components.md#applicable-standards) and [Standard ECMA-335 - Common Language Infrastructure (CLI)](http://www.ecma-international.org/publications/standards/Ecma-335.htm).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="30077-113">要求</span><span class="sxs-lookup"><span data-stu-id="30077-113">Requirements</span></span>  

 <span data-ttu-id="30077-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="30077-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="30077-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="30077-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="30077-116">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="30077-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="30077-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="30077-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30077-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="30077-118">See also</span></span>

- [<span data-ttu-id="30077-119">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="30077-119">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="30077-120">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="30077-120">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
