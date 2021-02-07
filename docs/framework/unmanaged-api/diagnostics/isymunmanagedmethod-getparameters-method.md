---
description: 了解详细信息： ISymUnmanagedMethod：： GetParameters 方法
title: ISymUnmanagedMethod::GetParameters 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetParameters
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetParameters
helpviewer_keywords:
- ISymUnmanagedMethod::GetParameters method [.NET Framework debugging]
- GetParameters method [.NET Framework debugging]
ms.assetid: 3a8074f1-facc-4a3f-bb9b-d6574fc2fc74
topic_type:
- apiref
ms.openlocfilehash: c8860a4d42019aaacef01879b175fd45ea837f2b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721367"
---
# <a name="isymunmanagedmethodgetparameters-method"></a><span data-ttu-id="96c08-103">ISymUnmanagedMethod::GetParameters 方法</span><span class="sxs-lookup"><span data-stu-id="96c08-103">ISymUnmanagedMethod::GetParameters Method</span></span>

<span data-ttu-id="96c08-104">获取此方法的参数。</span><span class="sxs-lookup"><span data-stu-id="96c08-104">Gets the parameters for this method.</span></span> <span data-ttu-id="96c08-105">按参数在方法签名中的定义顺序返回参数。</span><span class="sxs-lookup"><span data-stu-id="96c08-105">The parameters are returned in the order in which they are defined within the method's signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96c08-106">语法</span><span class="sxs-lookup"><span data-stu-id="96c08-106">Syntax</span></span>  
  
```cpp  
HRESULT GetParameters(  
    [in]  ULONG32  cParams,  
    [out] ULONG32  *pcParams,  
    [out, size_is(cParams),  
        length_is(*pcParams)] ISymUnmanagedVariable*  params[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="96c08-107">参数</span><span class="sxs-lookup"><span data-stu-id="96c08-107">Parameters</span></span>  

 `cParams`  
 <span data-ttu-id="96c08-108">[in] `params` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="96c08-108">[in] The size of the `params` array.</span></span>  
  
 `pcParams`  
 <span data-ttu-id="96c08-109">中指向的指针 `ULONG32` ，该指针接收包含参数所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="96c08-109">[in] A pointer to a `ULONG32` that receives the size of the buffer that is required to contain the parameters.</span></span>  
  
 `params`  
 <span data-ttu-id="96c08-110">弄指向接收参数的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="96c08-110">[out] A pointer to the buffer that receives the parameters.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="96c08-111">返回值</span><span class="sxs-lookup"><span data-stu-id="96c08-111">Return Value</span></span>  

 <span data-ttu-id="96c08-112">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="96c08-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="96c08-113">要求</span><span class="sxs-lookup"><span data-stu-id="96c08-113">Requirements</span></span>  

 <span data-ttu-id="96c08-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="96c08-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="96c08-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="96c08-115">See also</span></span>

- [<span data-ttu-id="96c08-116">ISymUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="96c08-116">ISymUnmanagedMethod Interface</span></span>](isymunmanagedmethod-interface.md)
