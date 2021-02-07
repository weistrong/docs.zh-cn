---
description: 了解详细信息： ICorDebugHandleValue：:D ispose 方法
title: ICorDebugHandleValue::Dispose 方法
ms.date: 03/30/2017
api_name:
- ICorDebugHandleValue.Dispose
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHandleValue::Dispose
helpviewer_keywords:
- ICorDebugHandleValue::Dispose method [.NET Framework debugging]
- Dispose method [.NET Framework debugging]
ms.assetid: c1542811-0a7f-4235-bcfd-b24370d6f24b
topic_type:
- apiref
ms.openlocfilehash: e39ff66137e12ebc939e1e060dd37ea8af9b623a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692051"
---
# <a name="icordebughandlevaluedispose-method"></a><span data-ttu-id="96719-103">ICorDebugHandleValue::Dispose 方法</span><span class="sxs-lookup"><span data-stu-id="96719-103">ICorDebugHandleValue::Dispose Method</span></span>

<span data-ttu-id="96719-104">释放此 ICorDebugHandleValue 对象引用的句柄，无需显式释放接口指针。</span><span class="sxs-lookup"><span data-stu-id="96719-104">Releases the handle referenced by this ICorDebugHandleValue object without explicitly releasing the interface pointer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96719-105">语法</span><span class="sxs-lookup"><span data-stu-id="96719-105">Syntax</span></span>  
  
```cpp  
HRESULT Dispose ();  
```  
  
## <a name="requirements"></a><span data-ttu-id="96719-106">要求</span><span class="sxs-lookup"><span data-stu-id="96719-106">Requirements</span></span>  

 <span data-ttu-id="96719-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="96719-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="96719-108">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="96719-108">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="96719-109">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="96719-109">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="96719-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="96719-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
