---
description: 了解详细信息： ICLRDebugging 接口
title: ICLRDebugging 接口
ms.date: 03/30/2017
api_name:
- ICLRDebugging
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDebugging
helpviewer_keywords:
- ICLRDebugging interface [.NET Framework debugging]
ms.assetid: 429d8fce-b1b1-49d7-895c-28c1c1aa2dbd
topic_type:
- apiref
ms.openlocfilehash: 647b6f7634ef3b9f6ec6080aaff19476c027952a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723330"
---
# <a name="iclrdebugging-interface"></a><span data-ttu-id="8ebb6-103">ICLRDebugging 接口</span><span class="sxs-lookup"><span data-stu-id="8ebb6-103">ICLRDebugging Interface</span></span>

<span data-ttu-id="8ebb6-104">提供一些方法，用于处理模块的加载和卸载以进行调试。</span><span class="sxs-lookup"><span data-stu-id="8ebb6-104">Provides methods that handle loading and unloading modules for debugging.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8ebb6-105">方法</span><span class="sxs-lookup"><span data-stu-id="8ebb6-105">Methods</span></span>  
  
|<span data-ttu-id="8ebb6-106">方法</span><span class="sxs-lookup"><span data-stu-id="8ebb6-106">Method</span></span>|<span data-ttu-id="8ebb6-107">说明</span><span class="sxs-lookup"><span data-stu-id="8ebb6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8ebb6-108">OpenVirtualProcess 方法</span><span class="sxs-lookup"><span data-stu-id="8ebb6-108">OpenVirtualProcess Method</span></span>](iclrdebugging-openvirtualprocess-method.md)|<span data-ttu-id="8ebb6-109">获取 "ICorDebugProcess" 接口，该接口对应于进程中加载的公共语言运行时 (CLR) 模块。</span><span class="sxs-lookup"><span data-stu-id="8ebb6-109">Gets the "ICorDebugProcess" interface that corresponds to a common language runtime (CLR) module loaded in the process.</span></span>|  
|[<span data-ttu-id="8ebb6-110">CanUnloadNow 方法</span><span class="sxs-lookup"><span data-stu-id="8ebb6-110">CanUnloadNow Method</span></span>](iclrdebugging-canunloadnow-method.md)|<span data-ttu-id="8ebb6-111">确定 [ICLRDebuggingLibraryProvider](iclrdebugginglibraryprovider-interface.md) 接口提供的库是否仍在使用中或是否可以卸载。</span><span class="sxs-lookup"><span data-stu-id="8ebb6-111">Determines whether a library that was provided by an [ICLRDebuggingLibraryProvider](iclrdebugginglibraryprovider-interface.md) interface is still in use or can be unloaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8ebb6-112">备注</span><span class="sxs-lookup"><span data-stu-id="8ebb6-112">Remarks</span></span>  

 <span data-ttu-id="8ebb6-113">可以 `ICLRDebugging` 使用 [CLRCreateInstance](../hosting/clrcreateinstance-function.md) 函数获取接口的实例。</span><span class="sxs-lookup"><span data-stu-id="8ebb6-113">You can obtain an instance of the `ICLRDebugging` interface by using the [CLRCreateInstance](../hosting/clrcreateinstance-function.md) function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ebb6-114">要求</span><span class="sxs-lookup"><span data-stu-id="8ebb6-114">Requirements</span></span>  

 <span data-ttu-id="8ebb6-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8ebb6-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ebb6-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8ebb6-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8ebb6-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8ebb6-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8ebb6-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ebb6-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ebb6-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="8ebb6-119">See also</span></span>

- [<span data-ttu-id="8ebb6-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="8ebb6-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="8ebb6-121">调试</span><span class="sxs-lookup"><span data-stu-id="8ebb6-121">Debugging</span></span>](index.md)
