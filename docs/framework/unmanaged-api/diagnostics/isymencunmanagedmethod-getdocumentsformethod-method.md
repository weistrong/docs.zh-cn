---
description: 了解详细信息： ISymENCUnmanagedMethod：： GetDocumentsForMethod 方法
title: ISymENCUnmanagedMethod::GetDocumentsForMethod 方法
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetDocumentsForMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetDocumentsForMethod
helpviewer_keywords:
- GetDocumentsForMethod method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetDocumentsForMethod method [.NET Framework debugging]
ms.assetid: bd6ccde5-d578-48d8-abed-b474fbd48d13
topic_type:
- apiref
ms.openlocfilehash: 01c7280abe437266618d96c6e195e61a4f830131
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721536"
---
# <a name="isymencunmanagedmethodgetdocumentsformethod-method"></a><span data-ttu-id="84a98-103">ISymENCUnmanagedMethod::GetDocumentsForMethod 方法</span><span class="sxs-lookup"><span data-stu-id="84a98-103">ISymENCUnmanagedMethod::GetDocumentsForMethod Method</span></span>

<span data-ttu-id="84a98-104">获取此方法在中具有线条的文档。</span><span class="sxs-lookup"><span data-stu-id="84a98-104">Gets the documents that this method has lines in.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84a98-105">语法</span><span class="sxs-lookup"><span data-stu-id="84a98-105">Syntax</span></span>  
  
```cpp  
HRESULT GetDocumentsForMethod(  
    [in]  ULONG32  cDocs,  
    [out] ULONG32  *pcDocs,
    [in, size_is(cDocs)] ISymUnmanagedDocument* documents[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="84a98-106">参数</span><span class="sxs-lookup"><span data-stu-id="84a98-106">Parameters</span></span>  

 `cDocs`  
 <span data-ttu-id="84a98-107">中所指向的缓冲区的长度 `pcDocs` 。</span><span class="sxs-lookup"><span data-stu-id="84a98-107">[in] The length of the buffer pointed to by `pcDocs`.</span></span>  
  
 `pcDocs`  
 <span data-ttu-id="84a98-108">弄指向的指针， `ULONG32` 该指针接收包含文档所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="84a98-108">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the documents.</span></span>  
  
 `documents`  
 <span data-ttu-id="84a98-109">中包含文档的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="84a98-109">[in] The buffer that contains the documents.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="84a98-110">返回值</span><span class="sxs-lookup"><span data-stu-id="84a98-110">Return Value</span></span>  

 <span data-ttu-id="84a98-111">如果该方法成功，则 S_OK;否则为错误代码。</span><span class="sxs-lookup"><span data-stu-id="84a98-111">S_OK if the method succeeds; otherwise, an error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="84a98-112">要求</span><span class="sxs-lookup"><span data-stu-id="84a98-112">Requirements</span></span>  

 <span data-ttu-id="84a98-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="84a98-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84a98-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="84a98-114">See also</span></span>

- [<span data-ttu-id="84a98-115">ISymENCUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="84a98-115">ISymENCUnmanagedMethod Interface</span></span>](isymencunmanagedmethod-interface.md)
