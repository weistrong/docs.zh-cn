---
description: 了解详细信息： IAssemblyEnum：： Clone 方法
title: IAssemblyEnum::Clone 方法
ms.date: 03/30/2017
api_name:
- IAssemblyEnum.Clone
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyEnum::Clone
helpviewer_keywords:
- Clone method, IAssemblyEnum interface [.NET Framework fusion]
- IAssemblyEnum::Clone method [.NET Framework fusion]
ms.assetid: 0014bb66-590c-486c-9ade-f2133905cd99
topic_type:
- apiref
ms.openlocfilehash: 0b4da5818b66d5b82da0b693c2d1cfa257f08a7f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760831"
---
# <a name="iassemblyenumclone-method"></a><span data-ttu-id="d0715-103">IAssemblyEnum::Clone 方法</span><span class="sxs-lookup"><span data-stu-id="d0715-103">IAssemblyEnum::Clone Method</span></span>

<span data-ttu-id="d0715-104">创建此 [IAssemblyEnum](iassemblyenum-interface.md) 对象的浅表副本。</span><span class="sxs-lookup"><span data-stu-id="d0715-104">Creates a shallow copy of this [IAssemblyEnum](iassemblyenum-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d0715-105">语法</span><span class="sxs-lookup"><span data-stu-id="d0715-105">Syntax</span></span>  
  
```cpp  
HRESULT Clone (  
    [out] IAssemblyEnum   **ppEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d0715-106">参数</span><span class="sxs-lookup"><span data-stu-id="d0715-106">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="d0715-107">弄指向复制的指针。</span><span class="sxs-lookup"><span data-stu-id="d0715-107">[out] A pointer to the copy.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d0715-108">要求</span><span class="sxs-lookup"><span data-stu-id="d0715-108">Requirements</span></span>  

 <span data-ttu-id="d0715-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d0715-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d0715-110">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="d0715-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="d0715-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d0715-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0715-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="d0715-112">See also</span></span>

- [<span data-ttu-id="d0715-113">IAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="d0715-113">IAssemblyEnum Interface</span></span>](iassemblyenum-interface.md)
