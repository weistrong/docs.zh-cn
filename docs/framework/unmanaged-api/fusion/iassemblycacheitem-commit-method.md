---
description: 了解详细信息： IAssemblyCacheItem：： Commit 方法
title: IAssemblyCacheItem::Commit 方法
ms.date: 03/30/2017
api_name:
- IAssemblyCacheItem.Commit
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCacheItem::Commit
helpviewer_keywords:
- IAssemblyCacheItem::Commit method [.NET Framework fusion]
- Commit method, IAssemblyCacheItem interface [.NET Framework fusion]
ms.assetid: c2321f17-f46f-4815-ae41-b28678753613
topic_type:
- apiref
ms.openlocfilehash: bd73bb9099090089e52d52009cfef309b33adc53
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760846"
---
# <a name="iassemblycacheitemcommit-method"></a><span data-ttu-id="f1c71-103">IAssemblyCacheItem::Commit 方法</span><span class="sxs-lookup"><span data-stu-id="f1c71-103">IAssemblyCacheItem::Commit Method</span></span>

<span data-ttu-id="f1c71-104">将缓存的程序集引用提交到内存。</span><span class="sxs-lookup"><span data-stu-id="f1c71-104">Commits the cached assembly reference to memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1c71-105">语法</span><span class="sxs-lookup"><span data-stu-id="f1c71-105">Syntax</span></span>  
  
```cpp  
HRESULT Commit (  
    [in] DWORD dwFlags,
    [out, optional] ULONG *pulDisposition  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f1c71-106">参数</span><span class="sxs-lookup"><span data-stu-id="f1c71-106">Parameters</span></span>  

 `dwFlags`  
 <span data-ttu-id="f1c71-107">中在合成 .idl 中定义的标志。</span><span class="sxs-lookup"><span data-stu-id="f1c71-107">[in] Flags defined in Fusion.idl.</span></span>  
  
 `pulDisposition`  
 <span data-ttu-id="f1c71-108">[out，optional]一个指示操作结果的值。</span><span class="sxs-lookup"><span data-stu-id="f1c71-108">[out, optional] A value that indicates the result of the operation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f1c71-109">要求</span><span class="sxs-lookup"><span data-stu-id="f1c71-109">Requirements</span></span>  

 <span data-ttu-id="f1c71-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f1c71-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f1c71-111">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="f1c71-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="f1c71-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f1c71-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1c71-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="f1c71-113">See also</span></span>

- [<span data-ttu-id="f1c71-114">IAssemblyCacheItem 接口</span><span class="sxs-lookup"><span data-stu-id="f1c71-114">IAssemblyCacheItem Interface</span></span>](iassemblycacheitem-interface.md)
