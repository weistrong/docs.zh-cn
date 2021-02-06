---
description: 了解详细信息： ICorDebugProcess2：： SetDesiredNGENCompilerFlags 方法
title: ICorDebugProcess2::SetDesiredNGENCompilerFlags 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2.SetDesiredNGENCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2::SetDesiredNGENCompilerFlags
helpviewer_keywords:
- ICorDebugProcess2::SetDesiredNGENCompilerFlags method [.NET Framework debugging]
- SetDesiredNGENCompilerFlags method [.NET Framework debugging]
ms.assetid: 98320175-7c5e-4dbb-8683-86fa82e2641f
topic_type:
- apiref
ms.openlocfilehash: 3a4749ad26e88d1a602876f28a52754323093fce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650075"
---
# <a name="icordebugprocess2setdesiredngencompilerflags-method"></a><span data-ttu-id="d9eea-103">ICorDebugProcess2::SetDesiredNGENCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="d9eea-103">ICorDebugProcess2::SetDesiredNGENCompilerFlags Method</span></span>

<span data-ttu-id="d9eea-104">设置必须嵌入到预编译的映像中的标志，使运行时能够将该图像加载到当前进程。</span><span class="sxs-lookup"><span data-stu-id="d9eea-104">Sets the flags that must be embedded in a precompiled image in order for the runtime to load that image into the current process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9eea-105">语法</span><span class="sxs-lookup"><span data-stu-id="d9eea-105">Syntax</span></span>  
  
```cpp  
HRESULT SetDesiredNGENCompilerFlags (  
    [in] DWORD    pdwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d9eea-106">参数</span><span class="sxs-lookup"><span data-stu-id="d9eea-106">Parameters</span></span>  

 `pdwFlags`  
 <span data-ttu-id="d9eea-107">中 [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) 枚举的一个值，该值指定用于选择正确预编译图像的编译器标志。</span><span class="sxs-lookup"><span data-stu-id="d9eea-107">[in] A value of the [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) enumeration that specifies the compiler flags used to select the correct pre-compiled image.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d9eea-108">备注</span><span class="sxs-lookup"><span data-stu-id="d9eea-108">Remarks</span></span>  

 <span data-ttu-id="d9eea-109">`SetDesiredNGENCompilerFlags`方法指定必须嵌入到预编译的映像中的标志，以使运行时将该图像加载到此进程中。</span><span class="sxs-lookup"><span data-stu-id="d9eea-109">The `SetDesiredNGENCompilerFlags` method specifies the flags that must be embedded in a precompiled image so that the runtime will load that image into this process.</span></span> <span data-ttu-id="d9eea-110">此方法设置的标志仅用于选择正确的预编译映像。</span><span class="sxs-lookup"><span data-stu-id="d9eea-110">The flags set by this method are used only to select the correct precompiled image.</span></span> <span data-ttu-id="d9eea-111">如果不存在这样的图像，则运行时将 (MSIL) 映像和实时 (JIT) 编译器加载 Microsoft 中间语言。</span><span class="sxs-lookup"><span data-stu-id="d9eea-111">If no such image exists, the runtime will load the Microsoft intermediate language (MSIL) image and the just-in-time (JIT) compiler instead.</span></span> <span data-ttu-id="d9eea-112">在这种情况下，调试器仍必须使用 [ICorDebugModule2：： SetJITCompilerFlags](icordebugmodule2-setjitcompilerflags-method.md) 方法根据需要为 JIT 编译设置标志。</span><span class="sxs-lookup"><span data-stu-id="d9eea-112">In that case, the debugger must still use the [ICorDebugModule2::SetJITCompilerFlags](icordebugmodule2-setjitcompilerflags-method.md) method to set the flags as desired for the JIT compilation.</span></span>  
  
 <span data-ttu-id="d9eea-113">如果加载了某个映像，但对于该映像必须进行一些 JIT 编译 (这种情况下，如果映像包含泛型) ，则该方法指定的编译器标志 `SetDesiredNGENCompilerFlags` 将应用于额外的 JIT 编译。</span><span class="sxs-lookup"><span data-stu-id="d9eea-113">If an image is loaded, but some JIT compiling must take place for that image (which will be the case if the image contains generics), the compiler flags specified by the `SetDesiredNGENCompilerFlags` method will apply to the extra JIT compilation.</span></span>  
  
 <span data-ttu-id="d9eea-114">`SetDesiredNGENCompilerFlags`必须在[ICorDebugManagedCallback：： CreateProcess](icordebugmanagedcallback-createprocess-method.md)回调过程中调用方法。</span><span class="sxs-lookup"><span data-stu-id="d9eea-114">The `SetDesiredNGENCompilerFlags` method must be called during the [ICorDebugManagedCallback::CreateProcess](icordebugmanagedcallback-createprocess-method.md) callback.</span></span> <span data-ttu-id="d9eea-115">此后尝试调用 `SetDesiredNGENCompilerFlags` 方法将失败。</span><span class="sxs-lookup"><span data-stu-id="d9eea-115">Attempts to call the `SetDesiredNGENCompilerFlags` method afterwards will fail.</span></span> <span data-ttu-id="d9eea-116">另外，尝试设置未在枚举中定义的 `CorDebugJITCompilerFlags` 或对给定进程不合法的标志的尝试将失败。</span><span class="sxs-lookup"><span data-stu-id="d9eea-116">Also, attempts to set flags that are either not defined in the `CorDebugJITCompilerFlags` enumeration or are not legal for the given process will fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9eea-117">要求</span><span class="sxs-lookup"><span data-stu-id="d9eea-117">Requirements</span></span>  

 <span data-ttu-id="d9eea-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d9eea-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9eea-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d9eea-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d9eea-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d9eea-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d9eea-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9eea-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9eea-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="d9eea-122">See also</span></span>

- [<span data-ttu-id="d9eea-123">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="d9eea-123">ICorDebug Interface</span></span>](icordebug-interface.md)
- [<span data-ttu-id="d9eea-124">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="d9eea-124">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
