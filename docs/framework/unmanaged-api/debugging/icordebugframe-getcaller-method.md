---
description: 了解详细信息： ICorDebugFrame：： GetCaller 方法
title: ICorDebugFrame::GetCaller 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetCaller
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetCaller
helpviewer_keywords:
- GetCaller method, ICorDebugFrame interface [.NET Framework debugging]
- ICorDebugFrame::GetCaller method [.NET Framework debugging]
ms.assetid: bfdc946b-8238-4eb9-8a85-884049fb0fd4
topic_type:
- apiref
ms.openlocfilehash: a042341f6edfa0e8f6ca00f758107852f9e381cb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693039"
---
# <a name="icordebugframegetcaller-method"></a><span data-ttu-id="3d6b5-103">ICorDebugFrame::GetCaller 方法</span><span class="sxs-lookup"><span data-stu-id="3d6b5-103">ICorDebugFrame::GetCaller Method</span></span>

<span data-ttu-id="3d6b5-104">获取一个指针，该指针指向当前链中调用此帧的 ICorDebugFrame 对象。</span><span class="sxs-lookup"><span data-stu-id="3d6b5-104">Gets a pointer to the ICorDebugFrame object in the current chain that called this frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3d6b5-105">语法</span><span class="sxs-lookup"><span data-stu-id="3d6b5-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCaller (  
    [out] ICorDebugFrame     **ppFrame  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3d6b5-106">参数</span><span class="sxs-lookup"><span data-stu-id="3d6b5-106">Parameters</span></span>  

 `ppFrame`  
 <span data-ttu-id="3d6b5-107">弄指向 `ICorDebugFrame` 表示调用帧的对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="3d6b5-107">[out] A pointer to the address of an `ICorDebugFrame` object that represents the calling frame.</span></span> <span data-ttu-id="3d6b5-108">如果被调用的帧是当前链中最外层的帧，则此值为 null。</span><span class="sxs-lookup"><span data-stu-id="3d6b5-108">This value is null if the called frame is the outermost frame in the current chain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3d6b5-109">要求</span><span class="sxs-lookup"><span data-stu-id="3d6b5-109">Requirements</span></span>  

 <span data-ttu-id="3d6b5-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3d6b5-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3d6b5-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3d6b5-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3d6b5-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3d6b5-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3d6b5-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3d6b5-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
