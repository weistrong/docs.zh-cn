---
description: 了解详细信息： ICorDebugStepper2：： SetJMC 方法
title: ICorDebugStepper2::SetJMC 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStepper2.SetJMC
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper2::SetJMC
helpviewer_keywords:
- ICorDebugStepper2::SetJMC method [.NET Framework debugging]
- SetJMC method [.NET Framework debugging]
ms.assetid: f5cdc135-6db4-4b32-9dd1-260ec58b774f
topic_type:
- apiref
ms.openlocfilehash: 07178ab90bb392e64c9d8a8fddf961efbb268002
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717532"
---
# <a name="icordebugstepper2setjmc-method"></a><span data-ttu-id="db51e-103">ICorDebugStepper2::SetJMC 方法</span><span class="sxs-lookup"><span data-stu-id="db51e-103">ICorDebugStepper2::SetJMC Method</span></span>

<span data-ttu-id="db51e-104">设置一个值，该值指定此 ICorDebugStepper 是否仅通过应用程序开发人员编写的代码执行步骤。</span><span class="sxs-lookup"><span data-stu-id="db51e-104">Sets a value that specifies whether this ICorDebugStepper steps only through code that is authored by an application's developer.</span></span> <span data-ttu-id="db51e-105">此过程也称为 (JMC) 调试的 "仅我的代码"。</span><span class="sxs-lookup"><span data-stu-id="db51e-105">This process is also known as just my code (JMC) debugging.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db51e-106">语法</span><span class="sxs-lookup"><span data-stu-id="db51e-106">Syntax</span></span>  
  
```cpp  
HRESULT SetJMC (  
    [in] BOOL    fIsJMCStepper  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="db51e-107">参数</span><span class="sxs-lookup"><span data-stu-id="db51e-107">Parameters</span></span>  

 `fIsJMCStepper`  
 <span data-ttu-id="db51e-108">中如果设置为， `true` 则仅通过由应用程序开发人员编写的代码执行，否则设置为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="db51e-108">[in] Set to `true` to step only through code that is authored by an application's developer; otherwise, set to `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db51e-109">要求</span><span class="sxs-lookup"><span data-stu-id="db51e-109">Requirements</span></span>  

 <span data-ttu-id="db51e-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="db51e-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="db51e-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="db51e-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="db51e-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="db51e-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="db51e-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="db51e-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
