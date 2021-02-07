---
description: 了解详细信息： ISymENCUnmanagedMethod：： GetDocumentsForMethodCount 方法
title: ISymENCUnmanagedMethod::GetDocumentsForMethodCount 方法
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetDocumentsForMethodCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetDocumentsForMethodCount
helpviewer_keywords:
- GetDocumentsForMethodCount method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetDocumentsForMethodCount method [.NET Framework debugging]
ms.assetid: cc1a823a-3ff3-4a33-b641-96edc93d2b17
topic_type:
- apiref
ms.openlocfilehash: 0594771c544ad1de32531e92f30fe96f245b5699
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738008"
---
# <a name="isymencunmanagedmethodgetdocumentsformethodcount-method"></a><span data-ttu-id="4efff-103">ISymENCUnmanagedMethod::GetDocumentsForMethodCount 方法</span><span class="sxs-lookup"><span data-stu-id="4efff-103">ISymENCUnmanagedMethod::GetDocumentsForMethodCount Method</span></span>

<span data-ttu-id="4efff-104">获取此方法在中包含行的文档数。</span><span class="sxs-lookup"><span data-stu-id="4efff-104">Gets the number of documents that this method has lines in.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4efff-105">语法</span><span class="sxs-lookup"><span data-stu-id="4efff-105">Syntax</span></span>  
  
```cpp  
HRESULT GetDocumentsForMethodCount(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4efff-106">参数</span><span class="sxs-lookup"><span data-stu-id="4efff-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="4efff-107">弄指向的指针 `ULONG32` ，该指针接收包含文档所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="4efff-107">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the documents.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4efff-108">返回值</span><span class="sxs-lookup"><span data-stu-id="4efff-108">Return Value</span></span>  

 <span data-ttu-id="4efff-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="4efff-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4efff-110">要求</span><span class="sxs-lookup"><span data-stu-id="4efff-110">Requirements</span></span>  

 <span data-ttu-id="4efff-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="4efff-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4efff-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="4efff-112">See also</span></span>

- [<span data-ttu-id="4efff-113">ISymENCUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="4efff-113">ISymENCUnmanagedMethod Interface</span></span>](isymencunmanagedmethod-interface.md)
