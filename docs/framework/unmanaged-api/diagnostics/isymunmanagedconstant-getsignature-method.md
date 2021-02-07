---
description: 了解详细信息： ISymUnmanagedConstant：： GetSignature 方法
title: ISymUnmanagedConstant::GetSignature 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedConstant.GetSignature
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedConstant::GetSignature
helpviewer_keywords:
- GetSignature method, ISymUnmanagedConstant interface [.NET Framework debugging]
- ISymUnmanagedConstant::GetSignature method [.NET Framework debugging]
ms.assetid: 3eb41151-a228-43e3-ba8f-e6dd3ceb8542
topic_type:
- apiref
ms.openlocfilehash: d28051c9d0e2675e980926fe63ffa7c4d13ef13a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689789"
---
# <a name="isymunmanagedconstantgetsignature-method"></a><span data-ttu-id="0b8dc-103">ISymUnmanagedConstant::GetSignature 方法</span><span class="sxs-lookup"><span data-stu-id="0b8dc-103">ISymUnmanagedConstant::GetSignature Method</span></span>

<span data-ttu-id="0b8dc-104">获取常量的签名。</span><span class="sxs-lookup"><span data-stu-id="0b8dc-104">Gets the signature of the constant.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b8dc-105">语法</span><span class="sxs-lookup"><span data-stu-id="0b8dc-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSignature(  
    [in]  ULONG32  cSig,  
    [out] ULONG32  *pcSig,  
    [out, size_is(cSig),  
        length_is(*pcSig)] BYTE sig[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0b8dc-106">参数</span><span class="sxs-lookup"><span data-stu-id="0b8dc-106">Parameters</span></span>  

 `cSig`  
 <span data-ttu-id="0b8dc-107">中参数指向的缓冲区的长度 `pcSig` 。</span><span class="sxs-lookup"><span data-stu-id="0b8dc-107">[in] The length of the buffer that the `pcSig` parameter points to.</span></span>  
  
 `pcSig`  
 <span data-ttu-id="0b8dc-108">弄指向的指针， `ULONG32` 该指针接收包含签名所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="0b8dc-108">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the signature.</span></span>  
  
 `sig`  
 <span data-ttu-id="0b8dc-109">弄存储签名的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="0b8dc-109">[out] The buffer that stores the signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0b8dc-110">返回值</span><span class="sxs-lookup"><span data-stu-id="0b8dc-110">Return Value</span></span>  

 <span data-ttu-id="0b8dc-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="0b8dc-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0b8dc-112">要求</span><span class="sxs-lookup"><span data-stu-id="0b8dc-112">Requirements</span></span>  

 <span data-ttu-id="0b8dc-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="0b8dc-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b8dc-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="0b8dc-114">See also</span></span>

- [<span data-ttu-id="0b8dc-115">ISymUnmanagedConstant 接口</span><span class="sxs-lookup"><span data-stu-id="0b8dc-115">ISymUnmanagedConstant Interface</span></span>](isymunmanagedconstant-interface.md)
- [<span data-ttu-id="0b8dc-116">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="0b8dc-116">GetName Method</span></span>](isymunmanagedconstant-getname-method.md)
- [<span data-ttu-id="0b8dc-117">GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="0b8dc-117">GetValue Method</span></span>](isymunmanagedconstant-getvalue-method.md)
