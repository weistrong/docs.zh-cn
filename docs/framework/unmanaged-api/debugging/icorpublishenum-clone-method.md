---
description: 了解详细信息： ICorPublishEnum：： Clone 方法
title: ICorPublishEnum::Clone 方法
ms.date: 03/30/2017
api_name:
- ICorPublishEnum.Clone
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishEnum::Clone
helpviewer_keywords:
- Clone method, ICorPublishEnum interface [.NET Framework debugging]
- ICorPublishEnum::Clone method [.NET Framework debugging]
ms.assetid: c9a26ea3-b8eb-4b8e-854f-9a2ca26b3b39
topic_type:
- apiref
ms.openlocfilehash: 6001f27451afdb564da6275a31256ac348bc693a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721640"
---
# <a name="icorpublishenumclone-method"></a><span data-ttu-id="3c84c-103">ICorPublishEnum::Clone 方法</span><span class="sxs-lookup"><span data-stu-id="3c84c-103">ICorPublishEnum::Clone Method</span></span>

<span data-ttu-id="3c84c-104">创建此 [ICorPublishEnum](icorpublishenum-interface.md) 对象的副本。</span><span class="sxs-lookup"><span data-stu-id="3c84c-104">Creates a copy of this [ICorPublishEnum](icorpublishenum-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c84c-105">语法</span><span class="sxs-lookup"><span data-stu-id="3c84c-105">Syntax</span></span>  
  
```cpp  
HRESULT Clone (  
    [out] ICorPublishEnum   **ppEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3c84c-106">参数</span><span class="sxs-lookup"><span data-stu-id="3c84c-106">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="3c84c-107">弄指向作为 `ICorPublishEnum` 此对象副本的对象地址的指针 `ICorPublishEnum` 。</span><span class="sxs-lookup"><span data-stu-id="3c84c-107">[out] A pointer to the address of an `ICorPublishEnum` object that is a copy of this `ICorPublishEnum` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c84c-108">要求</span><span class="sxs-lookup"><span data-stu-id="3c84c-108">Requirements</span></span>  

 <span data-ttu-id="3c84c-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3c84c-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c84c-110">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="3c84c-110">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="3c84c-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3c84c-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3c84c-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c84c-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c84c-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="3c84c-113">See also</span></span>

- [<span data-ttu-id="3c84c-114">ICorPublishEnum 接口</span><span class="sxs-lookup"><span data-stu-id="3c84c-114">ICorPublishEnum Interface</span></span>](icorpublishenum-interface.md)
