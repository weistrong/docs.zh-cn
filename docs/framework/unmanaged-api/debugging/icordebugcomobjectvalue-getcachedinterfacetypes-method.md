---
description: 了解详细信息： ICorDebugComObjectValue：： GetCachedInterfaceTypes 方法
title: ICorDebugComObjectValue::GetCachedInterfaceTypes 方法
ms.date: 03/30/2017
api_name:
- ICorDebugComObjectValue::GetCachedInterfaceTypes
api_location:
- mscordbi.dll
f1_keywords:
- ICorDebugComObjectValue::GetCachedInterfaceTypes
helpviewer_keywords:
- GetCachedInterface method, ICorDebugComObjectValue interface [.NET Framework debugging]
- ICorDebugComObjectValue::GetCachedInterface method [.NET Framework debugging]
ms.assetid: d492284f-d3c5-4614-adb8-d718d5042500
topic_type:
- apiref
ms.openlocfilehash: b1c65979895dfaeacae3d171adbcfd1455b7030d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764614"
---
# <a name="icordebugcomobjectvaluegetcachedinterfacetypes-method"></a><span data-ttu-id="fadaf-103">ICorDebugComObjectValue::GetCachedInterfaceTypes 方法</span><span class="sxs-lookup"><span data-stu-id="fadaf-103">ICorDebugComObjectValue::GetCachedInterfaceTypes Method</span></span>

<span data-ttu-id="fadaf-104">为当前对象已强制转换为或用作的接口类型提供枚举器。</span><span class="sxs-lookup"><span data-stu-id="fadaf-104">Provides an enumerator for the interface types that the current object has been cast to or used as.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fadaf-105">语法</span><span class="sxs-lookup"><span data-stu-id="fadaf-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCachedInterfaceTypes(  
    [in] BOOL bIInspectableOnly,  
    [out] ICorDebugTypeEnum **ppInterfacesEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fadaf-106">参数</span><span class="sxs-lookup"><span data-stu-id="fadaf-106">Parameters</span></span>  

 `bIInspectableOnly`  
 <span data-ttu-id="fadaf-107">中一个值，该值指示方法是只返回 (`IInspectable` 接口) 或由运行时可调用 (包装器缓存的所有 COM 接口接口 Windows 运行时接口) 。</span><span class="sxs-lookup"><span data-stu-id="fadaf-107">[in] A value that indicates whether the method returns only Windows Runtime interfaces (`IInspectable` interfaces) or all COM interfaces cached by the runtime callable wrapper (RCW).</span></span>  
  
 `ppInterfacesEnum`  
 <span data-ttu-id="fadaf-108">弄指向 ICorDebugTypeEnum 枚举器地址的指针，该枚举数提供对 ICorDebugType 对象的访问，这些对象表示根据筛选的已筛选的缓存接口类型 `bIInspectableOnly` 。</span><span class="sxs-lookup"><span data-stu-id="fadaf-108">[out] A pointer to the address of an ICorDebugTypeEnum enumerator that provides access to ICorDebugType objects that represent cached interface types filtered according to `bIInspectableOnly`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fadaf-109">备注</span><span class="sxs-lookup"><span data-stu-id="fadaf-109">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fadaf-110">要求</span><span class="sxs-lookup"><span data-stu-id="fadaf-110">Requirements</span></span>  

 <span data-ttu-id="fadaf-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fadaf-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fadaf-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fadaf-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fadaf-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fadaf-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fadaf-114">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fadaf-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fadaf-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="fadaf-115">See also</span></span>

- [<span data-ttu-id="fadaf-116">ICorDebugComObjectValue 接口</span><span class="sxs-lookup"><span data-stu-id="fadaf-116">ICorDebugComObjectValue Interface</span></span>](icordebugcomobjectvalue-interface.md)
- [<span data-ttu-id="fadaf-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="fadaf-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
