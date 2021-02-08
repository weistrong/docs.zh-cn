---
description: 了解详细信息： ICorDebugType：： GetRank 方法
title: ICorDebugType::GetRank 方法
ms.date: 03/30/2017
api_name:
- ICorDebugType.GetRank
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::GetRank
helpviewer_keywords:
- GetRank method, ICorDebugType interface [.NET Framework debugging]
- ICorDebugType::GetRank method [.NET Framework debugging]
ms.assetid: 72d3d927-f590-4f2d-8f60-448f3dfb96af
topic_type:
- apiref
ms.openlocfilehash: e13416856f900846d2df4b8a39303cf0b6a48ebc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800898"
---
# <a name="icordebugtypegetrank-method"></a><span data-ttu-id="7d79e-103">ICorDebugType::GetRank 方法</span><span class="sxs-lookup"><span data-stu-id="7d79e-103">ICorDebugType::GetRank Method</span></span>

<span data-ttu-id="7d79e-104">获取数组类型中的维度数。</span><span class="sxs-lookup"><span data-stu-id="7d79e-104">Gets the number of dimensions in an array type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d79e-105">语法</span><span class="sxs-lookup"><span data-stu-id="7d79e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRank (  
    [out] ULONG32   *pnRank  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7d79e-106">参数</span><span class="sxs-lookup"><span data-stu-id="7d79e-106">Parameters</span></span>  

 `pnRank`  
 <span data-ttu-id="7d79e-107">弄指向维度数的指针。</span><span class="sxs-lookup"><span data-stu-id="7d79e-107">[out] A pointer to the number of dimensions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7d79e-108">要求</span><span class="sxs-lookup"><span data-stu-id="7d79e-108">Requirements</span></span>  

 <span data-ttu-id="7d79e-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7d79e-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7d79e-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7d79e-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7d79e-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7d79e-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7d79e-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7d79e-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
