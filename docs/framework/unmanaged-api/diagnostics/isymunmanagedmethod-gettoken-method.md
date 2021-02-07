---
description: 了解详细信息： ISymUnmanagedMethod：： GetToken 方法
title: ISymUnmanagedMethod::GetToken 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetToken
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetToken
helpviewer_keywords:
- ISymUnmanagedMethod::GetToken method [.NET Framework debugging]
- GetToken method, ISymUnmanagedMethod interface [.NET Framework debugging]
ms.assetid: 4effbe95-c36e-4a45-8b2a-ee21339415fb
topic_type:
- apiref
ms.openlocfilehash: fde9936a6e79b9d1fff5b38ee7242cf5bb71369d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721302"
---
# <a name="isymunmanagedmethodgettoken-method"></a><span data-ttu-id="a675c-103">ISymUnmanagedMethod::GetToken 方法</span><span class="sxs-lookup"><span data-stu-id="a675c-103">ISymUnmanagedMethod::GetToken Method</span></span>

<span data-ttu-id="a675c-104">返回此方法的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="a675c-104">Returns the metadata token for this method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a675c-105">语法</span><span class="sxs-lookup"><span data-stu-id="a675c-105">Syntax</span></span>  
  
```cpp  
HRESULT GetToken(  
   [out, retval]  mdMethodDef  *pToken);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a675c-106">参数</span><span class="sxs-lookup"><span data-stu-id="a675c-106">Parameters</span></span>  

 `pToken`  
 <span data-ttu-id="a675c-107">弄指向的指针， `mdMethodDef` 该指针接收包含元数据所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="a675c-107">[out] A pointer to a `mdMethodDef` that receives the size, in characters, of the buffer required to contain the metadata.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a675c-108">返回值</span><span class="sxs-lookup"><span data-stu-id="a675c-108">Return Value</span></span>  

 <span data-ttu-id="a675c-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="a675c-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a675c-110">要求</span><span class="sxs-lookup"><span data-stu-id="a675c-110">Requirements</span></span>  

 <span data-ttu-id="a675c-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="a675c-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a675c-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="a675c-112">See also</span></span>

- [<span data-ttu-id="a675c-113">ISymUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="a675c-113">ISymUnmanagedMethod Interface</span></span>](isymunmanagedmethod-interface.md)
