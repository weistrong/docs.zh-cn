---
description: 了解详细信息： ICorDebugModule3：： CreateReaderForInMemorySymbols 方法
title: ICorDebugModule3::CreateReaderForInMemorySymbols 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule3.CreateReaderForInMemorySymbols
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule3::CreateReaderForInMemorySymbols
helpviewer_keywords:
- CreateReaderForInMemorySymbols method, ICorDebugModule3 interface [.NET Framework debugging]
- ICorDebugModule3::CreateReaderForInMemorySymbols method [.NET Framework debugging]
ms.assetid: af317171-d66d-4114-89eb-063554c74940
topic_type:
- apiref
ms.openlocfilehash: af037cc891e83f53fd94bad290f40286ed665e6f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790771"
---
# <a name="icordebugmodule3createreaderforinmemorysymbols-method"></a><span data-ttu-id="360c5-103">ICorDebugModule3::CreateReaderForInMemorySymbols 方法</span><span class="sxs-lookup"><span data-stu-id="360c5-103">ICorDebugModule3::CreateReaderForInMemorySymbols Method</span></span>

<span data-ttu-id="360c5-104">为动态模块创建调试符号读取器。</span><span class="sxs-lookup"><span data-stu-id="360c5-104">Creates a debug symbol reader for a dynamic module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="360c5-105">语法</span><span class="sxs-lookup"><span data-stu-id="360c5-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateReaderForInMemorySymbols (  
      [in] REFIID riid,  
      [out][iid_is(riid)] void **    ppObj  
```  
  
## <a name="parameters"></a><span data-ttu-id="360c5-106">参数</span><span class="sxs-lookup"><span data-stu-id="360c5-106">Parameters</span></span>  

 <span data-ttu-id="360c5-107">riid</span><span class="sxs-lookup"><span data-stu-id="360c5-107">riid</span></span>  
 <span data-ttu-id="360c5-108">中要返回的 COM 接口的 IID。</span><span class="sxs-lookup"><span data-stu-id="360c5-108">[in] The IID of the COM interface to return.</span></span> <span data-ttu-id="360c5-109">通常，这是一个 [ISymUnmanagedReader 接口](../diagnostics/isymunmanagedreader-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="360c5-109">Typically, this is an [ISymUnmanagedReader Interface](../diagnostics/isymunmanagedreader-interface.md).</span></span>  
  
 <span data-ttu-id="360c5-110">ppObj</span><span class="sxs-lookup"><span data-stu-id="360c5-110">ppObj</span></span>  
 <span data-ttu-id="360c5-111">弄指向返回接口的指针的指针。</span><span class="sxs-lookup"><span data-stu-id="360c5-111">[out] Pointer to a pointer to the returned interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="360c5-112">返回值</span><span class="sxs-lookup"><span data-stu-id="360c5-112">Return Value</span></span>  

 <span data-ttu-id="360c5-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="360c5-113">S_OK</span></span>  
 <span data-ttu-id="360c5-114">已成功创建读取器。</span><span class="sxs-lookup"><span data-stu-id="360c5-114">Successfully created the reader.</span></span>  
  
 <span data-ttu-id="360c5-115">CORDBG_E_MODULE_LOADED_FROM_DISK</span><span class="sxs-lookup"><span data-stu-id="360c5-115">CORDBG_E_MODULE_LOADED_FROM_DISK</span></span>  
 <span data-ttu-id="360c5-116">该模块不是内存中或动态模块。</span><span class="sxs-lookup"><span data-stu-id="360c5-116">The module is not an in-memory or dynamic module.</span></span>  
  
 <span data-ttu-id="360c5-117">CORDBG_E_SYMBOLS_NOT_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="360c5-117">CORDBG_E_SYMBOLS_NOT_AVAILABLE</span></span>  
 <span data-ttu-id="360c5-118">符号尚未由应用程序提供或尚未提供。</span><span class="sxs-lookup"><span data-stu-id="360c5-118">Symbols have not been supplied by the application or are not yet available.</span></span>  
  
 <span data-ttu-id="360c5-119">E_FAIL（或其他 E_ 返回代码）</span><span class="sxs-lookup"><span data-stu-id="360c5-119">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="360c5-120">无法创建读取器。</span><span class="sxs-lookup"><span data-stu-id="360c5-120">Unable to create the reader.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="360c5-121">备注</span><span class="sxs-lookup"><span data-stu-id="360c5-121">Remarks</span></span>  

 <span data-ttu-id="360c5-122">此方法还可用于为内存中 (非动态) 模块创建符号读取器对象，但仅在符号首次可用之后 ([UpdateModuleSymbols 方法](icordebugmanagedcallback-updatemodulesymbols-method.md) 回调) 指示。</span><span class="sxs-lookup"><span data-stu-id="360c5-122">This method can also be used to create a symbol reader object for in-memory (non-dynamic) modules, but only after the symbols are first available (indicated by the [UpdateModuleSymbols Method](icordebugmanagedcallback-updatemodulesymbols-method.md) callback).</span></span>  
  
 <span data-ttu-id="360c5-123">此方法会在每次调用时返回一个新的读取器实例 (如 [CComPtrBase：： CoCreateInstance](/cpp/atl/reference/ccomptrbase-class#cocreateinstance)) 。</span><span class="sxs-lookup"><span data-stu-id="360c5-123">This method returns a new reader instance every time it is called (like [CComPtrBase::CoCreateInstance](/cpp/atl/reference/ccomptrbase-class#cocreateinstance)).</span></span> <span data-ttu-id="360c5-124">因此，只有当基础数据可能已更改时，调试器才应缓存结果，并请求新实例 (也就是说，当) 接收到 [LoadClass 方法](icordebugmanagedcallback-loadclass-method.md) 回调时。</span><span class="sxs-lookup"><span data-stu-id="360c5-124">Therefore, the debugger should cache the result and request a new instance only when the underlying data may have changed (that is, when a [LoadClass Method](icordebugmanagedcallback-loadclass-method.md) callback is received).</span></span>  
  
 <span data-ttu-id="360c5-125">在加载第一个类型之前，动态模块没有可用的任何符号 (如 [LoadClass 方法](icordebugmanagedcallback-loadclass-method.md) 回调) 所示。</span><span class="sxs-lookup"><span data-stu-id="360c5-125">Dynamic modules do not have any symbols available until the first type has been loaded (as indicated by the [LoadClass Method](icordebugmanagedcallback-loadclass-method.md) callback).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="360c5-126">要求</span><span class="sxs-lookup"><span data-stu-id="360c5-126">Requirements</span></span>  

 <span data-ttu-id="360c5-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="360c5-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="360c5-128">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="360c5-128">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="360c5-129">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="360c5-129">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="360c5-130">**.NET Framework 版本：** 4.5、4、3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="360c5-130">**.NET Framework Versions:** 4.5, 4, 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="360c5-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="360c5-131">See also</span></span>

- [<span data-ttu-id="360c5-132">ICorDebugRemoteTarget 接口</span><span class="sxs-lookup"><span data-stu-id="360c5-132">ICorDebugRemoteTarget Interface</span></span>](icordebugremotetarget-interface.md)
- [<span data-ttu-id="360c5-133">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="360c5-133">ICorDebug Interface</span></span>](icordebug-interface.md)

- [<span data-ttu-id="360c5-134">调试接口</span><span class="sxs-lookup"><span data-stu-id="360c5-134">Debugging Interfaces</span></span>](debugging-interfaces.md)
