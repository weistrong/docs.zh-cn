---
description: 了解详细信息： IMetaDataEmit：： SaveToMemory 方法
title: IMetaDataEmit::SaveToMemory 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SaveToMemory
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SaveToMemory
helpviewer_keywords:
- IMetaDataEmit::SaveToMemory method [.NET Framework metadata]
- SaveToMemory method [.NET Framework metadata]
ms.assetid: d5237628-2675-45ed-a39e-65c0731b6a56
topic_type:
- apiref
ms.openlocfilehash: b5fbca2c3ce06398de72bf2690108077545fef9c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745796"
---
# <a name="imetadataemitsavetomemory-method"></a><span data-ttu-id="16107-103">IMetaDataEmit::SaveToMemory 方法</span><span class="sxs-lookup"><span data-stu-id="16107-103">IMetaDataEmit::SaveToMemory Method</span></span>

<span data-ttu-id="16107-104">将当前范围中的所有元数据保存到指定的内存区域。</span><span class="sxs-lookup"><span data-stu-id="16107-104">Saves all metadata in the current scope to the specified area of memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="16107-105">语法</span><span class="sxs-lookup"><span data-stu-id="16107-105">Syntax</span></span>  
  
```cpp  
HRESULT SaveToMemory (
    [out]  void        *pbData,
    [in]   ULONG       cbData
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="16107-106">参数</span><span class="sxs-lookup"><span data-stu-id="16107-106">Parameters</span></span>  

 `pbData`  
 <span data-ttu-id="16107-107">弄开始写入元数据的地址。</span><span class="sxs-lookup"><span data-stu-id="16107-107">[out] The address at which to begin writing metadata.</span></span>  
  
 `cbData`  
 <span data-ttu-id="16107-108">中已分配内存的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="16107-108">[in] The size, in bytes, of the allocated memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="16107-109">要求</span><span class="sxs-lookup"><span data-stu-id="16107-109">Requirements</span></span>  

 <span data-ttu-id="16107-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="16107-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="16107-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="16107-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="16107-112">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="16107-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="16107-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="16107-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="16107-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="16107-114">See also</span></span>

- [<span data-ttu-id="16107-115">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="16107-115">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="16107-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="16107-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
