---
description: 了解详细信息： ICorDebugVariableHome：： GetLocationType 方法
title: ICorDebugVariableHome：： GetLocationType 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetLocationType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetLocationType
helpviewer_keywords:
- ICorDebugVariableHome::GetLocationType method [.NET Framework debugging]
- GetLocationType method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: 88027c55-8ec6-4f1e-a55b-7eefdbbc3515
topic_type:
- apiref
ms.openlocfilehash: 6efe9c045641d162be820961ca75c21a2b8fc14b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728790"
---
# <a name="icordebugvariablehomegetlocationtype-method"></a><span data-ttu-id="c5758-103">ICorDebugVariableHome：： GetLocationType 方法</span><span class="sxs-lookup"><span data-stu-id="c5758-103">ICorDebugVariableHome::GetLocationType Method</span></span>

<span data-ttu-id="c5758-104">获取变量的本机位置的类型。</span><span class="sxs-lookup"><span data-stu-id="c5758-104">Gets the type of the variable's native location.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c5758-105">语法</span><span class="sxs-lookup"><span data-stu-id="c5758-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLocationType(  
    [out] VariableLocationType *pLocationType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c5758-106">参数</span><span class="sxs-lookup"><span data-stu-id="c5758-106">Parameters</span></span>  

 `pLocationType`  
 <span data-ttu-id="c5758-107">弄指向变量的本机位置的类型的指针。</span><span class="sxs-lookup"><span data-stu-id="c5758-107">[out] A pointer to the type of the variable's native location.</span></span>  <span data-ttu-id="c5758-108">有关详细信息，请参阅 [VariableLocationType](variablelocationtype-enumeration.md) 枚举。</span><span class="sxs-lookup"><span data-stu-id="c5758-108">See the [VariableLocationType](variablelocationtype-enumeration.md) enumeration for more information.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c5758-109">要求</span><span class="sxs-lookup"><span data-stu-id="c5758-109">Requirements</span></span>  

 <span data-ttu-id="c5758-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c5758-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c5758-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c5758-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c5758-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c5758-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c5758-113">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c5758-113">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5758-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="c5758-114">See also</span></span>

- [<span data-ttu-id="c5758-115">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="c5758-115">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
- [<span data-ttu-id="c5758-116">VariableLocationType 枚举</span><span class="sxs-lookup"><span data-stu-id="c5758-116">VariableLocationType Enumeration</span></span>](variablelocationtype-enumeration.md)
