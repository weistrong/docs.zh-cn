---
description: 了解详细信息： ICorDebugILFrame：： GetArgument 方法
title: ICorDebugILFrame::GetArgument 方法
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.GetArgument
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::GetArgument
helpviewer_keywords:
- GetArgument method [.NET Framework debugging]
- ICorDebugILFrame::GetArgument method [.NET Framework debugging]
ms.assetid: 4e2fd423-f643-4c27-ba5f-41b5ebc3b416
topic_type:
- apiref
ms.openlocfilehash: c845f3c07502f3b1ce564833ee6ef98e3305463f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650503"
---
# <a name="icordebugilframegetargument-method"></a><span data-ttu-id="8b58e-103">ICorDebugILFrame::GetArgument 方法</span><span class="sxs-lookup"><span data-stu-id="8b58e-103">ICorDebugILFrame::GetArgument Method</span></span>

<span data-ttu-id="8b58e-104">获取此 Microsoft 中间语言 (MSIL) 堆栈帧中的指定参数的值。</span><span class="sxs-lookup"><span data-stu-id="8b58e-104">Gets the value of the specified argument in this Microsoft intermediate language (MSIL) stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b58e-105">语法</span><span class="sxs-lookup"><span data-stu-id="8b58e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetArgument (  
    [in] DWORD                  dwIndex,  
    [out] ICorDebugValue        **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8b58e-106">参数</span><span class="sxs-lookup"><span data-stu-id="8b58e-106">Parameters</span></span>  

 `dwIndex`  
 <span data-ttu-id="8b58e-107">中此 MSIL 堆栈帧中的参数的索引。</span><span class="sxs-lookup"><span data-stu-id="8b58e-107">[in] The index of the argument in this MSIL stack frame.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="8b58e-108">[out] 一个指向 ICorDebugValue 对象地址的指针，该对象表示检索到的值。</span><span class="sxs-lookup"><span data-stu-id="8b58e-108">[out] A pointer to the address of an ICorDebugValue object that represents the retrieved value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8b58e-109">备注</span><span class="sxs-lookup"><span data-stu-id="8b58e-109">Remarks</span></span>  

 <span data-ttu-id="8b58e-110">`GetArgument`方法既可以在 MSIL 堆栈帧中使用，也可以在实时 (JIT) 编译的框架中使用。</span><span class="sxs-lookup"><span data-stu-id="8b58e-110">The `GetArgument` method can be used either in an MSIL stack frame or in a just-in-time (JIT) compiled frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8b58e-111">要求</span><span class="sxs-lookup"><span data-stu-id="8b58e-111">Requirements</span></span>  

 <span data-ttu-id="8b58e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8b58e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8b58e-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8b58e-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8b58e-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8b58e-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8b58e-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8b58e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
