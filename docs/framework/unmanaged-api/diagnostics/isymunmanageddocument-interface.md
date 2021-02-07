---
description: 了解详细信息： ISymUnmanagedDocument 接口
title: ISymUnmanagedDocument 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument
helpviewer_keywords:
- ISymUnmanagedDocument interface [.NET Framework debugging]
ms.assetid: 5c26b366-6e81-467c-9dd0-02dd26fee0a3
topic_type:
- apiref
ms.openlocfilehash: cd1907e570dd15ebcac3ee12aa09c626c9bb7787
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710135"
---
# <a name="isymunmanageddocument-interface"></a><span data-ttu-id="b1987-103">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="b1987-103">ISymUnmanagedDocument Interface</span></span>

<span data-ttu-id="b1987-104">表示由符号存储引用的文档。</span><span class="sxs-lookup"><span data-stu-id="b1987-104">Represents a document referenced by a symbol store.</span></span> <span data-ttu-id="b1987-105">文档由统一资源定位符定义 (URL) 和文档类型 GUID。</span><span class="sxs-lookup"><span data-stu-id="b1987-105">A document is defined by a uniform resource locator (URL) and a document type GUID.</span></span> <span data-ttu-id="b1987-106">可以通过使用 URL 和文档类型 GUID 来查找文档，而不考虑其存储方式。</span><span class="sxs-lookup"><span data-stu-id="b1987-106">You can locate the document regardless of how it is stored by using the URL and document type GUID.</span></span> <span data-ttu-id="b1987-107">可以将文档源存储在符号存储区中，并通过此接口进行检索。</span><span class="sxs-lookup"><span data-stu-id="b1987-107">You can store the document source in the symbol store and retrieve it through this interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b1987-108">方法</span><span class="sxs-lookup"><span data-stu-id="b1987-108">Methods</span></span>  
  
|<span data-ttu-id="b1987-109">方法</span><span class="sxs-lookup"><span data-stu-id="b1987-109">Method</span></span>|<span data-ttu-id="b1987-110">说明</span><span class="sxs-lookup"><span data-stu-id="b1987-110">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b1987-111">FindClosestLine 方法</span><span class="sxs-lookup"><span data-stu-id="b1987-111">FindClosestLine Method</span></span>](isymunmanageddocument-findclosestline-method.md)|<span data-ttu-id="b1987-112">如果此文档中的一行可能是也可能不是序列点，则返回作为序列点的最近行。</span><span class="sxs-lookup"><span data-stu-id="b1987-112">Returns the closest line that is a sequence point, given a line in this document that may or may not be a sequence point.</span></span>|  
|[<span data-ttu-id="b1987-113">GetCheckSum 方法</span><span class="sxs-lookup"><span data-stu-id="b1987-113">GetCheckSum Method</span></span>](isymunmanageddocument-getchecksum-method.md)|<span data-ttu-id="b1987-114">获取校验和。</span><span class="sxs-lookup"><span data-stu-id="b1987-114">Gets the checksum.</span></span>|  
|[<span data-ttu-id="b1987-115">GetCheckSumAlgorithmId 方法</span><span class="sxs-lookup"><span data-stu-id="b1987-115">GetCheckSumAlgorithmId Method</span></span>](isymunmanageddocument-getchecksumalgorithmid-method.md)|<span data-ttu-id="b1987-116">如果没有校验和，则获取校验和算法标识符，或返回所有零的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b1987-116">Gets the checksum algorithm identifier, or returns a GUID of all zeros if there is no checksum.</span></span>|  
|[<span data-ttu-id="b1987-117">GetDocumentType 方法</span><span class="sxs-lookup"><span data-stu-id="b1987-117">GetDocumentType Method</span></span>](isymunmanageddocument-getdocumenttype-method.md)|<span data-ttu-id="b1987-118">获取此文档的文档类型。</span><span class="sxs-lookup"><span data-stu-id="b1987-118">Gets the document type of this document.</span></span>|  
|[<span data-ttu-id="b1987-119">GetLanguage 方法</span><span class="sxs-lookup"><span data-stu-id="b1987-119">GetLanguage Method</span></span>](isymunmanageddocument-getlanguage-method.md)|<span data-ttu-id="b1987-120">获取此文档的语言标识符。</span><span class="sxs-lookup"><span data-stu-id="b1987-120">Gets the language identifier of this document.</span></span>|  
|[<span data-ttu-id="b1987-121">GetLanguageVendor 方法</span><span class="sxs-lookup"><span data-stu-id="b1987-121">GetLanguageVendor Method</span></span>](isymunmanageddocument-getlanguagevendor-method.md)|<span data-ttu-id="b1987-122">获取此文档的语言供应商。</span><span class="sxs-lookup"><span data-stu-id="b1987-122">Gets the language vendor of this document.</span></span>|  
|[<span data-ttu-id="b1987-123">GetSourceLength 方法</span><span class="sxs-lookup"><span data-stu-id="b1987-123">GetSourceLength Method</span></span>](isymunmanageddocument-getsourcelength-method.md)|<span data-ttu-id="b1987-124">获取嵌入源的长度（以字节表示）。</span><span class="sxs-lookup"><span data-stu-id="b1987-124">Gets the length, in bytes, of the embedded source.</span></span>|  
|[<span data-ttu-id="b1987-125">GetSourceRange 方法</span><span class="sxs-lookup"><span data-stu-id="b1987-125">GetSourceRange Method</span></span>](isymunmanageddocument-getsourcerange-method.md)|<span data-ttu-id="b1987-126">将嵌入源的指定范围返回到给定缓冲区中。</span><span class="sxs-lookup"><span data-stu-id="b1987-126">Returns the specified range of the embedded source into the given buffer.</span></span>|  
|[<span data-ttu-id="b1987-127">GetURL 方法</span><span class="sxs-lookup"><span data-stu-id="b1987-127">GetURL Method</span></span>](isymunmanageddocument-geturl-method.md)|<span data-ttu-id="b1987-128">返回此文档的 URL。</span><span class="sxs-lookup"><span data-stu-id="b1987-128">Returns the URL for this document.</span></span>|  
|[<span data-ttu-id="b1987-129">HasEmbeddedSource 方法</span><span class="sxs-lookup"><span data-stu-id="b1987-129">HasEmbeddedSource Method</span></span>](isymunmanageddocument-hasembeddedsource-method.md)|<span data-ttu-id="b1987-130">`true`如果文档在调试符号中嵌入了源，则返回; 否则返回 `false` 。</span><span class="sxs-lookup"><span data-stu-id="b1987-130">Returns `true` if the document has source embedded in the debugging symbols; otherwise, returns `false`.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b1987-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="b1987-131">See also</span></span>

- [<span data-ttu-id="b1987-132">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="b1987-132">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
