---
description: 了解详细信息： IcorDebugVariableHome：： GetLiveRange 方法
title: IcorDebugVariableHome：： GetLiveRange 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetLiveRange
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetLiveRange
helpviewer_keywords:
- ICorDebugVariableHome::GetLiveRange method [.NET Framework debugging]
- GetLiveRange method, ICorDebugVariableFrame interface [.NET Framework debugging]
ms.assetid: 87277e1a-1595-4729-9e25-d1c3ac18ce5f
topic_type:
- apiref
ms.openlocfilehash: daa53a164c7660826d44285ce21ecea1b649a727
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800833"
---
# <a name="icordebugvariablehomegetliverange-method"></a><span data-ttu-id="4c5fe-103">IcorDebugVariableHome：： GetLiveRange 方法</span><span class="sxs-lookup"><span data-stu-id="4c5fe-103">IcorDebugVariableHome::GetLiveRange Method</span></span>

<span data-ttu-id="4c5fe-104">获取此变量的生存期的本机范围。</span><span class="sxs-lookup"><span data-stu-id="4c5fe-104">Gets the native range over which this variable is live.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4c5fe-105">语法</span><span class="sxs-lookup"><span data-stu-id="4c5fe-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLiveRange(  
    [out] ULONG32* pStartOffset,  
    [out] ULONG32 *pEndOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4c5fe-106">参数</span><span class="sxs-lookup"><span data-stu-id="4c5fe-106">Parameters</span></span>  

 `pStartOffset`  
 <span data-ttu-id="4c5fe-107">弄变量首次处于活动状态的逻辑偏移量。</span><span class="sxs-lookup"><span data-stu-id="4c5fe-107">[out] The logical offset at which the variable is first live.</span></span>  
  
 `pEndOffset`  
 <span data-ttu-id="4c5fe-108">弄紧跟在变量上一次生存点之后的逻辑偏移量。</span><span class="sxs-lookup"><span data-stu-id="4c5fe-108">[out] The logical offset immediately after the point at which the variable is last live.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4c5fe-109">要求</span><span class="sxs-lookup"><span data-stu-id="4c5fe-109">Requirements</span></span>  

 <span data-ttu-id="4c5fe-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4c5fe-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4c5fe-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4c5fe-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4c5fe-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4c5fe-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4c5fe-113">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4c5fe-113">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c5fe-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="4c5fe-114">See also</span></span>

- [<span data-ttu-id="4c5fe-115">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="4c5fe-115">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
