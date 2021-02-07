---
description: 了解详细信息： ISymUnmanagedDocument：： HasEmbeddedSource 方法
title: ISymUnmanagedDocument::HasEmbeddedSource 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.HasEmbeddedSource
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::HasEmbeddedSource
helpviewer_keywords:
- HasEmbeddedSource method [.NET Framework debugging]
- ISymUnmanagedDocument::HasEmbeddedSource method [.NET Framework debugging]
ms.assetid: 385fc4d3-365c-4645-b7b0-6c4c5344b79f
topic_type:
- apiref
ms.openlocfilehash: fcab83fea65d9a9e483bff9d2d75714c233718eb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710122"
---
# <a name="isymunmanageddocumenthasembeddedsource-method"></a><span data-ttu-id="2b7c7-103">ISymUnmanagedDocument::HasEmbeddedSource 方法</span><span class="sxs-lookup"><span data-stu-id="2b7c7-103">ISymUnmanagedDocument::HasEmbeddedSource Method</span></span>

<span data-ttu-id="2b7c7-104">`true`如果文档在调试符号中嵌入了源，则返回; 否则返回 `false` 。</span><span class="sxs-lookup"><span data-stu-id="2b7c7-104">Returns `true` if the document has source embedded in the debugging symbols; otherwise, returns `false`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b7c7-105">语法</span><span class="sxs-lookup"><span data-stu-id="2b7c7-105">Syntax</span></span>  
  
```cpp  
HRESULT HasEmbeddedSource(  
   [out, retval]  BOOL  *pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2b7c7-106">参数</span><span class="sxs-lookup"><span data-stu-id="2b7c7-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="2b7c7-107">弄指向一个变量的指针，该变量指示文档是否将源嵌入调试符号。</span><span class="sxs-lookup"><span data-stu-id="2b7c7-107">[out] A pointer to a variable that indicates whether the document has source embedded in the debugging symbols.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2b7c7-108">返回值</span><span class="sxs-lookup"><span data-stu-id="2b7c7-108">Return Value</span></span>  

 <span data-ttu-id="2b7c7-109">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="2b7c7-109">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b7c7-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="2b7c7-110">See also</span></span>

- [<span data-ttu-id="2b7c7-111">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="2b7c7-111">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
