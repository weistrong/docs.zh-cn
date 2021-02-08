---
description: 了解详细信息： ICorPublishProcessEnum：： Next 方法
title: ICorPublishProcessEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorPublishProcessEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcessEnum::Next
helpviewer_keywords:
- ICorPublishProcessEnum::Next method [.NET Framework debugging]
- Next method, ICorPublishProcessEnum interface [.NET Framework debugging]
ms.assetid: 6c399f37-1e38-4ca1-b70d-8ae41f7228b7
topic_type:
- apiref
ms.openlocfilehash: 14b4f815aff986b23a22ed3d5736c37128d3d7e3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790472"
---
# <a name="icorpublishprocessenumnext-method"></a><span data-ttu-id="e2134-103">ICorPublishProcessEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="e2134-103">ICorPublishProcessEnum::Next Method</span></span>

<span data-ttu-id="e2134-104">从当前游标位置开始，获取集合中指定数量的进程。</span><span class="sxs-lookup"><span data-stu-id="e2134-104">Gets the specified number of processes from the collection, starting at the current cursor position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2134-105">语法</span><span class="sxs-lookup"><span data-stu-id="e2134-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorPublishProcess **objects,  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e2134-106">参数</span><span class="sxs-lookup"><span data-stu-id="e2134-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="e2134-107">中要检索的进程数。</span><span class="sxs-lookup"><span data-stu-id="e2134-107">[in] The number of processes to be retrieved.</span></span>  
  
 `objects`  
 <span data-ttu-id="e2134-108">弄一个指针，指向检索到的 [ICorPublishProcess](icorpublishprocess-interface.md) 对象的数组，其中每个对象都表示一个进程。</span><span class="sxs-lookup"><span data-stu-id="e2134-108">[out] A pointer to the array of retrieved [ICorPublishProcess](icorpublishprocess-interface.md) objects, each of which represents a process.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="e2134-109">弄一个指针，指向实际返回的进程数。</span><span class="sxs-lookup"><span data-stu-id="e2134-109">[out] Pointer to the number of processes actually returned.</span></span> <span data-ttu-id="e2134-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="e2134-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e2134-111">要求</span><span class="sxs-lookup"><span data-stu-id="e2134-111">Requirements</span></span>  

 <span data-ttu-id="e2134-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e2134-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e2134-113">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="e2134-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="e2134-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e2134-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e2134-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e2134-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2134-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="e2134-116">See also</span></span>

- [<span data-ttu-id="e2134-117">ICorPublishProcessEnum 接口</span><span class="sxs-lookup"><span data-stu-id="e2134-117">ICorPublishProcessEnum Interface</span></span>](icorpublishprocessenum-interface.md)
