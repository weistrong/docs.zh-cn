---
description: 了解详细信息： ICorDebugAppDomain：： EnumerateSteppers 方法
title: ICorDebugAppDomain::EnumerateSteppers 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.EnumerateSteppers
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::EnumerateSteppers
helpviewer_keywords:
- ICorDebugAppDomain::EnumerateSteppers method [.NET Framework debugging]
- EnumerateSteppers method [.NET Framework debugging]
ms.assetid: 3f3c4503-570e-44c1-ae6a-a3c6b840c732
topic_type:
- apiref
ms.openlocfilehash: a9c7f8b1486522b4740ec18c575c9876512b7d8c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754246"
---
# <a name="icordebugappdomainenumeratesteppers-method"></a><span data-ttu-id="c9b43-103">ICorDebugAppDomain::EnumerateSteppers 方法</span><span class="sxs-lookup"><span data-stu-id="c9b43-103">ICorDebugAppDomain::EnumerateSteppers Method</span></span>

<span data-ttu-id="c9b43-104">获取应用程序域中所有活动 steppers 的枚举器。</span><span class="sxs-lookup"><span data-stu-id="c9b43-104">Gets an enumerator for all active steppers in the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9b43-105">语法</span><span class="sxs-lookup"><span data-stu-id="c9b43-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateSteppers (  
    [out] ICorDebugStepperEnum   **ppSteppers  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c9b43-106">参数</span><span class="sxs-lookup"><span data-stu-id="c9b43-106">Parameters</span></span>  

 `ppSteppers`  
 <span data-ttu-id="c9b43-107">弄指向 ICorDebugStepperEnum 对象地址的指针，该对象是应用程序域中所有活动 steppers 的枚举器。</span><span class="sxs-lookup"><span data-stu-id="c9b43-107">[out] A pointer to the address of an ICorDebugStepperEnum object that is the enumerator for all active steppers in the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c9b43-108">要求</span><span class="sxs-lookup"><span data-stu-id="c9b43-108">Requirements</span></span>  

 <span data-ttu-id="c9b43-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c9b43-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c9b43-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c9b43-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c9b43-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c9b43-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c9b43-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c9b43-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
