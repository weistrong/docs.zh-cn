---
description: 了解详细信息： ISymENCUnmanagedMethod 接口
title: ISymENCUnmanagedMethod 接口
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod
helpviewer_keywords:
- ISymENCUnmanagedMethod interface [.NET Framework debugging]
ms.assetid: faebf594-67d5-4abf-b9c1-547fd3a1ff87
topic_type:
- apiref
ms.openlocfilehash: 59dd56c20279b2507fc4432182d0abb5b3e9c289
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790316"
---
# <a name="isymencunmanagedmethod-interface"></a><span data-ttu-id="886db-103">ISymENCUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="886db-103">ISymENCUnmanagedMethod Interface</span></span>

<span data-ttu-id="886db-104">提供 "编辑并继续" 功能的信息。</span><span class="sxs-lookup"><span data-stu-id="886db-104">Provides information for the Edit and Continue feature.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="886db-105">方法</span><span class="sxs-lookup"><span data-stu-id="886db-105">Methods</span></span>  
  
|<span data-ttu-id="886db-106">方法</span><span class="sxs-lookup"><span data-stu-id="886db-106">Method</span></span>|<span data-ttu-id="886db-107">说明</span><span class="sxs-lookup"><span data-stu-id="886db-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="886db-108">GetDocumentsForMethod 方法</span><span class="sxs-lookup"><span data-stu-id="886db-108">GetDocumentsForMethod Method</span></span>](isymencunmanagedmethod-getdocumentsformethod-method.md)|<span data-ttu-id="886db-109">获取此方法在中具有线条的文档。</span><span class="sxs-lookup"><span data-stu-id="886db-109">Gets the documents that this method has lines in.</span></span>|  
|[<span data-ttu-id="886db-110">GetDocumentsForMethodCount 方法</span><span class="sxs-lookup"><span data-stu-id="886db-110">GetDocumentsForMethodCount Method</span></span>](isymencunmanagedmethod-getdocumentsformethodcount-method.md)|<span data-ttu-id="886db-111">获取此方法在中包含行的文档数。</span><span class="sxs-lookup"><span data-stu-id="886db-111">Gets the number of documents that this method has lines in.</span></span>|  
|[<span data-ttu-id="886db-112">GetFileNameFromOffset 方法</span><span class="sxs-lookup"><span data-stu-id="886db-112">GetFileNameFromOffset Method</span></span>](isymencunmanagedmethod-getfilenamefromoffset-method.md)|<span data-ttu-id="886db-113">获取与偏移量关联的行的文件名。</span><span class="sxs-lookup"><span data-stu-id="886db-113">Gets the file name for the line associated with an offset.</span></span>|  
|[<span data-ttu-id="886db-114">GetLineFromOffset 方法</span><span class="sxs-lookup"><span data-stu-id="886db-114">GetLineFromOffset Method</span></span>](isymencunmanagedmethod-getlinefromoffset-method.md)|<span data-ttu-id="886db-115">获取与偏移量关联的行信息。</span><span class="sxs-lookup"><span data-stu-id="886db-115">Gets the line information associated with an offset.</span></span>|  
|[<span data-ttu-id="886db-116">GetSourceExtentInDocument 方法</span><span class="sxs-lookup"><span data-stu-id="886db-116">GetSourceExtentInDocument Method</span></span>](isymencunmanagedmethod-getsourceextentindocument-method.md)|<span data-ttu-id="886db-117">获取特定文档中该方法的最小起始行和最大结束行。</span><span class="sxs-lookup"><span data-stu-id="886db-117">Gets the smallest start line and largest end line for the method in a specific document.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="886db-118">要求</span><span class="sxs-lookup"><span data-stu-id="886db-118">Requirements</span></span>  

 <span data-ttu-id="886db-119">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="886db-119">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="886db-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="886db-120">See also</span></span>

- [<span data-ttu-id="886db-121">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="886db-121">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
