---
description: 了解详细信息： ICorPublishEnum：： GetCount 方法
title: ICorPublishEnum::GetCount 方法
ms.date: 03/30/2017
api_name:
- ICorPublishEnum.GetCount
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishEnum::GetCount
helpviewer_keywords:
- GetCount method, ICorPublishEnum interface [.NET Framework debugging]
- ICorPublishEnum::GetCount method [.NET Framework debugging]
ms.assetid: d228f684-2be3-4029-93ae-31fe02213c1f
topic_type:
- apiref
ms.openlocfilehash: 99e831ae366604e2ae7494bf80fb2e7f25532582
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721614"
---
# <a name="icorpublishenumgetcount-method"></a><span data-ttu-id="04527-103">ICorPublishEnum::GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="04527-103">ICorPublishEnum::GetCount Method</span></span>

<span data-ttu-id="04527-104">获取枚举中的项数。</span><span class="sxs-lookup"><span data-stu-id="04527-104">Gets the number of items in the enumeration.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="04527-105">语法</span><span class="sxs-lookup"><span data-stu-id="04527-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCount (  
    [out] ULONG   *pcelt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="04527-106">参数</span><span class="sxs-lookup"><span data-stu-id="04527-106">Parameters</span></span>  

 `pcelt`  
 <span data-ttu-id="04527-107">弄一个指针，指向枚举中的项数。</span><span class="sxs-lookup"><span data-stu-id="04527-107">[out] A pointer to the number of items in the enumeration.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="04527-108">要求</span><span class="sxs-lookup"><span data-stu-id="04527-108">Requirements</span></span>  

 <span data-ttu-id="04527-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="04527-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="04527-110">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="04527-110">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="04527-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="04527-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="04527-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="04527-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04527-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="04527-113">See also</span></span>

- [<span data-ttu-id="04527-114">ICorPublishEnum 接口</span><span class="sxs-lookup"><span data-stu-id="04527-114">ICorPublishEnum Interface</span></span>](icorpublishenum-interface.md)
