---
description: 了解详细信息： ICorDebugFunction：： GetILCode 方法
title: ICorDebugFunction::GetILCode 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetILCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetILCode
helpviewer_keywords:
- ICorDebugFunction::GetILCode method [.NET Framework debugging]
- GetILCode method [.NET Framework debugging]
ms.assetid: f794dd47-a7cd-47f6-96e9-a41a4dae8e72
topic_type:
- apiref
ms.openlocfilehash: 3b7bb29a028b189b24d3fbf02edc8190d9989a51
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692519"
---
# <a name="icordebugfunctiongetilcode-method"></a><span data-ttu-id="30a7f-103">ICorDebugFunction::GetILCode 方法</span><span class="sxs-lookup"><span data-stu-id="30a7f-103">ICorDebugFunction::GetILCode Method</span></span>

<span data-ttu-id="30a7f-104">获取 ICorDebugCode 实例，它表示与此 ICorDebugFunction 对象关联的 Microsoft 中间语言 (MSIL) 代码。</span><span class="sxs-lookup"><span data-stu-id="30a7f-104">Gets the ICorDebugCode instance that represents the Microsoft intermediate language (MSIL) code associated with this ICorDebugFunction object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30a7f-105">语法</span><span class="sxs-lookup"><span data-stu-id="30a7f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetILCode (  
    [out] ICorDebugCode **ppCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="30a7f-106">参数</span><span class="sxs-lookup"><span data-stu-id="30a7f-106">Parameters</span></span>  

 `ppCode`  
 <span data-ttu-id="30a7f-107">弄指向实例的指针 `ICorDebugCode` ，如果该函数未编译为 MSIL，则为 null。</span><span class="sxs-lookup"><span data-stu-id="30a7f-107">[out] A pointer to the `ICorDebugCode` instance, or null, if the function was not compiled into MSIL.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="30a7f-108">备注</span><span class="sxs-lookup"><span data-stu-id="30a7f-108">Remarks</span></span>  

 <span data-ttu-id="30a7f-109">如果此函数允许使用 "编辑并继续"，则该 `GetILCode` 方法将在公共语言运行时 (CLR) 中获取与此函数的编辑版本对应的 MSIL 代码。</span><span class="sxs-lookup"><span data-stu-id="30a7f-109">If Edit and Continue has been allowed on this function, the `GetILCode` method will get the MSIL code corresponding to this function's edited version of the code in the common language runtime (CLR).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="30a7f-110">要求</span><span class="sxs-lookup"><span data-stu-id="30a7f-110">Requirements</span></span>  

 <span data-ttu-id="30a7f-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="30a7f-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="30a7f-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="30a7f-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="30a7f-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="30a7f-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="30a7f-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="30a7f-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
