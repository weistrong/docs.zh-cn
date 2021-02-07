---
description: 了解详细信息： ISymUnmanagedScope2：： GetConstants 方法
title: ISymUnmanagedScope2::GetConstants 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope2.GetConstants
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope2::GetConstants
helpviewer_keywords:
- ISymUnmanagedScope2::GetConstants method [.NET Framework debugging]
- GetConstants method [.NET Framework debugging]
ms.assetid: f241b620-9ec5-42fd-92ef-3b22329db72a
topic_type:
- apiref
ms.openlocfilehash: 025bb9ddd0501f2309b2c0a3f7af20eb961604cb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763210"
---
# <a name="isymunmanagedscope2getconstants-method"></a><span data-ttu-id="d2a73-103">ISymUnmanagedScope2::GetConstants 方法</span><span class="sxs-lookup"><span data-stu-id="d2a73-103">ISymUnmanagedScope2::GetConstants Method</span></span>

<span data-ttu-id="d2a73-104">获取在此范围内定义的局部变量。</span><span class="sxs-lookup"><span data-stu-id="d2a73-104">Gets the local constants defined within this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d2a73-105">语法</span><span class="sxs-lookup"><span data-stu-id="d2a73-105">Syntax</span></span>  
  
```cpp  
HRESULT GetConstants(  
     [in]  ULONG32  cConstants,  
     [out] ULONG32  *pcConstants,  
     [out, size_is(cConstants),  
         length_is(*pcConstants)] ISymUnmanagedConstant*
             constants[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d2a73-106">参数</span><span class="sxs-lookup"><span data-stu-id="d2a73-106">Parameters</span></span>  

 `cConstants`  
 <span data-ttu-id="d2a73-107">中参数指向的缓冲区的长度 `pcConstants` 。</span><span class="sxs-lookup"><span data-stu-id="d2a73-107">[in] The length of the buffer that the `pcConstants` parameter points to.</span></span>  
  
 `pcConstants`  
 <span data-ttu-id="d2a73-108">弄指向的指针， `ULONG32` 该指针接收包含常量所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="d2a73-108">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the constants.</span></span>  
  
 `constants`  
 <span data-ttu-id="d2a73-109">弄用于存储常量的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="d2a73-109">[out] The buffer that stores the constants.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d2a73-110">返回值</span><span class="sxs-lookup"><span data-stu-id="d2a73-110">Return Value</span></span>  

 <span data-ttu-id="d2a73-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="d2a73-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d2a73-112">要求</span><span class="sxs-lookup"><span data-stu-id="d2a73-112">Requirements</span></span>  

 <span data-ttu-id="d2a73-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="d2a73-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2a73-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="d2a73-114">See also</span></span>

- [<span data-ttu-id="d2a73-115">ISymUnmanagedScope2 接口</span><span class="sxs-lookup"><span data-stu-id="d2a73-115">ISymUnmanagedScope2 Interface</span></span>](isymunmanagedscope2-interface.md)
