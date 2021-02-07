---
description: 了解详细信息： ICorDebugCode：： GetAddress 方法
title: ICorDebugCode::GetAddress 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetAddress
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetAddress
helpviewer_keywords:
- GetAddress method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetAddress method [.NET Framework debugging]
ms.assetid: cc507cb0-df2e-49c2-b32e-0c3271a8df9a
topic_type:
- apiref
ms.openlocfilehash: 4c074a407d8153703fd92aeddb53e9fa05b0ef01
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711331"
---
# <a name="icordebugcodegetaddress-method"></a><span data-ttu-id="c47b9-103">ICorDebugCode::GetAddress 方法</span><span class="sxs-lookup"><span data-stu-id="c47b9-103">ICorDebugCode::GetAddress Method</span></span>

<span data-ttu-id="c47b9-104">获取此 "ICorDebugCode" 接口表示的代码段 (RVA) 的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="c47b9-104">Gets the relative virtual address (RVA) of the code segment that this "ICorDebugCode" interface represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c47b9-105">语法</span><span class="sxs-lookup"><span data-stu-id="c47b9-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAddress (  
    [out] CORDB_ADDRESS *pStart  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c47b9-106">参数</span><span class="sxs-lookup"><span data-stu-id="c47b9-106">Parameters</span></span>  

 `pStart`  
 <span data-ttu-id="c47b9-107">弄指向代码段的 RVA 的指针。</span><span class="sxs-lookup"><span data-stu-id="c47b9-107">[out] A pointer to the RVA of the code segment.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c47b9-108">要求</span><span class="sxs-lookup"><span data-stu-id="c47b9-108">Requirements</span></span>  

 <span data-ttu-id="c47b9-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c47b9-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c47b9-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c47b9-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c47b9-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c47b9-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c47b9-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c47b9-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
