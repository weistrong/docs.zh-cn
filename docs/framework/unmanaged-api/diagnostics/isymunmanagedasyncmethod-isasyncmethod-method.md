---
description: 了解详细信息： ISymUnmanagedAsyncMethod：： IsAsyncMethod 方法
title: ISymUnmanagedAsyncMethod::IsAsyncMethod 方法
ms.date: 03/30/2017
ms.assetid: 670a7653-dac6-4171-98ee-d669e3adf4b2
ms.openlocfilehash: 4b151f5367bac5fd92cc8237492cad6dacfb8e88
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790251"
---
# <a name="isymunmanagedasyncmethodisasyncmethod-method"></a><span data-ttu-id="30151-103">ISymUnmanagedAsyncMethod::IsAsyncMethod 方法</span><span class="sxs-lookup"><span data-stu-id="30151-103">ISymUnmanagedAsyncMethod::IsAsyncMethod Method</span></span>

<span data-ttu-id="30151-104">检查方法是否有异步信息。</span><span class="sxs-lookup"><span data-stu-id="30151-104">Checks if the method has async information or not.</span></span>  
  
 <span data-ttu-id="30151-105">如果此方法返回，则 `FALSE` 调用此接口中的任何其他方法无效。</span><span class="sxs-lookup"><span data-stu-id="30151-105">If this method returns `FALSE` then it is invalid to call any other methods in this interface.</span></span> <span data-ttu-id="30151-106">`E_UNEXPECTED`在这种情况下，它们都将返回。</span><span class="sxs-lookup"><span data-stu-id="30151-106">They will all return `E_UNEXPECTED` in this case.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30151-107">语法</span><span class="sxs-lookup"><span data-stu-id="30151-107">Syntax</span></span>  
  
```idl  
HRESULT IsAsyncMethod(    [out, retval] BOOL* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="30151-108">参数</span><span class="sxs-lookup"><span data-stu-id="30151-108">Parameters</span></span>  
  
|<span data-ttu-id="30151-109">参数</span><span class="sxs-lookup"><span data-stu-id="30151-109">Parameter</span></span>|<span data-ttu-id="30151-110">说明</span><span class="sxs-lookup"><span data-stu-id="30151-110">Description</span></span>|  
|---------------|-----------------|  
|`pRetVal`||  
  
## <a name="return-value"></a><span data-ttu-id="30151-111">返回值</span><span class="sxs-lookup"><span data-stu-id="30151-111">Return Value</span></span>  

 <span data-ttu-id="30151-112">返回 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="30151-112">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="30151-113">要求</span><span class="sxs-lookup"><span data-stu-id="30151-113">Requirements</span></span>  

 <span data-ttu-id="30151-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="30151-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30151-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="30151-115">See also</span></span>

- [<span data-ttu-id="30151-116">ISymUnmanagedAsyncMethod 接口</span><span class="sxs-lookup"><span data-stu-id="30151-116">ISymUnmanagedAsyncMethod Interface</span></span>](isymunmanagedasyncmethod-interface.md)
