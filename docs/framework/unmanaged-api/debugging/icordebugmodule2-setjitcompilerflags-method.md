---
description: 了解详细信息： ICorDebugModule2：： SetJITCompilerFlags 方法
title: ICorDebugModule2::SetJITCompilerFlags 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule2.SetJITCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2::SetJITCompilerFlags
helpviewer_keywords:
- ICorDebugModule2::SetJITCompilerFlags method [.NET Framework debugging]
- SetJITCompilerFlags method [.NET Framework debugging]
ms.assetid: ea574c84-c622-4589-9a14-b55771af5e06
topic_type:
- apiref
ms.openlocfilehash: 72139c2fefc0eab7e76e38d07558e4386b47bc34
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801054"
---
# <a name="icordebugmodule2setjitcompilerflags-method"></a><span data-ttu-id="badf3-103">ICorDebugModule2::SetJITCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="badf3-103">ICorDebugModule2::SetJITCompilerFlags Method</span></span>

<span data-ttu-id="badf3-104">设置用于控制此 ICorDebugModule2 的实时 (JIT) 编译的标志。</span><span class="sxs-lookup"><span data-stu-id="badf3-104">Sets the flags that control the just-in-time (JIT) compilation of this ICorDebugModule2.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="badf3-105">语法</span><span class="sxs-lookup"><span data-stu-id="badf3-105">Syntax</span></span>  
  
```cpp  
HRESULT SetJITCompilerFlags (  
    [in] DWORD dwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="badf3-106">参数</span><span class="sxs-lookup"><span data-stu-id="badf3-106">Parameters</span></span>  

 `dwFlags`  
 <span data-ttu-id="badf3-107">中 [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) 枚举值的按位组合。</span><span class="sxs-lookup"><span data-stu-id="badf3-107">[in] A bitwise combination of the [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) enumeration values.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="badf3-108">备注</span><span class="sxs-lookup"><span data-stu-id="badf3-108">Remarks</span></span>  

 <span data-ttu-id="badf3-109">如果 `dwFlags` 值无效，则该 `SetJITCompilerFlags` 方法将失败。</span><span class="sxs-lookup"><span data-stu-id="badf3-109">If the `dwFlags` value is invalid, the `SetJITCompilerFlags` method will fail.</span></span>  
  
 <span data-ttu-id="badf3-110">只能在 `SetJITCompilerFlags` 此模块的 [ICorDebugManagedCallback：： LoadModule](icordebugmanagedcallback-loadmodule-method.md) 回调中调用方法。</span><span class="sxs-lookup"><span data-stu-id="badf3-110">The `SetJITCompilerFlags` method can be called only from within the [ICorDebugManagedCallback::LoadModule](icordebugmanagedcallback-loadmodule-method.md) callback for this module.</span></span> <span data-ttu-id="badf3-111">在提供回调后，尝试调用它 `ICorDebugManagedCallback::LoadModule` 将会失败。</span><span class="sxs-lookup"><span data-stu-id="badf3-111">Attempts to call it after the `ICorDebugManagedCallback::LoadModule` callback has been delivered will fail.</span></span>  
  
 <span data-ttu-id="badf3-112">64位或 Win9x 平台不支持 "编辑并继续"。</span><span class="sxs-lookup"><span data-stu-id="badf3-112">Edit and Continue is not supported on 64-bit or Win9x platforms.</span></span> <span data-ttu-id="badf3-113">因此，如果在这 `SetJITCompilerFlags` 两个平台中的任何一个上调用方法，并且在中设置了 CORDEBUG_JIT_ENABLE_ENC 标志 `dwFlags` ，则 `SetJITCompilerFlags` 特定于 "编辑并继续" 的方法和所有方法（例如 [ICorDebugModule2：： ApplyChanges](icordebugmodule2-applychanges-method.md)）将会失败。</span><span class="sxs-lookup"><span data-stu-id="badf3-113">Therefore, if you call the `SetJITCompilerFlags` method on either of these two platforms with the CORDEBUG_JIT_ENABLE_ENC flag set in `dwFlags`, the `SetJITCompilerFlags` method and all methods specific to Edit and Continue, such as [ICorDebugModule2::ApplyChanges](icordebugmodule2-applychanges-method.md), will fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="badf3-114">要求</span><span class="sxs-lookup"><span data-stu-id="badf3-114">Requirements</span></span>  

 <span data-ttu-id="badf3-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="badf3-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="badf3-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="badf3-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="badf3-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="badf3-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="badf3-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="badf3-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
