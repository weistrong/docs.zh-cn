---
description: 了解详细信息： IBindingDisplay：： GetCurrentDisplay 方法
title: IBindingDisplay::GetCurrentDisplay 方法
ms.date: 03/30/2017
api_name:
- IBindingDisplay.GetCurrentDisplay
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- IBindingDisplay::GetCurrentDisplay
helpviewer_keywords:
- IBindingDisplay::GetCurrentDisplay method [.NET Framework debugging]
- GetCurrentDisplay method [.NET Framework debugging]
ms.assetid: d28eeea4-c4e0-40d4-91de-198d98cfa13c
topic_type:
- apiref
ms.openlocfilehash: 680a91c8025ac3247701c14c23f442da5e304ecb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800414"
---
# <a name="ibindingdisplaygetcurrentdisplay-method"></a><span data-ttu-id="d8c89-103">IBindingDisplay::GetCurrentDisplay 方法</span><span class="sxs-lookup"><span data-stu-id="d8c89-103">IBindingDisplay::GetCurrentDisplay Method</span></span>

<span data-ttu-id="d8c89-104">返回当前绑定显示信息。</span><span class="sxs-lookup"><span data-stu-id="d8c89-104">Returns the current binding display information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8c89-105">语法</span><span class="sxs-lookup"><span data-stu-id="d8c89-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentDisplay (  
    [out, retval] SAFEARRAY(struct BindingDisplayTabControl) *display  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d8c89-106">参数</span><span class="sxs-lookup"><span data-stu-id="d8c89-106">Parameters</span></span>  

 `display`  
 <span data-ttu-id="d8c89-107">[out，retval]指向包含绑定显示信息的 safearray 的指针。</span><span class="sxs-lookup"><span data-stu-id="d8c89-107">[out, retval] A pointer to a safearray containing the binding display information.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d8c89-108">备注</span><span class="sxs-lookup"><span data-stu-id="d8c89-108">Remarks</span></span>  

 <span data-ttu-id="d8c89-109">[IBindingDisplay：： InitializeForProcess](ibindingdisplay-initializeforprocess-method.md)方法之前必须已成功，并且调试器必须停止该程序。</span><span class="sxs-lookup"><span data-stu-id="d8c89-109">The [IBindingDisplay::InitializeForProcess](ibindingdisplay-initializeforprocess-method.md) method must have previously succeeded, and the program must be stopped by a debugger.</span></span>  
  
 <span data-ttu-id="d8c89-110">调用方必须使用 SafeArrayDestroy 释放返回的 `SAFEARRAY` 内存[](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy)。</span><span class="sxs-lookup"><span data-stu-id="d8c89-110">The caller must deallocate the returned `SAFEARRAY` memory by using [SafeArrayDestroy](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8c89-111">要求</span><span class="sxs-lookup"><span data-stu-id="d8c89-111">Requirements</span></span>  

 <span data-ttu-id="d8c89-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d8c89-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8c89-113">**标头：** BindingDisplay</span><span class="sxs-lookup"><span data-stu-id="d8c89-113">**Header:** BindingDisplay.h</span></span>  
  
 <span data-ttu-id="d8c89-114">**库：** BindingDisplay .idl</span><span class="sxs-lookup"><span data-stu-id="d8c89-114">**Library:** BindingDisplay.idl</span></span>  
  
 <span data-ttu-id="d8c89-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8c89-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8c89-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="d8c89-116">See also</span></span>

- [<span data-ttu-id="d8c89-117">IBindingDisplay 接口</span><span class="sxs-lookup"><span data-stu-id="d8c89-117">IBindingDisplay Interface</span></span>](ibindingdisplay-interface.md)
- [<span data-ttu-id="d8c89-118">InitializeForProcess 方法</span><span class="sxs-lookup"><span data-stu-id="d8c89-118">InitializeForProcess Method</span></span>](ibindingdisplay-initializeforprocess-method.md)
