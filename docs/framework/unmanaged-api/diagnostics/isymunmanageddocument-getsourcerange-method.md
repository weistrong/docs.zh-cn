---
description: 了解详细信息： ISymUnmanagedDocument：： GetSourceRange 方法
title: ISymUnmanagedDocument::GetSourceRange 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetSourceRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetSourceRange
helpviewer_keywords:
- ISymUnmanagedDocument::GetSourceRange method [.NET Framework debugging]
- GetSourceRange method [.NET Framework debugging]
ms.assetid: 20fefee7-1040-41ba-93dc-bd42f68b90c2
topic_type:
- apiref
ms.openlocfilehash: 98718298d7bf2f44d418a40f17ad19cdee0b6771
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790160"
---
# <a name="isymunmanageddocumentgetsourcerange-method"></a><span data-ttu-id="ac0cb-103">ISymUnmanagedDocument::GetSourceRange 方法</span><span class="sxs-lookup"><span data-stu-id="ac0cb-103">ISymUnmanagedDocument::GetSourceRange Method</span></span>

<span data-ttu-id="ac0cb-104">将嵌入源的指定范围返回到给定缓冲区中。</span><span class="sxs-lookup"><span data-stu-id="ac0cb-104">Returns the specified range of the embedded source into the given buffer.</span></span> <span data-ttu-id="ac0cb-105">缓冲区必须足够大才能容纳源。</span><span class="sxs-lookup"><span data-stu-id="ac0cb-105">The buffer must be large enough to hold the source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac0cb-106">语法</span><span class="sxs-lookup"><span data-stu-id="ac0cb-106">Syntax</span></span>  
  
```cpp  
HRESULT GetSourceRange(  
    [in]  ULONG32  startLine,  
    [in]  ULONG32  startColumn,  
    [in]  ULONG32  endLine,  
    [in]  ULONG32  endColumn,  
    [in]  ULONG32  cSourceBytes,  
    [out] ULONG32  *pcSourceBytes,  
    [out, size_is(cSourceBytes),  
        length_is(*pcSourceBytes)] BYTE source[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ac0cb-107">参数</span><span class="sxs-lookup"><span data-stu-id="ac0cb-107">Parameters</span></span>  

 `startLine`  
 <span data-ttu-id="ac0cb-108">中当前文档中的起始行。</span><span class="sxs-lookup"><span data-stu-id="ac0cb-108">[in] The starting line in the current document.</span></span>  
  
 `startColumn`  
 <span data-ttu-id="ac0cb-109">中当前文档中的起始列。</span><span class="sxs-lookup"><span data-stu-id="ac0cb-109">[in] The starting column in the current document.</span></span>  
  
 `endLine`  
 <span data-ttu-id="ac0cb-110">中当前文档中的最后一行。</span><span class="sxs-lookup"><span data-stu-id="ac0cb-110">[in] The final line in the current document.</span></span>  
  
 `endColumn`  
 <span data-ttu-id="ac0cb-111">中当前文档中的最后一列。</span><span class="sxs-lookup"><span data-stu-id="ac0cb-111">[in] The final column in the current document.</span></span>  
  
 `cSourceBytes`  
 <span data-ttu-id="ac0cb-112">中源的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="ac0cb-112">[in] The size of the source, in bytes.</span></span>  
  
 `pcSourceBytes`  
 <span data-ttu-id="ac0cb-113">弄指向接收源大小的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="ac0cb-113">[out] A pointer to a variable that receives the source size.</span></span>  
  
 `source`  
 <span data-ttu-id="ac0cb-114">弄源文档的指定范围的大小和长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="ac0cb-114">[out] The size and length of the specified range of the source document, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ac0cb-115">返回值</span><span class="sxs-lookup"><span data-stu-id="ac0cb-115">Return Value</span></span>  

 <span data-ttu-id="ac0cb-116">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="ac0cb-116">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac0cb-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="ac0cb-117">See also</span></span>

- [<span data-ttu-id="ac0cb-118">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="ac0cb-118">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
