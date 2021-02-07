---
description: 了解详细信息： IMetaDataTables：： GetNumTables 方法
title: IMetaDataTables::GetNumTables 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNumTables
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNumTables
helpviewer_keywords:
- GetNumTables method [.NET Framework metadata]
- IMetaDataTables::GetNumTables method [.NET Framework metadata]
ms.assetid: 8196f2a3-bbf2-45d3-a6cd-74502c356644
topic_type:
- apiref
ms.openlocfilehash: 1d1e386b1f1eb0f73fbd0df8ddff9cebc5817692
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687839"
---
# <a name="imetadatatablesgetnumtables-method"></a><span data-ttu-id="a559e-103">IMetaDataTables::GetNumTables 方法</span><span class="sxs-lookup"><span data-stu-id="a559e-103">IMetaDataTables::GetNumTables Method</span></span>

<span data-ttu-id="a559e-104">获取当前实例的范围中的表数 `IMetaDataTables` 。</span><span class="sxs-lookup"><span data-stu-id="a559e-104">Gets the number of tables in the scope of the current `IMetaDataTables` instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a559e-105">语法</span><span class="sxs-lookup"><span data-stu-id="a559e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNumTables (  
    [out]  ULONG   *pcTables  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a559e-106">参数</span><span class="sxs-lookup"><span data-stu-id="a559e-106">Parameters</span></span>  

 `pcTables`  
 <span data-ttu-id="a559e-107">弄一个指针，指向当前实例范围中的表数。</span><span class="sxs-lookup"><span data-stu-id="a559e-107">[out] A pointer to the number of tables in the current instance scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a559e-108">要求</span><span class="sxs-lookup"><span data-stu-id="a559e-108">Requirements</span></span>  

 <span data-ttu-id="a559e-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a559e-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a559e-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="a559e-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a559e-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="a559e-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a559e-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a559e-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a559e-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="a559e-113">See also</span></span>

- [<span data-ttu-id="a559e-114">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="a559e-114">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="a559e-115">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="a559e-115">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
