---
description: 了解详细信息： ICorDebugModule：： GetSize 方法
title: ICorDebugModule::GetSize 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetSize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetSize
helpviewer_keywords:
- GetSize method, ICorDebugModule interface [.NET Framework debugging]
- ICorDebugModule::GetSize method [.NET Framework debugging]
ms.assetid: 5c68375d-145d-46ef-a7c8-2dc4257472de
topic_type:
- apiref
ms.openlocfilehash: b2179c8830911e417ccd482fe72438c4cd7fd3df
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660136"
---
# <a name="icordebugmodulegetsize-method"></a><span data-ttu-id="42bf1-103">ICorDebugModule::GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="42bf1-103">ICorDebugModule::GetSize Method</span></span>

<span data-ttu-id="42bf1-104">获取模块的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="42bf1-104">Gets the size, in bytes, of the module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42bf1-105">语法</span><span class="sxs-lookup"><span data-stu-id="42bf1-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSize(  
    [out] ULONG32 *pcBytes  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="42bf1-106">参数</span><span class="sxs-lookup"><span data-stu-id="42bf1-106">Parameters</span></span>  

 `pcBytes`  
 <span data-ttu-id="42bf1-107">弄模块的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="42bf1-107">[out] The size of the module in bytes.</span></span>  
  
 <span data-ttu-id="42bf1-108">如果该模块是通过本机映像生成器生成的 ( # A0) ，则该模块的大小将为零。</span><span class="sxs-lookup"><span data-stu-id="42bf1-108">If the module was produced from the native image generator (NGen.exe), the size of the module will be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="42bf1-109">要求</span><span class="sxs-lookup"><span data-stu-id="42bf1-109">Requirements</span></span>  

 <span data-ttu-id="42bf1-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="42bf1-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="42bf1-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="42bf1-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="42bf1-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="42bf1-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="42bf1-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="42bf1-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
