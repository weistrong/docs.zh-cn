---
description: 了解详细信息： ICorDebugClass：： GetModule 方法
title: ICorDebugClass::GetModule 方法
ms.date: 03/30/2017
api_name:
- ICorDebugClass.GetModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass::GetModule
helpviewer_keywords:
- GetModule method, ICorDebugClass interface [.NET Framework debugging]
- ICorDebugClass::GetModule method [.NET Framework debugging]
ms.assetid: 87029cc4-e5e1-42d5-8b98-655bb7ece520
topic_type:
- apiref
ms.openlocfilehash: 338ea5aeede4a209f7a3e3ed685ae9bd84105890
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711534"
---
# <a name="icordebugclassgetmodule-method"></a><span data-ttu-id="b4d90-103">ICorDebugClass::GetModule 方法</span><span class="sxs-lookup"><span data-stu-id="b4d90-103">ICorDebugClass::GetModule Method</span></span>

<span data-ttu-id="b4d90-104">获取定义此类的模块。</span><span class="sxs-lookup"><span data-stu-id="b4d90-104">Gets the module that defines this class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b4d90-105">语法</span><span class="sxs-lookup"><span data-stu-id="b4d90-105">Syntax</span></span>  
  
```cpp  
HRESULT GetModule (  
    [out] ICorDebugModule    **pModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b4d90-106">参数</span><span class="sxs-lookup"><span data-stu-id="b4d90-106">Parameters</span></span>  

 `pModule`  
 <span data-ttu-id="b4d90-107">弄指向 ICorDebugModule 对象的地址的指针，该对象表示在其中定义此类的模块。</span><span class="sxs-lookup"><span data-stu-id="b4d90-107">[out] A pointer to the address of an ICorDebugModule object that represents the module in which this class is defined.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b4d90-108">要求</span><span class="sxs-lookup"><span data-stu-id="b4d90-108">Requirements</span></span>  

 <span data-ttu-id="b4d90-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b4d90-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b4d90-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b4d90-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b4d90-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b4d90-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b4d90-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b4d90-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
