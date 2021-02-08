---
description: 了解详细信息： ICorDebug：： Initialize 方法
title: ICorDebug::Initialize 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.Initialize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::Initialize
helpviewer_keywords:
- Initialize method, ICorDebug interface [.NET Framework debugging]
- ICorDebug::Initialize method [.NET Framework debugging]
ms.assetid: 6fae3b23-5c9f-47c0-85d8-6bb75e050786
topic_type:
- apiref
ms.openlocfilehash: 6b6ddd8c1c21470477420909bcf75906b5731ee6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791590"
---
# <a name="icordebuginitialize-method"></a><span data-ttu-id="29ef6-103">ICorDebug::Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="29ef6-103">ICorDebug::Initialize Method</span></span>

<span data-ttu-id="29ef6-104">初始化 `ICorDebug` 对象。</span><span class="sxs-lookup"><span data-stu-id="29ef6-104">Initializes the `ICorDebug` object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="29ef6-105">语法</span><span class="sxs-lookup"><span data-stu-id="29ef6-105">Syntax</span></span>  
  
```cpp  
HRESULT Initialize ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="29ef6-106">备注</span><span class="sxs-lookup"><span data-stu-id="29ef6-106">Remarks</span></span>  

 <span data-ttu-id="29ef6-107">调试器必须 `Initialize` 在创建时调用来初始化调试服务。</span><span class="sxs-lookup"><span data-stu-id="29ef6-107">The debugger must call `Initialize` at creation time to initialize the debugging services.</span></span> <span data-ttu-id="29ef6-108">调用任何其他方法之前，必须先调用此方法 `ICorDebug` 。</span><span class="sxs-lookup"><span data-stu-id="29ef6-108">This method must be called before any other method on `ICorDebug` is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="29ef6-109">要求</span><span class="sxs-lookup"><span data-stu-id="29ef6-109">Requirements</span></span>  

 <span data-ttu-id="29ef6-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="29ef6-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="29ef6-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="29ef6-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="29ef6-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="29ef6-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="29ef6-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="29ef6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29ef6-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="29ef6-114">See also</span></span>

- [<span data-ttu-id="29ef6-115">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="29ef6-115">ICorDebug Interface</span></span>](icordebug-interface.md)
