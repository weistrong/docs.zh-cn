---
description: 了解详细信息： IMetaDataTables：： GetNextString 方法
title: IMetaDataTables::GetNextString 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNextString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNextString
helpviewer_keywords:
- IMetaDataTables::GetNextString method [.NET Framework metadata]
- GetNextString method [.NET Framework metadata]
ms.assetid: d9720428-c353-4f07-a7e8-899e106a1b37
topic_type:
- apiref
ms.openlocfilehash: b3c4f94a2659b83c89bef322517465a585b63ddc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688008"
---
# <a name="imetadatatablesgetnextstring-method"></a><span data-ttu-id="1811f-103">IMetaDataTables::GetNextString 方法</span><span class="sxs-lookup"><span data-stu-id="1811f-103">IMetaDataTables::GetNextString Method</span></span>

<span data-ttu-id="1811f-104">获取当前表列中的下一个字符串的索引。</span><span class="sxs-lookup"><span data-stu-id="1811f-104">Gets the index of the next string in the current table column.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1811f-105">语法</span><span class="sxs-lookup"><span data-stu-id="1811f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNextString (
    [in]  ULONG   ixString,  
    [out] ULONG   *pNext  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1811f-106">参数</span><span class="sxs-lookup"><span data-stu-id="1811f-106">Parameters</span></span>  

 `ixString`  
 <span data-ttu-id="1811f-107">中字符串表列的索引值。</span><span class="sxs-lookup"><span data-stu-id="1811f-107">[in] The index value from a string table column.</span></span>  
  
 `pNext`  
 <span data-ttu-id="1811f-108">弄指向列中的下一个字符串的索引的指针。</span><span class="sxs-lookup"><span data-stu-id="1811f-108">[out] A pointer to the index of the next string in the column.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1811f-109">要求</span><span class="sxs-lookup"><span data-stu-id="1811f-109">Requirements</span></span>  

 <span data-ttu-id="1811f-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1811f-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1811f-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="1811f-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1811f-112">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="1811f-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1811f-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1811f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1811f-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="1811f-114">See also</span></span>

- [<span data-ttu-id="1811f-115">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="1811f-115">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="1811f-116">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="1811f-116">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
