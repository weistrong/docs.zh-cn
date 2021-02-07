---
description: 了解详细信息： ISymUnmanagedWriter：： SetMethodSourceRange 方法
title: ISymUnmanagedWriter::SetMethodSourceRange 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.SetMethodSourceRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::SetMethodSourceRange
helpviewer_keywords:
- SetMethodSourceRange method [.NET Framework debugging]
- ISymUnmanagedWriter::SetMethodSourceRange method [.NET Framework debugging]
ms.assetid: c698b86e-ace7-4b21-9549-f52d6a034959
topic_type:
- apiref
ms.openlocfilehash: 2e2f0f664d8be30a8c3628100fafb3740d34f54f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762066"
---
# <a name="isymunmanagedwritersetmethodsourcerange-method"></a><span data-ttu-id="c0977-103">ISymUnmanagedWriter::SetMethodSourceRange 方法</span><span class="sxs-lookup"><span data-stu-id="c0977-103">ISymUnmanagedWriter::SetMethodSourceRange Method</span></span>

<span data-ttu-id="c0977-104">指定源文件内方法的真正开始和结尾。</span><span class="sxs-lookup"><span data-stu-id="c0977-104">Specifies the true start and end of a method within a source file.</span></span> <span data-ttu-id="c0977-105">使用此方法可以独立于方法中存在的序列点来指定方法的范围。</span><span class="sxs-lookup"><span data-stu-id="c0977-105">Use this method to specify the extent of a method independently of the sequence points that exist within the method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0977-106">语法</span><span class="sxs-lookup"><span data-stu-id="c0977-106">Syntax</span></span>  
  
```cpp  
HRESULT SetMethodSourceRange(  
    [in] ISymUnmanagedDocumentWriter  *startDoc,  
    [in] ULONG32                      startLine,  
    [in] ULONG32                      startColumn,  
    [in] ISymUnmanagedDocumentWriter  *endDoc,  
    [in] ULONG32                      endLine,  
    [in] ULONG32                      endColumn);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c0977-107">参数</span><span class="sxs-lookup"><span data-stu-id="c0977-107">Parameters</span></span>  

 `startDoc`  
 <span data-ttu-id="c0977-108">中指向包含起始位置的文档的指针。</span><span class="sxs-lookup"><span data-stu-id="c0977-108">[in] A pointer to the document containing the starting position.</span></span>  
  
 `startLine`  
 <span data-ttu-id="c0977-109">中起始行号。</span><span class="sxs-lookup"><span data-stu-id="c0977-109">[in] The starting line number.</span></span>  
  
 `startColumn`  
 <span data-ttu-id="c0977-110">中起始列。</span><span class="sxs-lookup"><span data-stu-id="c0977-110">[in] The starting column.</span></span>  
  
 `endDoc`  
 <span data-ttu-id="c0977-111">中指向包含结束位置的文档的指针。</span><span class="sxs-lookup"><span data-stu-id="c0977-111">[in] A pointer to the document containing the ending position.</span></span>  
  
 `endLine`  
 <span data-ttu-id="c0977-112">中结束行号。</span><span class="sxs-lookup"><span data-stu-id="c0977-112">[in] The ending line number.</span></span>  
  
 `endColumn`  
 <span data-ttu-id="c0977-113">中结束列号。</span><span class="sxs-lookup"><span data-stu-id="c0977-113">[in] The ending column number.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c0977-114">返回值</span><span class="sxs-lookup"><span data-stu-id="c0977-114">Return Value</span></span>  

 <span data-ttu-id="c0977-115">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="c0977-115">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0977-116">要求</span><span class="sxs-lookup"><span data-stu-id="c0977-116">Requirements</span></span>  

 <span data-ttu-id="c0977-117">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="c0977-117">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0977-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="c0977-118">See also</span></span>

- [<span data-ttu-id="c0977-119">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="c0977-119">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
