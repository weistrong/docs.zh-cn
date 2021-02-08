---
description: 了解详细信息： ISymUnmanagedReader：： GetDocumentVersion 方法
title: ISymUnmanagedReader::GetDocumentVersion 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetDocumentVersion
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetDocumentVersion
helpviewer_keywords:
- GetDocumentVersion method [.NET Framework debugging]
- ISymUnmanagedReader::GetDocumentVersion method [.NET Framework debugging]
ms.assetid: a51f1f64-e084-44c5-830c-2222da5a6bbf
topic_type:
- apiref
ms.openlocfilehash: e6877a10f0c285186330b320c9b614939f4d9e3f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800196"
---
# <a name="isymunmanagedreadergetdocumentversion-method"></a><span data-ttu-id="d6d7a-103">ISymUnmanagedReader::GetDocumentVersion 方法</span><span class="sxs-lookup"><span data-stu-id="d6d7a-103">ISymUnmanagedReader::GetDocumentVersion Method</span></span>

<span data-ttu-id="d6d7a-104">获取指定文档的指定版本。</span><span class="sxs-lookup"><span data-stu-id="d6d7a-104">Gets the specified version of the specified document.</span></span> <span data-ttu-id="d6d7a-105">文档版本从1开始，并在每次使用 [UpdateSymbolStore](isymunmanagedreader-updatesymbolstore-method.md) 方法更新文档时递增。</span><span class="sxs-lookup"><span data-stu-id="d6d7a-105">The document version starts at 1 and is incremented each time the document is updated using the [UpdateSymbolStore](isymunmanagedreader-updatesymbolstore-method.md) method.</span></span> <span data-ttu-id="d6d7a-106">如果 `pbCurrent` 参数为 `true` ，则这是最新版本的文档。</span><span class="sxs-lookup"><span data-stu-id="d6d7a-106">If the `pbCurrent` parameter is `true`, this is the latest version of the document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d6d7a-107">语法</span><span class="sxs-lookup"><span data-stu-id="d6d7a-107">Syntax</span></span>  
  
```cpp  
HRESULT GetDocumentVersion (  
    [in]  ISymUnmanagedDocument *pDoc,  
    [out] int* version,  
    [out] BOOL* pbCurrent);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d6d7a-108">参数</span><span class="sxs-lookup"><span data-stu-id="d6d7a-108">Parameters</span></span>  

 `pDoc`  
 <span data-ttu-id="d6d7a-109">中指定的文档。</span><span class="sxs-lookup"><span data-stu-id="d6d7a-109">[in] The specified document.</span></span>  
  
 `version`  
 <span data-ttu-id="d6d7a-110">弄指向一个变量的指针，该变量接收指定文档的版本。</span><span class="sxs-lookup"><span data-stu-id="d6d7a-110">[out] A pointer to a variable that receives the version of the specified document.</span></span>  
  
 `pbCurrent`  
 <span data-ttu-id="d6d7a-111">弄指向一个变量的指针， `true` 如果这是该文档的最新版本，则为; `false` 如果它不是最新版本，则为。</span><span class="sxs-lookup"><span data-stu-id="d6d7a-111">[out] A pointer to a variable that receives `true` if this is the latest version of the document, or `false` if it isn't the latest version.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d6d7a-112">返回值</span><span class="sxs-lookup"><span data-stu-id="d6d7a-112">Return Value</span></span>  

 <span data-ttu-id="d6d7a-113">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="d6d7a-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d6d7a-114">要求</span><span class="sxs-lookup"><span data-stu-id="d6d7a-114">Requirements</span></span>  

 <span data-ttu-id="d6d7a-115">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="d6d7a-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6d7a-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="d6d7a-116">See also</span></span>

- [<span data-ttu-id="d6d7a-117">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="d6d7a-117">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
