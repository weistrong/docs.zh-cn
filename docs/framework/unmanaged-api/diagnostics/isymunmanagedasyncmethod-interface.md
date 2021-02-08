---
description: 了解详细信息： ISymUnmanagedAsyncMethod 接口
title: ISymUnmanagedAsyncMethod 接口
ms.date: 03/30/2017
ms.assetid: f2de5224-fd91-45de-9e58-bc600c6d22f1
ms.openlocfilehash: cb3120464224137dfdcff4f13ca4aee82ef4d89e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790264"
---
# <a name="isymunmanagedasyncmethod-interface"></a><span data-ttu-id="e2503-103">ISymUnmanagedAsyncMethod 接口</span><span class="sxs-lookup"><span data-stu-id="e2503-103">ISymUnmanagedAsyncMethod Interface</span></span>

<span data-ttu-id="e2503-104">此接口是 [ISymUnmanagedAsyncMethodPropertiesWriter 接口](isymunmanagedasyncmethodpropertieswriter-interface.md)的读取补充。</span><span class="sxs-lookup"><span data-stu-id="e2503-104">This interface is the reading complement to [ISymUnmanagedAsyncMethodPropertiesWriter Interface](isymunmanagedasyncmethodpropertieswriter-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2503-105">语法</span><span class="sxs-lookup"><span data-stu-id="e2503-105">Syntax</span></span>  
  
```idl  
[object,uuid(B20D55B3-532E-4906-87E7-25BD5734ABD2),pointer_default(unique)]interface ISymUnmanagedAsyncMethod : IUnknown  
```  
  
## <a name="methods"></a><span data-ttu-id="e2503-106">方法</span><span class="sxs-lookup"><span data-stu-id="e2503-106">Methods</span></span>  

 <span data-ttu-id="e2503-107">此接口包含下列方法：</span><span class="sxs-lookup"><span data-stu-id="e2503-107">This interface contains the following methods:</span></span>  
  
|<span data-ttu-id="e2503-108">方法</span><span class="sxs-lookup"><span data-stu-id="e2503-108">Method</span></span>|<span data-ttu-id="e2503-109">说明</span><span class="sxs-lookup"><span data-stu-id="e2503-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e2503-110">GetAsyncStepInfo 方法</span><span class="sxs-lookup"><span data-stu-id="e2503-110">GetAsyncStepInfo Method</span></span>](isymunmanagedasyncmethod-getasyncstepinfo-method.md)|<span data-ttu-id="e2503-111">请参阅 [DefineAsyncStepInfo 方法](isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md)。</span><span class="sxs-lookup"><span data-stu-id="e2503-111">See [DefineAsyncStepInfo Method](isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>|  
|[<span data-ttu-id="e2503-112">GetAsyncStepInfoCount 方法</span><span class="sxs-lookup"><span data-stu-id="e2503-112">GetAsyncStepInfoCount Method</span></span>](isymunmanagedasyncmethod-getasyncstepinfocount-method.md)|<span data-ttu-id="e2503-113">请参阅 [DefineAsyncStepInfo 方法](isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md)。</span><span class="sxs-lookup"><span data-stu-id="e2503-113">See [DefineAsyncStepInfo Method](isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>|  
|[<span data-ttu-id="e2503-114">GetCatchHandlerILOffset 方法</span><span class="sxs-lookup"><span data-stu-id="e2503-114">GetCatchHandlerILOffset Method</span></span>](isymunmanagedasyncmethod-getcatchhandleriloffset-method.md)|<span data-ttu-id="e2503-115">请参阅 [DefineCatchHandlerILOffset 方法](isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md)。</span><span class="sxs-lookup"><span data-stu-id="e2503-115">See [DefineCatchHandlerILOffset Method](isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md).</span></span>|  
|[<span data-ttu-id="e2503-116">GetKickoffMethod 方法</span><span class="sxs-lookup"><span data-stu-id="e2503-116">GetKickoffMethod Method</span></span>](isymunmanagedasyncmethod-getkickoffmethod-method.md)|<span data-ttu-id="e2503-117">请参阅 [DefineKickoffMethod 方法](isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md)。</span><span class="sxs-lookup"><span data-stu-id="e2503-117">See [DefineKickoffMethod Method](isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span></span>|  
|[<span data-ttu-id="e2503-118">HasCatchHandlerILOffset 方法</span><span class="sxs-lookup"><span data-stu-id="e2503-118">HasCatchHandlerILOffset Method</span></span>](isymunmanagedasyncmethod-hascatchhandleriloffset-method.md)|<span data-ttu-id="e2503-119">请参阅 [DefineCatchHandlerILOffset 方法](isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md)。</span><span class="sxs-lookup"><span data-stu-id="e2503-119">See [DefineCatchHandlerILOffset Method](isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md).</span></span>|  
|[<span data-ttu-id="e2503-120">IsAsyncMethod 方法</span><span class="sxs-lookup"><span data-stu-id="e2503-120">IsAsyncMethod Method</span></span>](isymunmanagedasyncmethod-isasyncmethod-method.md)|<span data-ttu-id="e2503-121">检查方法是否有异步信息。</span><span class="sxs-lookup"><span data-stu-id="e2503-121">Checks if the method has async information or not.</span></span><br /><br /> <span data-ttu-id="e2503-122">如果此方法返回，则 `FALSE` 调用此接口中的任何其他方法无效。</span><span class="sxs-lookup"><span data-stu-id="e2503-122">If this method returns `FALSE` then it is invalid to call any other methods in this interface.</span></span> <span data-ttu-id="e2503-123">`E_UNEXPECTED`在这种情况下，它们都将返回。</span><span class="sxs-lookup"><span data-stu-id="e2503-123">They will all return `E_UNEXPECTED` in this case.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e2503-124">要求</span><span class="sxs-lookup"><span data-stu-id="e2503-124">Requirements</span></span>  

 <span data-ttu-id="e2503-125">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="e2503-125">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2503-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="e2503-126">See also</span></span>

- [<span data-ttu-id="e2503-127">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="e2503-127">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
