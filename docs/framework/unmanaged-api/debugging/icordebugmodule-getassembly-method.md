---
description: 了解详细信息： ICorDebugModule：： GetAssembly 方法
title: ICorDebugModule::GetAssembly 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetAssembly
helpviewer_keywords:
- ICorDebugModule::GetAssembly method [.NET Framework debugging]
- GetAssembly method [.NET Framework debugging]
ms.assetid: 989762c4-3d15-4485-b8ee-69e0fa8ec895
topic_type:
- apiref
ms.openlocfilehash: 88bda923cd4c3ebfa5da6b3343e1cead4cebbad9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722603"
---
# <a name="icordebugmodulegetassembly-method"></a><span data-ttu-id="ea6e0-103">ICorDebugModule::GetAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="ea6e0-103">ICorDebugModule::GetAssembly Method</span></span>

<span data-ttu-id="ea6e0-104">获取包含此模块的程序集。</span><span class="sxs-lookup"><span data-stu-id="ea6e0-104">Gets the containing assembly for this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea6e0-105">语法</span><span class="sxs-lookup"><span data-stu-id="ea6e0-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAssembly(  
    [out] ICorDebugAssembly **ppAssembly  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ea6e0-106">参数</span><span class="sxs-lookup"><span data-stu-id="ea6e0-106">Parameters</span></span>  

 `ppAssembly`  
 <span data-ttu-id="ea6e0-107">弄指向 ICorDebugAssembly 对象的指针，该对象表示包含此模块的程序集。</span><span class="sxs-lookup"><span data-stu-id="ea6e0-107">[out] A pointer to an ICorDebugAssembly object that represents the assembly containing this module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ea6e0-108">要求</span><span class="sxs-lookup"><span data-stu-id="ea6e0-108">Requirements</span></span>  

 <span data-ttu-id="ea6e0-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ea6e0-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ea6e0-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ea6e0-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ea6e0-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ea6e0-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ea6e0-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ea6e0-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
