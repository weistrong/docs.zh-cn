---
description: 了解详细信息： ICorDebugObjectValue2：： GetVirtualMethodAndType 方法
title: ICorDebugObjectValue2::GetVirtualMethodAndType 方法
ms.date: 03/30/2017
api_name:
- ICorDebugObjectValue2.GetVirtualMethodAndType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectValue2::GetVirtualMethodAndType
helpviewer_keywords:
- GetVirtualMethodAndType method [.NET Framework debugging]
- ICorDebugObjectValue2::GetVirtualMethodAndType method
ms.assetid: 621b4543-a8f7-4117-98e4-930992cd688a
topic_type:
- apiref
ms.openlocfilehash: 73866cc902d60316e3f1f31a86473116c0bff129
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781917"
---
# <a name="icordebugobjectvalue2getvirtualmethodandtype-method"></a><span data-ttu-id="7b106-103">ICorDebugObjectValue2::GetVirtualMethodAndType 方法</span><span class="sxs-lookup"><span data-stu-id="7b106-103">ICorDebugObjectValue2::GetVirtualMethodAndType Method</span></span>

<span data-ttu-id="7b106-104">此方法尚未实现。</span><span class="sxs-lookup"><span data-stu-id="7b106-104">This method is not yet implemented.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b106-105">语法</span><span class="sxs-lookup"><span data-stu-id="7b106-105">Syntax</span></span>  
  
```cpp  
HRESULT GetVirtualMethodAndType (  
    [in] mdMemberRef          memberRef,  
    [out] ICorDebugFunction   **ppFunction,  
    [out] ICorDebugType       **ppType  
);  
```  
  
## <a name="remarks"></a><span data-ttu-id="7b106-106">备注</span><span class="sxs-lookup"><span data-stu-id="7b106-106">Remarks</span></span>  

 <span data-ttu-id="7b106-107">获取指向 "ICorDebugFunction" 和 "ICorDebugType" 实例的接口指针，这些实例表示指定成员引用的派生程度最高的方法和类型。</span><span class="sxs-lookup"><span data-stu-id="7b106-107">Gets interface pointers to the "ICorDebugFunction" and "ICorDebugType" instances that represent the most derived method and type for the specified member reference.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b106-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="7b106-108">See also</span></span>
