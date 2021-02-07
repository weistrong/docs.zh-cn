---
description: 了解详细信息： ICLRDebugging：： CanUnloadNow 方法
title: ICLRDebugging::CanUnloadNow 方法
ms.date: 03/30/2017
api_name:
- ICLRDebugging.CanUnloadNow Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDebugging::CanUnloadNow
helpviewer_keywords:
- CanUnloadNow method [.NET Framework debugging]
- ICLRDebugging::CanUnloadNow method [.NET Framework debugging]
ms.assetid: 62e0630c-8cb7-45d2-b622-5a472abfd8cf
topic_type:
- apiref
ms.openlocfilehash: 537494fe862c58aa8a8768dd5ce2abc8ca94f87d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723369"
---
# <a name="iclrdebuggingcanunloadnow-method"></a><span data-ttu-id="26aea-103">ICLRDebugging::CanUnloadNow 方法</span><span class="sxs-lookup"><span data-stu-id="26aea-103">ICLRDebugging::CanUnloadNow Method</span></span>

<span data-ttu-id="26aea-104">确定 [ICLRDebuggingLibraryProvider](iclrdebugginglibraryprovider-interface.md) 接口提供的库是否仍在使用中或是否可以卸载。</span><span class="sxs-lookup"><span data-stu-id="26aea-104">Determines whether a library that was provided by an [ICLRDebuggingLibraryProvider](iclrdebugginglibraryprovider-interface.md) interface is still in use or can be unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26aea-105">语法</span><span class="sxs-lookup"><span data-stu-id="26aea-105">Syntax</span></span>  
  
```cpp  
HRESULT CanUnloadNow(HMODULE hModule);  
```  
  
## <a name="parameters"></a><span data-ttu-id="26aea-106">参数</span><span class="sxs-lookup"><span data-stu-id="26aea-106">Parameters</span></span>  

 `hmodule`  
 <span data-ttu-id="26aea-107">中目标进程中的模块的基址。</span><span class="sxs-lookup"><span data-stu-id="26aea-107">[in] The base address of a module in the target process.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="26aea-108">返回值</span><span class="sxs-lookup"><span data-stu-id="26aea-108">Return Value</span></span>  

 <span data-ttu-id="26aea-109">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="26aea-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="26aea-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="26aea-110">HRESULT</span></span>|<span data-ttu-id="26aea-111">说明</span><span class="sxs-lookup"><span data-stu-id="26aea-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="26aea-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="26aea-112">S_OK</span></span>|<span data-ttu-id="26aea-113">可卸载引用的模块 `hmodule` 。</span><span class="sxs-lookup"><span data-stu-id="26aea-113">The module that is referenced by `hmodule` can be unloaded.</span></span>|  
|<span data-ttu-id="26aea-114">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="26aea-114">S_FALSE</span></span>|<span data-ttu-id="26aea-115">引用的模块 `hmodule` 仍在使用中。</span><span class="sxs-lookup"><span data-stu-id="26aea-115">The module that is referenced by `hmodule` is still in use.</span></span>|  
|<span data-ttu-id="26aea-116">COR_E_NOT_CLR</span><span class="sxs-lookup"><span data-stu-id="26aea-116">COR_E_NOT_CLR</span></span>|<span data-ttu-id="26aea-117">指示的模块不是 CLR 模块。</span><span class="sxs-lookup"><span data-stu-id="26aea-117">The indicated module is not a CLR module.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="26aea-118">例外</span><span class="sxs-lookup"><span data-stu-id="26aea-118">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="26aea-119">备注</span><span class="sxs-lookup"><span data-stu-id="26aea-119">Remarks</span></span>  

 <span data-ttu-id="26aea-120">此方法检查是否 `ICorDebug*` 已释放接口的所有实例，并且当前在对 [ICLRDebugging：： OpenVirtualProcess](iclrdebugging-openvirtualprocess-method.md) 方法的调用中没有线程。</span><span class="sxs-lookup"><span data-stu-id="26aea-120">This method checks to see if all instances of `ICorDebug*` interfaces have been released and no thread is currently within a call to the [ICLRDebugging::OpenVirtualProcess](iclrdebugging-openvirtualprocess-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="26aea-121">要求</span><span class="sxs-lookup"><span data-stu-id="26aea-121">Requirements</span></span>  

 <span data-ttu-id="26aea-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="26aea-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="26aea-123">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="26aea-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="26aea-124">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="26aea-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="26aea-125">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="26aea-125">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26aea-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="26aea-126">See also</span></span>

- [<span data-ttu-id="26aea-127">调试接口</span><span class="sxs-lookup"><span data-stu-id="26aea-127">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="26aea-128">调试</span><span class="sxs-lookup"><span data-stu-id="26aea-128">Debugging</span></span>](index.md)
