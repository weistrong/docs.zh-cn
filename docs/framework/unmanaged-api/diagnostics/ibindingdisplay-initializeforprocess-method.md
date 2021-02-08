---
description: 了解详细信息： IBindingDisplay：： InitializeForProcess 方法
title: IBindingDisplay::InitializeForProcess 方法
ms.date: 03/30/2017
api_name:
- IBindingDisplay.InitializeForProcess
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- IBindingDisplay::InitializeForProcess
helpviewer_keywords:
- IBindingDisplay::InitializeForProcess method [.NET Framework debugging]
- InitializeForProcess method [.NET Framework debugging]
ms.assetid: 59417acb-4e59-46ad-acfe-d827e6ab6078
topic_type:
- apiref
ms.openlocfilehash: cf7f0f4d057659089bd7da173e5fac98a7c00dad
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800404"
---
# <a name="ibindingdisplayinitializeforprocess-method"></a><span data-ttu-id="5a63c-103">IBindingDisplay::InitializeForProcess 方法</span><span class="sxs-lookup"><span data-stu-id="5a63c-103">IBindingDisplay::InitializeForProcess Method</span></span>

<span data-ttu-id="5a63c-104">初始化 [IBindingDisplay](ibindingdisplay-interface.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="5a63c-104">Initializes the [IBindingDisplay](ibindingdisplay-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5a63c-105">语法</span><span class="sxs-lookup"><span data-stu-id="5a63c-105">Syntax</span></span>  
  
```cpp  
HRESULT InitializeForProcess (  
    [in] ULONG32   pid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5a63c-106">参数</span><span class="sxs-lookup"><span data-stu-id="5a63c-106">Parameters</span></span>  

 `pid`  
 <span data-ttu-id="5a63c-107">中进程标识符。</span><span class="sxs-lookup"><span data-stu-id="5a63c-107">[in] The process identifier.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5a63c-108">备注</span><span class="sxs-lookup"><span data-stu-id="5a63c-108">Remarks</span></span>  

 <span data-ttu-id="5a63c-109">调试器 `InitializeForProcess` 在创建时调用方法以初始化绑定显示。</span><span class="sxs-lookup"><span data-stu-id="5a63c-109">The debugger calls the `InitializeForProcess` method at creation time to initialize the binding display.</span></span> <span data-ttu-id="5a63c-110">`InitializeForProcess` 调用任何其他方法之前，必须在创建时调用 `IBindingDisplay` 。</span><span class="sxs-lookup"><span data-stu-id="5a63c-110">`InitializeForProcess` must be called at creation time before any other method on `IBindingDisplay` is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5a63c-111">要求</span><span class="sxs-lookup"><span data-stu-id="5a63c-111">Requirements</span></span>  

 <span data-ttu-id="5a63c-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5a63c-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5a63c-113">**标头：** BindingDisplay</span><span class="sxs-lookup"><span data-stu-id="5a63c-113">**Header:** BindingDisplay.h</span></span>  
  
 <span data-ttu-id="5a63c-114">**库：** BindingDisplay .idl</span><span class="sxs-lookup"><span data-stu-id="5a63c-114">**Library:** BindingDisplay.idl</span></span>  
  
 <span data-ttu-id="5a63c-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5a63c-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5a63c-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="5a63c-116">See also</span></span>

- [<span data-ttu-id="5a63c-117">IBindingDisplay 接口</span><span class="sxs-lookup"><span data-stu-id="5a63c-117">IBindingDisplay Interface</span></span>](ibindingdisplay-interface.md)
