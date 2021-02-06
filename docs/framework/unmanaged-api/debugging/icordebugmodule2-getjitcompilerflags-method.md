---
description: 了解详细信息： ICorDebugModule2：： GetJITCompilerFlags 方法
title: ICorDebugModule2::GetJITCompilerFlags 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule2.GetJITCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2::GetJITCompilerFlags
helpviewer_keywords:
- GetJITCompilerFlags method [.NET Framework debugging]
- ICorDebugModule2::GetJITCompilerFlags method [.NET Framework debugging]
ms.assetid: 7212d9f4-989b-44e3-b8d4-ffc35922f6a0
topic_type:
- apiref
ms.openlocfilehash: f1aa01bf2bc92a6fc20687b726ef1c0a6f860a97
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659967"
---
# <a name="icordebugmodule2getjitcompilerflags-method"></a><span data-ttu-id="8a088-103">ICorDebugModule2::GetJITCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="8a088-103">ICorDebugModule2::GetJITCompilerFlags Method</span></span>

<span data-ttu-id="8a088-104">获取用于控制此 ICorDebugModule2 的实时 (JIT) 编译的标志。</span><span class="sxs-lookup"><span data-stu-id="8a088-104">Gets the flags that control the just-in-time (JIT) compilation of this ICorDebugModule2.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a088-105">语法</span><span class="sxs-lookup"><span data-stu-id="8a088-105">Syntax</span></span>  
  
```cpp  
HRESULT GetJITCompilerFlags (  
    [out] DWORD   *pdwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8a088-106">参数</span><span class="sxs-lookup"><span data-stu-id="8a088-106">Parameters</span></span>  

 `pdwFlags`  
 <span data-ttu-id="8a088-107">弄指向控制 JIT 编译的 [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) 枚举的值的指针。</span><span class="sxs-lookup"><span data-stu-id="8a088-107">[out] A pointer to a value of the [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) enumeration that controls the JIT compilation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a088-108">要求</span><span class="sxs-lookup"><span data-stu-id="8a088-108">Requirements</span></span>  

 <span data-ttu-id="8a088-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8a088-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a088-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8a088-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8a088-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8a088-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8a088-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a088-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
