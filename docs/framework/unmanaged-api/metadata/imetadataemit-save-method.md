---
description: 了解详细信息： IMetaDataEmit：： Save 方法
title: IMetaDataEmit::Save 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.Save
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::Save
helpviewer_keywords:
- Save method, IMetaDataEmit interface [.NET Framework metadata]
- IMetaDataEmit::Save method [.NET Framework metadata]
ms.assetid: c1de8400-adfe-4a71-b828-a1d0cc1ea505
topic_type:
- apiref
ms.openlocfilehash: bf8675540ae2c851d2b6ed14883c9b75e9631903
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745861"
---
# <a name="imetadataemitsave-method"></a><span data-ttu-id="5e24e-103">IMetaDataEmit::Save 方法</span><span class="sxs-lookup"><span data-stu-id="5e24e-103">IMetaDataEmit::Save Method</span></span>

<span data-ttu-id="5e24e-104">将当前范围中的所有元数据保存到指定地址处的文件。</span><span class="sxs-lookup"><span data-stu-id="5e24e-104">Saves all metadata in the current scope to the file at the specified address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e24e-105">语法</span><span class="sxs-lookup"><span data-stu-id="5e24e-105">Syntax</span></span>  
  
```cpp  
HRESULT Save (
    [in]  LPCWSTR     szFile,
    [in]  DWORD       dwSaveFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5e24e-106">参数</span><span class="sxs-lookup"><span data-stu-id="5e24e-106">Parameters</span></span>  

 `wzFile`  
 <span data-ttu-id="5e24e-107">中要保存到的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="5e24e-107">[in] The name of the file to save to.</span></span> <span data-ttu-id="5e24e-108">如果此值为 null，则内存中的副本将保存到上次使用的位置。</span><span class="sxs-lookup"><span data-stu-id="5e24e-108">If this value is null, the in-memory copy will be saved to the last location that was used.</span></span>  
  
 `dwSaveFlags`  
 <span data-ttu-id="5e24e-109">[in] 保留。</span><span class="sxs-lookup"><span data-stu-id="5e24e-109">[in] Reserved.</span></span> <span data-ttu-id="5e24e-110">必须为零。</span><span class="sxs-lookup"><span data-stu-id="5e24e-110">Must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5e24e-111">要求</span><span class="sxs-lookup"><span data-stu-id="5e24e-111">Requirements</span></span>  

 <span data-ttu-id="5e24e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5e24e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5e24e-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="5e24e-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5e24e-114">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="5e24e-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5e24e-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5e24e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e24e-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="5e24e-116">See also</span></span>

- [<span data-ttu-id="5e24e-117">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="5e24e-117">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="5e24e-118">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="5e24e-118">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
