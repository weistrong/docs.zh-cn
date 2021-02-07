---
description: 了解详细信息： ICorDebugFrame：： GetCallee 方法
title: ICorDebugFrame::GetCallee 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetCallee
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetCallee
helpviewer_keywords:
- ICorDebugFrame::GetCallee method [.NET Framework debugging]
- GetCallee method, ICorDebugFrame interface [.NET Framework debugging]
ms.assetid: 92d8136d-0436-4c7e-a6b2-80765f892a0d
topic_type:
- apiref
ms.openlocfilehash: 85b64933cb2f180445b88f7b19f8b78f1788252e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693065"
---
# <a name="icordebugframegetcallee-method"></a><span data-ttu-id="b6e00-103">ICorDebugFrame::GetCallee 方法</span><span class="sxs-lookup"><span data-stu-id="b6e00-103">ICorDebugFrame::GetCallee Method</span></span>

<span data-ttu-id="b6e00-104">获取一个指针，该指针指向此框架调用的当前链中的 ICorDebugFrame 对象。</span><span class="sxs-lookup"><span data-stu-id="b6e00-104">Gets a pointer to the ICorDebugFrame object in the current chain that this frame called.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6e00-105">语法</span><span class="sxs-lookup"><span data-stu-id="b6e00-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCallee (  
    [out] ICorDebugFrame     **ppFrame  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b6e00-106">参数</span><span class="sxs-lookup"><span data-stu-id="b6e00-106">Parameters</span></span>  

 `ppFrame`  
 <span data-ttu-id="b6e00-107">弄一个指针，指向 `ICorDebugFrame` 表示被调用的帧的对象的地址。</span><span class="sxs-lookup"><span data-stu-id="b6e00-107">[out] A pointer to the address of an `ICorDebugFrame` object that represents the called frame.</span></span> <span data-ttu-id="b6e00-108">如果调用帧是当前链中最内层的帧，则此值为 null。</span><span class="sxs-lookup"><span data-stu-id="b6e00-108">This value is null if the calling frame is the innermost frame in the current chain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b6e00-109">要求</span><span class="sxs-lookup"><span data-stu-id="b6e00-109">Requirements</span></span>  

 <span data-ttu-id="b6e00-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b6e00-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b6e00-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b6e00-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b6e00-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b6e00-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b6e00-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b6e00-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
