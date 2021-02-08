---
description: 了解详细信息： ICorDebugInternalFrame：： GetFrameType 方法
title: ICorDebugInternalFrame::GetFrameType 方法
ms.date: 03/30/2017
api_name:
- ICorDebugInternalFrame.GetFrameType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugInternalFrame::GetFrameType
helpviewer_keywords:
- GetFrameType method [.NET Framework debugging]
- ICorDebugInternalFrame::GetFrameType method [.NET Framework debugging]
ms.assetid: da278a29-dc2e-4bf7-96ce-801bdc4d7025
topic_type:
- apiref
ms.openlocfilehash: ea96f032ebfa5914503287d124242b74a84ea11f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791174"
---
# <a name="icordebuginternalframegetframetype-method"></a><span data-ttu-id="b8660-103">ICorDebugInternalFrame::GetFrameType 方法</span><span class="sxs-lookup"><span data-stu-id="b8660-103">ICorDebugInternalFrame::GetFrameType Method</span></span>

<span data-ttu-id="b8660-104">获取此内部帧的类型。</span><span class="sxs-lookup"><span data-stu-id="b8660-104">Gets the type of this internal frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b8660-105">语法</span><span class="sxs-lookup"><span data-stu-id="b8660-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFrameType (  
    [out] CorDebugInternalFrameType  *pType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b8660-106">参数</span><span class="sxs-lookup"><span data-stu-id="b8660-106">Parameters</span></span>  

 `pType`  
 <span data-ttu-id="b8660-107">弄一个指针，指向 CorDebugInternalFrameType 枚举的值，该值指示由此对象表示的内部帧的类型 `ICorDebugInternalFrame` 。</span><span class="sxs-lookup"><span data-stu-id="b8660-107">[out] A pointer to a value of the CorDebugInternalFrameType enumeration that indicates the type of internal frame represented by this `ICorDebugInternalFrame` object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b8660-108">备注</span><span class="sxs-lookup"><span data-stu-id="b8660-108">Remarks</span></span>  

 <span data-ttu-id="b8660-109">内部帧类型永远不会 STUBFRAME_NONE。</span><span class="sxs-lookup"><span data-stu-id="b8660-109">The internal frame type will never be STUBFRAME_NONE.</span></span> <span data-ttu-id="b8660-110">调试器应正常忽略无法识别的内部帧类型。</span><span class="sxs-lookup"><span data-stu-id="b8660-110">Debuggers should gracefully ignore unrecognized internal frame types.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b8660-111">要求</span><span class="sxs-lookup"><span data-stu-id="b8660-111">Requirements</span></span>  

 <span data-ttu-id="b8660-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b8660-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b8660-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b8660-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b8660-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b8660-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b8660-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b8660-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
