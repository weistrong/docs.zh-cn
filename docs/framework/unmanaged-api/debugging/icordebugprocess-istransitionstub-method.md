---
description: 了解详细信息： ICorDebugProcess：： IsTransitionStub 方法
title: ICorDebugProcess::IsTransitionStub 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.IsTransitionStub
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::IsTransitionStub
helpviewer_keywords:
- ICorDebugProcess::IsTransitionStub method [.NET Framework debugging]
- IsTransitionStub method [.NET Framework debugging]
ms.assetid: f7653317-7e48-4163-be03-f50f1a4b0f70
topic_type:
- apiref
ms.openlocfilehash: 0da8527538c2573b1ec0d26f8711644fe8fcca2a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781995"
---
# <a name="icordebugprocessistransitionstub-method"></a><span data-ttu-id="4fc6b-103">ICorDebugProcess::IsTransitionStub 方法</span><span class="sxs-lookup"><span data-stu-id="4fc6b-103">ICorDebugProcess::IsTransitionStub Method</span></span>

<span data-ttu-id="4fc6b-104">获取一个值，该值指示地址是否在将导致转换到托管代码的存根内。</span><span class="sxs-lookup"><span data-stu-id="4fc6b-104">Gets a value that indicates whether an address is inside a stub that will cause a transition to managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4fc6b-105">语法</span><span class="sxs-lookup"><span data-stu-id="4fc6b-105">Syntax</span></span>  
  
```cpp  
HRESULT IsTransitionStub(  
    [in]  CORDB_ADDRESS address,  
    [out] BOOL *pbTransitionStub);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4fc6b-106">参数</span><span class="sxs-lookup"><span data-stu-id="4fc6b-106">Parameters</span></span>  

 `address`  
 <span data-ttu-id="4fc6b-107">中一个 `CORDB_ADDRESS` 值，该值指定相关的地址。</span><span class="sxs-lookup"><span data-stu-id="4fc6b-107">[in] A `CORDB_ADDRESS` value that specifies the address in question.</span></span>  
  
 `pbTransitionStub`  
 <span data-ttu-id="4fc6b-108">弄指向布尔值的指针， `true` 如果指定的地址在将导致转换到托管代码的存根内，则为; 否则 `pbTransitionStub` 为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="4fc6b-108">[out] A pointer to a Boolean value that is `true` if the specified address is inside a stub that will cause a transition to managed code; otherwise \*`pbTransitionStub` is `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4fc6b-109">备注</span><span class="sxs-lookup"><span data-stu-id="4fc6b-109">Remarks</span></span>  

 <span data-ttu-id="4fc6b-110">`IsTransitionStub`非托管的单步执行代码可以使用方法来确定何时将单步执行控件返回给托管分档器。</span><span class="sxs-lookup"><span data-stu-id="4fc6b-110">The `IsTransitionStub` method can be used by unmanaged stepping code to decide when to return stepping control to the managed stepper.</span></span>  
  
 <span data-ttu-id="4fc6b-111">还可以通过查看可移植可执行文件 (PE) 文件中的信息来标识转换存根。</span><span class="sxs-lookup"><span data-stu-id="4fc6b-111">You can also identity transition stubs by looking at information in the portable executable (PE) file.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4fc6b-112">要求</span><span class="sxs-lookup"><span data-stu-id="4fc6b-112">Requirements</span></span>  

 <span data-ttu-id="4fc6b-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4fc6b-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4fc6b-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4fc6b-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4fc6b-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4fc6b-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4fc6b-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4fc6b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
