---
description: 了解详细信息： ISymUnmanagedVariable：： GetSignature 方法
title: ISymUnmanagedVariable::GetSignature 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetSignature
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetSignature
helpviewer_keywords:
- GetSignature method, ISymUnmanagedVariable interface [.NET Framework debugging]
- ISymUnmanagedVariable::GetSignature method [.NET Framework debugging]
ms.assetid: 78c1ba28-a410-4360-805c-23a95408964a
topic_type:
- apiref
ms.openlocfilehash: 6e8242581cf2d59563b6193ed7c7686292cbf775
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762729"
---
# <a name="isymunmanagedvariablegetsignature-method"></a><span data-ttu-id="d2eee-103">ISymUnmanagedVariable::GetSignature 方法</span><span class="sxs-lookup"><span data-stu-id="d2eee-103">ISymUnmanagedVariable::GetSignature Method</span></span>

<span data-ttu-id="d2eee-104">获取此变量的签名。</span><span class="sxs-lookup"><span data-stu-id="d2eee-104">Gets the signature of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d2eee-105">语法</span><span class="sxs-lookup"><span data-stu-id="d2eee-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSignature(  
    [in]  ULONG32  cSig,  
    [out] ULONG32  *pcSig,  
    [out, size_is(cSig),  
        length_is(*pcSig)] BYTE sig[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d2eee-106">参数</span><span class="sxs-lookup"><span data-stu-id="d2eee-106">Parameters</span></span>  

 `cSig`  
 <span data-ttu-id="d2eee-107">中参数指向的缓冲区的长度 `sig` 。</span><span class="sxs-lookup"><span data-stu-id="d2eee-107">[in] The length of the buffer pointed to by the `sig` parameter.</span></span>  
  
 `pcSig`  
 <span data-ttu-id="d2eee-108">弄指向的指针， `ULONG32` 该指针接收包含签名所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="d2eee-108">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the signature.</span></span>  
  
 `sig`  
 <span data-ttu-id="d2eee-109">弄存储签名的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="d2eee-109">[out] The buffer that stores the signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d2eee-110">返回值</span><span class="sxs-lookup"><span data-stu-id="d2eee-110">Return Value</span></span>  

 <span data-ttu-id="d2eee-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="d2eee-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d2eee-112">要求</span><span class="sxs-lookup"><span data-stu-id="d2eee-112">Requirements</span></span>  

 <span data-ttu-id="d2eee-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="d2eee-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2eee-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="d2eee-114">See also</span></span>

- [<span data-ttu-id="d2eee-115">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="d2eee-115">ISymUnmanagedVariable Interface</span></span>](isymunmanagedvariable-interface.md)
