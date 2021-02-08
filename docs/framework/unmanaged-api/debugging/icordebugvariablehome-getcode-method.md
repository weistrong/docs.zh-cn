---
description: 了解详细信息： ICorDebugVariableHome：： GetCode 方法
title: ICorDebugVariableHome：： GetCode 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetCode
helpviewer_keywords:
- ICorDebugVariableHome::GetCode method [.NET Framework debugging]
- GetCode method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: ef002890-4a7b-4a5d-abbf-16c60083f794
topic_type:
- apiref
ms.openlocfilehash: e3ff96816e580fe3cd1cee782dc5bd4166f08a14
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794632"
---
# <a name="icordebugvariablehomegetcode-method"></a><span data-ttu-id="84d5f-103">ICorDebugVariableHome：： GetCode 方法</span><span class="sxs-lookup"><span data-stu-id="84d5f-103">ICorDebugVariableHome::GetCode Method</span></span>

<span data-ttu-id="84d5f-104">获取包含此 [ICorDebugVariableHome](icordebugvariablehome-interface.md) 对象的 "ICorDebugCode" 实例。</span><span class="sxs-lookup"><span data-stu-id="84d5f-104">Gets the "ICorDebugCode" instance that contains this [ICorDebugVariableHome](icordebugvariablehome-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84d5f-105">语法</span><span class="sxs-lookup"><span data-stu-id="84d5f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCode(  
    [out] ICorDebugCode **ppCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="84d5f-106">参数</span><span class="sxs-lookup"><span data-stu-id="84d5f-106">Parameters</span></span>  

 `ppCode`  
 <span data-ttu-id="84d5f-107">弄一个指针，指向包含此 [ICorDebugVariableHome](icordebugvariablehome-interface.md) 对象的 "ICorDebugCode" 实例的地址。</span><span class="sxs-lookup"><span data-stu-id="84d5f-107">[out] A pointer to the address of the "ICorDebugCode" instance that contains this [ICorDebugVariableHome](icordebugvariablehome-interface.md) object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="84d5f-108">要求</span><span class="sxs-lookup"><span data-stu-id="84d5f-108">Requirements</span></span>  

 <span data-ttu-id="84d5f-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="84d5f-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="84d5f-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="84d5f-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="84d5f-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="84d5f-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="84d5f-112">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="84d5f-112">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84d5f-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="84d5f-113">See also</span></span>

- [<span data-ttu-id="84d5f-114">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="84d5f-114">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
