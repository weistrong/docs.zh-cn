---
description: 了解详细信息： ICorDebugModule：： GetFunctionFromToken 方法
title: ICorDebugModule::GetFunctionFromToken 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetFunctionFromToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetFunctionFromToken
helpviewer_keywords:
- GetFunctionFromToken method, ICorDebugModule interface [.NET Framework debugging]
- ICorDebugModule::GetFunctionFromToken method [.NET Framework debugging]
ms.assetid: 6fe12194-4ef7-43c1-9570-ade35ccf127a
topic_type:
- apiref
ms.openlocfilehash: d6da43441f3774cff44a6f867c3ccf2a8581ebab
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691644"
---
# <a name="icordebugmodulegetfunctionfromtoken-method"></a><span data-ttu-id="95fab-103">ICorDebugModule::GetFunctionFromToken 方法</span><span class="sxs-lookup"><span data-stu-id="95fab-103">ICorDebugModule::GetFunctionFromToken Method</span></span>

<span data-ttu-id="95fab-104">获取元数据标记指定的函数。</span><span class="sxs-lookup"><span data-stu-id="95fab-104">Gets the function that is specified by the metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95fab-105">语法</span><span class="sxs-lookup"><span data-stu-id="95fab-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFunctionFromToken(  
    [in] mdMethodDef methodDef,  
    [out] ICorDebugFunction **ppFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="95fab-106">参数</span><span class="sxs-lookup"><span data-stu-id="95fab-106">Parameters</span></span>  

 `methodDef`  
 <span data-ttu-id="95fab-107">中 `mdMethodDef` 引用函数的元数据的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="95fab-107">[in] A `mdMethodDef` metadata token that references the function's metadata.</span></span>  
  
 `ppFunction`  
 <span data-ttu-id="95fab-108">弄指向表示函数的 ICorDebugFunction 接口对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="95fab-108">[out] A pointer to the address of a ICorDebugFunction interface object that represents the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="95fab-109">备注</span><span class="sxs-lookup"><span data-stu-id="95fab-109">Remarks</span></span>  

 <span data-ttu-id="95fab-110">`GetFunctionFromToken`如果传入的值 `methodDef` 不引用 Microsoft 中间语言 (MSIL) 方法，则方法将返回 CORDBG_E_FUNCTION_NOT_IL HRESULT。</span><span class="sxs-lookup"><span data-stu-id="95fab-110">The `GetFunctionFromToken` method returns a CORDBG_E_FUNCTION_NOT_IL HRESULT if the value passed in `methodDef` does not refer to a Microsoft intermediate language (MSIL) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="95fab-111">要求</span><span class="sxs-lookup"><span data-stu-id="95fab-111">Requirements</span></span>  

 <span data-ttu-id="95fab-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="95fab-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="95fab-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="95fab-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="95fab-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="95fab-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="95fab-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="95fab-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
