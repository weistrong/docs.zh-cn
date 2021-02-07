---
description: 了解详细信息： ICorPublishProcess：： GetProcessID 方法
title: ICorPublishProcess::GetProcessID 方法
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.GetProcessID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::GetProcessID
helpviewer_keywords:
- ICorPublishProcess::GetProcessID method [.NET Framework debugging]
- GetProcessID method [.NET Framework debugging]
ms.assetid: f31185e0-f01d-463a-b392-42163e39bfe9
topic_type:
- apiref
ms.openlocfilehash: f959a49330e0ef4ade2a878acfd287657b5086ec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728803"
---
# <a name="icorpublishprocessgetprocessid-method"></a><span data-ttu-id="fca0c-103">ICorPublishProcess::GetProcessID 方法</span><span class="sxs-lookup"><span data-stu-id="fca0c-103">ICorPublishProcess::GetProcessID Method</span></span>

<span data-ttu-id="fca0c-104">获取此进程的操作系统标识符。</span><span class="sxs-lookup"><span data-stu-id="fca0c-104">Gets the operating system identifier for this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fca0c-105">语法</span><span class="sxs-lookup"><span data-stu-id="fca0c-105">Syntax</span></span>  
  
```cpp  
HRESULT GetProcessID (  
    [out] unsigned   *pid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fca0c-106">参数</span><span class="sxs-lookup"><span data-stu-id="fca0c-106">Parameters</span></span>  

 `pid`  
 <span data-ttu-id="fca0c-107">弄一个指针，指向此 [ICorPublishProcess](icorpublishprocess-interface.md) 对象所表示的进程的标识符。</span><span class="sxs-lookup"><span data-stu-id="fca0c-107">[out] A pointer to the identifier of the process represented by this [ICorPublishProcess](icorpublishprocess-interface.md) object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fca0c-108">要求</span><span class="sxs-lookup"><span data-stu-id="fca0c-108">Requirements</span></span>  

 <span data-ttu-id="fca0c-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fca0c-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fca0c-110">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="fca0c-110">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="fca0c-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fca0c-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fca0c-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fca0c-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fca0c-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="fca0c-113">See also</span></span>

- [<span data-ttu-id="fca0c-114">ICorPublishProcess 接口</span><span class="sxs-lookup"><span data-stu-id="fca0c-114">ICorPublishProcess Interface</span></span>](icorpublishprocess-interface.md)
