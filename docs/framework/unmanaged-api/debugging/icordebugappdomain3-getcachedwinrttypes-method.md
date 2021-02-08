---
description: 了解详细信息： ICorDebugAppDomain3：： GetCachedWinRTTypes 方法
title: ICorDebugAppDomain3::GetCachedWinRTTypes 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain3.GetCachedWinRTTypes
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypes
helpviewer_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypes method [.NET Framework debugging]
- GetCachedWinRTTypes method, ICorDebugAppDomain3 interface [.NET Framework debugging]
ms.assetid: 9afd0e04-a403-41e2-9528-a6dcbcdcbd4d
topic_type:
- apiref
ms.openlocfilehash: 813fb6c05d5e1e5f119424c6e983b86b3ff5889d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772232"
---
# <a name="icordebugappdomain3getcachedwinrttypes-method"></a><span data-ttu-id="ac5e4-103">ICorDebugAppDomain3::GetCachedWinRTTypes 方法</span><span class="sxs-lookup"><span data-stu-id="ac5e4-103">ICorDebugAppDomain3::GetCachedWinRTTypes Method</span></span>

<span data-ttu-id="ac5e4-104">获取所有缓存 Windows 运行时类型的枚举器。</span><span class="sxs-lookup"><span data-stu-id="ac5e4-104">Gets an enumerator for all cached Windows Runtime types.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac5e4-105">语法</span><span class="sxs-lookup"><span data-stu-id="ac5e4-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCachedWinRTTypes (
    [out] ICorDebugGuidToTypeEnum **ppGuidToTypeEnum)  
;  
```  
  
## <a name="parameters"></a><span data-ttu-id="ac5e4-106">参数</span><span class="sxs-lookup"><span data-stu-id="ac5e4-106">Parameters</span></span>  

 `ppGuidToTypeEnum`  
 <span data-ttu-id="ac5e4-107">弄指向 [ICorDebugGuidToTypeEnum](icordebugguidtotypeenum-interface.md) 接口对象的指针，该对象可以枚举当前在应用程序域中加载的 Windows 运行时类型的托管表示形式。</span><span class="sxs-lookup"><span data-stu-id="ac5e4-107">[out] A pointer to an [ICorDebugGuidToTypeEnum](icordebugguidtotypeenum-interface.md) interface object that can enumerate the managed representations of Windows Runtime types currently loaded in the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ac5e4-108">要求</span><span class="sxs-lookup"><span data-stu-id="ac5e4-108">Requirements</span></span>  

 <span data-ttu-id="ac5e4-109">**平台：** Windows 运行时</span><span class="sxs-lookup"><span data-stu-id="ac5e4-109">**Platforms:** Windows Runtime</span></span>  
  
 <span data-ttu-id="ac5e4-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ac5e4-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ac5e4-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ac5e4-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ac5e4-112">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ac5e4-112">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac5e4-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="ac5e4-113">See also</span></span>

- [<span data-ttu-id="ac5e4-114">ICorDebugAppDomain3 接口</span><span class="sxs-lookup"><span data-stu-id="ac5e4-114">ICorDebugAppDomain3 Interface</span></span>](icordebugappdomain3-interface.md)
