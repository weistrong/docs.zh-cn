---
description: 了解详细信息： ICorDebugFunction：： GetLocalVarSigToken 方法
title: ICorDebugFunction::GetLocalVarSigToken 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetLocalVarSigToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetLocalVarSigToken
helpviewer_keywords:
- ICorDebugFunction::GetLocalVarSigToken method [.NET Framework debugging]
- GetLocalVarSigToken method [.NET Framework debugging]
ms.assetid: 31e53494-bcc9-4981-91a4-f7e0f02cad48
topic_type:
- apiref
ms.openlocfilehash: cd7fb03829285ddcb1da2f1a93985fa1f98d3d39
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692493"
---
# <a name="icordebugfunctiongetlocalvarsigtoken-method"></a><span data-ttu-id="48681-103">ICorDebugFunction::GetLocalVarSigToken 方法</span><span class="sxs-lookup"><span data-stu-id="48681-103">ICorDebugFunction::GetLocalVarSigToken Method</span></span>

<span data-ttu-id="48681-104">获取此 ICorDebugFunction 实例所表示的函数的局部变量签名的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="48681-104">Gets the metadata token for the local variable signature of the function that is represented by this ICorDebugFunction instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="48681-105">语法</span><span class="sxs-lookup"><span data-stu-id="48681-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLocalVarSigToken (  
    [out] mdSignature *pmdSig  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="48681-106">参数</span><span class="sxs-lookup"><span data-stu-id="48681-106">Parameters</span></span>  

 `pmdSig`  
 <span data-ttu-id="48681-107">弄一个指针，指向 `mdSignature` 此函数的局部变量签名的标记， `mdSignatureNil` 如果此函数没有本地变量，则为。</span><span class="sxs-lookup"><span data-stu-id="48681-107">[out] A pointer to the `mdSignature` token for the local variable signature of this function, or `mdSignatureNil`, if this function has no local variables.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="48681-108">要求</span><span class="sxs-lookup"><span data-stu-id="48681-108">Requirements</span></span>  

 <span data-ttu-id="48681-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="48681-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="48681-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="48681-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="48681-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="48681-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="48681-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="48681-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
