---
description: 了解详细信息： ISymUnmanagedDocument：： FindClosestLine 方法
title: ISymUnmanagedDocument::FindClosestLine 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.FindClosestLine
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::FindClosestLine
helpviewer_keywords:
- FindClosestLine method [.NET Framework debugging]
- ISymUnmanagedDocument::FindClosestLine method [.NET Framework debugging]
ms.assetid: 628f2a04-e529-407d-841e-3b3da219a9cb
topic_type:
- apiref
ms.openlocfilehash: 0409a5cc29bf148a49a5267d34662f763fc302d9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737826"
---
# <a name="isymunmanageddocumentfindclosestline-method"></a><span data-ttu-id="2dec7-103">ISymUnmanagedDocument::FindClosestLine 方法</span><span class="sxs-lookup"><span data-stu-id="2dec7-103">ISymUnmanagedDocument::FindClosestLine Method</span></span>

<span data-ttu-id="2dec7-104">如果此文档中的一行可能是也可能不是序列点，则返回作为序列点的最近行。</span><span class="sxs-lookup"><span data-stu-id="2dec7-104">Returns the closest line that is a sequence point, given a line in this document that may or may not be a sequence point.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2dec7-105">语法</span><span class="sxs-lookup"><span data-stu-id="2dec7-105">Syntax</span></span>  
  
```cpp  
HRESULT FindClosestLine(  
    [in]  ULONG32  line,  
    [out, retval] ULONG32*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2dec7-106">参数</span><span class="sxs-lookup"><span data-stu-id="2dec7-106">Parameters</span></span>  

 `line`  
 <span data-ttu-id="2dec7-107">中此文档中的一行。</span><span class="sxs-lookup"><span data-stu-id="2dec7-107">[in] A line in this document.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="2dec7-108">弄指向接收行的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="2dec7-108">[out] A pointer to a variable that receives the line.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2dec7-109">返回值</span><span class="sxs-lookup"><span data-stu-id="2dec7-109">Return Value</span></span>  

 <span data-ttu-id="2dec7-110">如果该方法成功，则 S_OK;否则为错误代码。</span><span class="sxs-lookup"><span data-stu-id="2dec7-110">S_OK if the method succeeds; otherwise, an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2dec7-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="2dec7-111">See also</span></span>

- [<span data-ttu-id="2dec7-112">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="2dec7-112">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
