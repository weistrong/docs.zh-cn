---
description: 了解详细信息： ISymUnmanagedWriter5：： MapTokenToSourceSpan 方法
title: ISymUnmanagedWriter5::MapTokenToSourceSpan 方法
ms.date: 03/30/2017
ms.assetid: d0fbbf61-71c6-4fb1-8c9f-d619ca5d7d68
ms.openlocfilehash: b30d8051f5d2872488639ce999cccd4248af367f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761611"
---
# <a name="isymunmanagedwriter5maptokentosourcespan-method"></a><span data-ttu-id="fddbc-103">ISymUnmanagedWriter5::MapTokenToSourceSpan 方法</span><span class="sxs-lookup"><span data-stu-id="fddbc-103">ISymUnmanagedWriter5::MapTokenToSourceSpan Method</span></span>

<span data-ttu-id="fddbc-104">将给定的元数据标记映射到指定源文件中的给定源行范围。</span><span class="sxs-lookup"><span data-stu-id="fddbc-104">Maps the given metadata token to the given source line span in the specified source file.</span></span>  
  
 <span data-ttu-id="fddbc-105">必须在对 [OpenMapTokensToSourceSpans 方法](isymunmanagedwriter5-openmaptokenstosourcespans-method.md) 和 [CloseMapTokensToSourceSpans 方法](isymunmanagedwriter5-closemaptokenstosourcespans-method.md)的调用之间调用。</span><span class="sxs-lookup"><span data-stu-id="fddbc-105">Must be called between calls to [OpenMapTokensToSourceSpans Method](isymunmanagedwriter5-openmaptokenstosourcespans-method.md) and [CloseMapTokensToSourceSpans Method](isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fddbc-106">语法</span><span class="sxs-lookup"><span data-stu-id="fddbc-106">Syntax</span></span>  
  
```idl  
HRESULT MapTokenToSourceSpan(    [in] mdToken token,    [in] ISymUnmanagedDocumentWriter* document,    [in] ULONG32 line,    [in] ULONG32 column,    [in] ULONG32 endLine,    [in] ULONG32 endColumn);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fddbc-107">参数</span><span class="sxs-lookup"><span data-stu-id="fddbc-107">Parameters</span></span>  
  
|<span data-ttu-id="fddbc-108">参数</span><span class="sxs-lookup"><span data-stu-id="fddbc-108">Parameter</span></span>|<span data-ttu-id="fddbc-109">说明</span><span class="sxs-lookup"><span data-stu-id="fddbc-109">Description</span></span>|  
|---------------|-----------------|  
|`token`||  
|`document`||  
|`line`||  
|`column`||  
|`endLine`||  
|`endColumn`||  
  
## <a name="return-value"></a><span data-ttu-id="fddbc-110">返回值</span><span class="sxs-lookup"><span data-stu-id="fddbc-110">Return Value</span></span>  

 <span data-ttu-id="fddbc-111">返回 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="fddbc-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fddbc-112">要求</span><span class="sxs-lookup"><span data-stu-id="fddbc-112">Requirements</span></span>  

 <span data-ttu-id="fddbc-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="fddbc-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fddbc-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="fddbc-114">See also</span></span>

- [<span data-ttu-id="fddbc-115">ISymUnmanagedWriter5 接口</span><span class="sxs-lookup"><span data-stu-id="fddbc-115">ISymUnmanagedWriter5 Interface</span></span>](isymunmanagedwriter5-interface.md)
