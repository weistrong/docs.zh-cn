---
description: 了解详细信息： ICorDebugEnum：： GetCount 方法
title: ICorDebugEnum::GetCount 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEnum.GetCount
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEnum::GetCount
helpviewer_keywords:
- ICorDebugEnum::GetCount method [.NET Framework debugging]
- GetCount method, ICorDebugEnum interface [.NET Framework debugging]
ms.assetid: d8a74304-1cb2-4977-a21d-e1af48c563ff
topic_type:
- apiref
ms.openlocfilehash: 38fa85958ea0c6945a5575d12700701ed355891d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694547"
---
# <a name="icordebugenumgetcount-method"></a><span data-ttu-id="4e559-103">ICorDebugEnum::GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="4e559-103">ICorDebugEnum::GetCount Method</span></span>

<span data-ttu-id="4e559-104">获取枚举中的项数。</span><span class="sxs-lookup"><span data-stu-id="4e559-104">Gets the number of items in the enumeration.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e559-105">语法</span><span class="sxs-lookup"><span data-stu-id="4e559-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCount (  
    [out] ULONG *pcelt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4e559-106">参数</span><span class="sxs-lookup"><span data-stu-id="4e559-106">Parameters</span></span>  

 `pcelt`  
 <span data-ttu-id="4e559-107">弄一个指针，指向枚举中的项数。</span><span class="sxs-lookup"><span data-stu-id="4e559-107">[out] A pointer to the number of items in the enumeration.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4e559-108">要求</span><span class="sxs-lookup"><span data-stu-id="4e559-108">Requirements</span></span>  

 <span data-ttu-id="4e559-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4e559-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4e559-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4e559-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4e559-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4e559-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4e559-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4e559-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
