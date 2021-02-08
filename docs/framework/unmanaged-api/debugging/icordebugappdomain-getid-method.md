---
description: 了解详细信息： ICorDebugAppDomain：： GetId 方法
title: ICorDebugAppDomain::GetId 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetId
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetId
helpviewer_keywords:
- GetId method, ICorDebugAppDomain interface [.NET Framework debugging]
- ICorDebugAppDomain::GetId method [.NET Framework debugging]
ms.assetid: 32c27576-71fa-42ee-8230-67b92913ea08
topic_type:
- apiref
ms.openlocfilehash: ea660aa08e93e4ce2d97f1e7ae05b261db91118f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772455"
---
# <a name="icordebugappdomaingetid-method"></a><span data-ttu-id="0e4a4-103">ICorDebugAppDomain::GetId 方法</span><span class="sxs-lookup"><span data-stu-id="0e4a4-103">ICorDebugAppDomain::GetId Method</span></span>

<span data-ttu-id="0e4a4-104">获取应用程序域的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="0e4a4-104">Gets the unique identifier of the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e4a4-105">语法</span><span class="sxs-lookup"><span data-stu-id="0e4a4-105">Syntax</span></span>  
  
```cpp  
HRESULT GetID (  
    [out] ULONG32   *pId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0e4a4-106">参数</span><span class="sxs-lookup"><span data-stu-id="0e4a4-106">Parameters</span></span>  

 `pId`  
 <span data-ttu-id="0e4a4-107">弄应用程序域的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="0e4a4-107">[out] The unique identifier of the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0e4a4-108">备注</span><span class="sxs-lookup"><span data-stu-id="0e4a4-108">Remarks</span></span>  

 <span data-ttu-id="0e4a4-109">应用程序域的标识符在包含进程中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0e4a4-109">The identifier for the application domain is unique within the containing process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0e4a4-110">要求</span><span class="sxs-lookup"><span data-stu-id="0e4a4-110">Requirements</span></span>  

 <span data-ttu-id="0e4a4-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0e4a4-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0e4a4-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0e4a4-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0e4a4-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0e4a4-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0e4a4-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0e4a4-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
