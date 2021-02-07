---
description: 了解详细信息： ICorDebugProcess6：： MarkDebuggerAttached 方法
title: ICorDebugProcess6::MarkDebuggerAttached 方法
ms.date: 03/30/2017
ms.assetid: bf94f090-5265-4112-8e57-5b4e20e070d0
ms.openlocfilehash: adbe16049cea73ca5e797f7758a17902b33645c5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691375"
---
# <a name="icordebugprocess6markdebuggerattached-method"></a><span data-ttu-id="7245e-103">ICorDebugProcess6::MarkDebuggerAttached 方法</span><span class="sxs-lookup"><span data-stu-id="7245e-103">ICorDebugProcess6::MarkDebuggerAttached Method</span></span>

<span data-ttu-id="7245e-104">更改调试对象的内部状态，以便 .NET Framework 类库中的 <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> 方法返回 `true`。</span><span class="sxs-lookup"><span data-stu-id="7245e-104">Changes the internal state of the debugee so that the <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> method in the .NET Framework Class Library returns `true`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7245e-105">语法</span><span class="sxs-lookup"><span data-stu-id="7245e-105">Syntax</span></span>  
  
```cpp  
HRESULT MarkDebuggerAttached(  
    BOOL fIsAttached  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7245e-106">参数</span><span class="sxs-lookup"><span data-stu-id="7245e-106">Parameters</span></span>  

 `fIsAttached`  
 <span data-ttu-id="7245e-107">如果 `true` 方法指出已连接调试程序，则为<xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType>；否则即为 `false`。</span><span class="sxs-lookup"><span data-stu-id="7245e-107">`true` if the <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> method should indicate that a debugger is attached; `false` otherwise.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7245e-108">返回值</span><span class="sxs-lookup"><span data-stu-id="7245e-108">Return Value</span></span>  

 <span data-ttu-id="7245e-109">该方法可以返回下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="7245e-109">The method can return the values listed in the following table.</span></span>  
  
|<span data-ttu-id="7245e-110">返回值</span><span class="sxs-lookup"><span data-stu-id="7245e-110">Return value</span></span>|<span data-ttu-id="7245e-111">说明</span><span class="sxs-lookup"><span data-stu-id="7245e-111">Description</span></span>|  
|------------------|-----------------|  
|`S_OK`|<span data-ttu-id="7245e-112">调试对象已成功更新。</span><span class="sxs-lookup"><span data-stu-id="7245e-112">The debuggee was successfully updated.</span></span>|  
|`CORDBG_E_MODULE_NOT_LOADED`|<span data-ttu-id="7245e-113">程序集包含未加载的 <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> 方法或一些其他错误（例如元数据丢失），无法被识别。</span><span class="sxs-lookup"><span data-stu-id="7245e-113">The assembly that contains the <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> method is not loaded, or some other error, such as missing metadata, is preventing it from being recognized.</span></span><br /><br /> <span data-ttu-id="7245e-114">该错误很常见，没有危害。</span><span class="sxs-lookup"><span data-stu-id="7245e-114">This error is common and benign.</span></span> <span data-ttu-id="7245e-115">你应当在其他程序集加载时再次调用方法。</span><span class="sxs-lookup"><span data-stu-id="7245e-115">You should call the method again when additional assemblies load.</span></span>|  
|<span data-ttu-id="7245e-116">其他失败 `HRESULT` 值。</span><span class="sxs-lookup"><span data-stu-id="7245e-116">Other failing `HRESULT` values.</span></span>|<span data-ttu-id="7245e-117">其他值可能表示错误调试程序或编译器组件。</span><span class="sxs-lookup"><span data-stu-id="7245e-117">Other values likely indicate misbehaving debugger or compiler components.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7245e-118">备注</span><span class="sxs-lookup"><span data-stu-id="7245e-118">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7245e-119">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="7245e-119">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7245e-120">要求</span><span class="sxs-lookup"><span data-stu-id="7245e-120">Requirements</span></span>  

 <span data-ttu-id="7245e-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7245e-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7245e-122">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7245e-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7245e-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7245e-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7245e-124">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7245e-124">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7245e-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="7245e-125">See also</span></span>

- [<span data-ttu-id="7245e-126">“ICor调试进程6”接口</span><span class="sxs-lookup"><span data-stu-id="7245e-126">ICorDebugProcess6 Interface</span></span>](icordebugprocess6-interface.md)
- [<span data-ttu-id="7245e-127">调试接口</span><span class="sxs-lookup"><span data-stu-id="7245e-127">Debugging Interfaces</span></span>](debugging-interfaces.md)
