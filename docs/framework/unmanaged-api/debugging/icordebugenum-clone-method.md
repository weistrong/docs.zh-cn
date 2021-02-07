---
description: 了解详细信息： ICorDebugEnum：： Clone 方法
title: ICorDebugEnum::Clone 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEnum.Clone
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEnum::Clone
helpviewer_keywords:
- Clone method, ICorDebugEnum interface [.NET Framework debugging]
- ICorDebugEnum::Clone method [.NET Framework debugging]
ms.assetid: 57eefaf3-75cf-4496-bc94-88c0706861b7
topic_type:
- apiref
ms.openlocfilehash: 18219757980870dcf9663477d195068a76814de1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694552"
---
# <a name="icordebugenumclone-method"></a><span data-ttu-id="52a04-103">ICorDebugEnum::Clone 方法</span><span class="sxs-lookup"><span data-stu-id="52a04-103">ICorDebugEnum::Clone Method</span></span>

<span data-ttu-id="52a04-104">创建此 ICorDebugEnum 对象的副本。</span><span class="sxs-lookup"><span data-stu-id="52a04-104">Creates a copy of this ICorDebugEnum object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="52a04-105">语法</span><span class="sxs-lookup"><span data-stu-id="52a04-105">Syntax</span></span>  
  
```cpp  
HRESULT Clone (  
    [out] ICorDebugEnum **ppEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="52a04-106">参数</span><span class="sxs-lookup"><span data-stu-id="52a04-106">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="52a04-107">弄指向作为 `ICorDebugEnum` 此对象副本的对象地址的指针 `ICorDebugEnum` 。</span><span class="sxs-lookup"><span data-stu-id="52a04-107">[out] A pointer to the address of an `ICorDebugEnum` object that is a copy of this `ICorDebugEnum` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="52a04-108">要求</span><span class="sxs-lookup"><span data-stu-id="52a04-108">Requirements</span></span>  

 <span data-ttu-id="52a04-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="52a04-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="52a04-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="52a04-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="52a04-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="52a04-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="52a04-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="52a04-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
