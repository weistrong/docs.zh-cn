---
description: 了解详细信息： ICorDebugEval：： NewString 方法
title: ICorDebugEval::NewString 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval.NewString
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::NewString
helpviewer_keywords:
- NewString method [.NET Framework debugging]
- ICorDebugEval::NewString method [.NET Framework debugging]
ms.assetid: 29e7a14b-d50e-4852-bfda-011b76c0c9ee
topic_type:
- apiref
ms.openlocfilehash: 21eb49900d84cb1ad1f68a701998a4a778c3ef17
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693832"
---
# <a name="icordebugevalnewstring-method"></a><span data-ttu-id="58beb-103">ICorDebugEval::NewString 方法</span><span class="sxs-lookup"><span data-stu-id="58beb-103">ICorDebugEval::NewString Method</span></span>

<span data-ttu-id="58beb-104">分配具有指定内容的新字符串实例。</span><span class="sxs-lookup"><span data-stu-id="58beb-104">Allocates a new string instance with the specified contents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58beb-105">语法</span><span class="sxs-lookup"><span data-stu-id="58beb-105">Syntax</span></span>  
  
```cpp  
HRESULT NewString (  
    [in] LPCWSTR   string  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="58beb-106">参数</span><span class="sxs-lookup"><span data-stu-id="58beb-106">Parameters</span></span>  

 `string`  
 <span data-ttu-id="58beb-107">中指向字符串内容的指针。</span><span class="sxs-lookup"><span data-stu-id="58beb-107">[in] Pointer to the contents for the string.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="58beb-108">备注</span><span class="sxs-lookup"><span data-stu-id="58beb-108">Remarks</span></span>  

 <span data-ttu-id="58beb-109">始终在当前执行线程的应用程序域中创建字符串。</span><span class="sxs-lookup"><span data-stu-id="58beb-109">The string is always created in the application domain in which the thread is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="58beb-110">要求</span><span class="sxs-lookup"><span data-stu-id="58beb-110">Requirements</span></span>  

 <span data-ttu-id="58beb-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="58beb-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="58beb-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="58beb-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="58beb-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="58beb-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="58beb-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="58beb-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
