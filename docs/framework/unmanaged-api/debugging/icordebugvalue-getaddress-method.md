---
description: 了解详细信息： ICorDebugValue：： GetAddress 方法
title: ICorDebugValue::GetAddress 方法
ms.date: 03/30/2017
api_name:
- ICorDebugValue.GetAddress
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue::GetAddress
helpviewer_keywords:
- ICorDebugValue::GetAddress method [.NET Framework debugging]
- GetAddress method, ICorDebugValue interface [.NET Framework debugging]
ms.assetid: a247c792-45e1-4538-9e1f-b46acca4a463
topic_type:
- apiref
ms.openlocfilehash: c922388fbab820e50edffc140be94a2c0920099d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690426"
---
# <a name="icordebugvaluegetaddress-method"></a><span data-ttu-id="36d07-103">ICorDebugValue::GetAddress 方法</span><span class="sxs-lookup"><span data-stu-id="36d07-103">ICorDebugValue::GetAddress Method</span></span>

<span data-ttu-id="36d07-104">获取此 "ICorDebugValue" 对象的地址，该对象处于调试过程中。</span><span class="sxs-lookup"><span data-stu-id="36d07-104">Gets the address of this "ICorDebugValue" object, which is in the process of being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="36d07-105">语法</span><span class="sxs-lookup"><span data-stu-id="36d07-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAddress (  
    [out] CORDB_ADDRESS   *pAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="36d07-106">参数</span><span class="sxs-lookup"><span data-stu-id="36d07-106">Parameters</span></span>  

 `pAddress`  
 <span data-ttu-id="36d07-107">弄指向 `CORDB_ADDRESS` 对象的指针，该对象指定此值对象的地址。</span><span class="sxs-lookup"><span data-stu-id="36d07-107">[out] Pointer to a `CORDB_ADDRESS` object that specifies the address of this value object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="36d07-108">备注</span><span class="sxs-lookup"><span data-stu-id="36d07-108">Remarks</span></span>  

 <span data-ttu-id="36d07-109">如果值不可用，则返回 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="36d07-109">If the value is unavailable, 0 (zero) is returned.</span></span> <span data-ttu-id="36d07-110">如果值至少出现在寄存器中或者存储在垃圾回收器句柄 () 中，则可能会发生这种情况 `GCHandle` 。</span><span class="sxs-lookup"><span data-stu-id="36d07-110">This could happen if the value is at least partly in registers or stored in a garbage collector handle (`GCHandle`).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="36d07-111">要求</span><span class="sxs-lookup"><span data-stu-id="36d07-111">Requirements</span></span>  

 <span data-ttu-id="36d07-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="36d07-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="36d07-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="36d07-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="36d07-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="36d07-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="36d07-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="36d07-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="36d07-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="36d07-116">See also</span></span>
