---
description: 了解详细信息： ISymUnmanagedWriter5 接口
title: ISymUnmanagedWriter5 接口
ms.date: 03/30/2017
ms.assetid: 15b8526e-4f5d-475c-a1e3-d8b2d145c879
ms.openlocfilehash: 0902385576e1eed17cea672b04858c7e3ef7add8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761624"
---
# <a name="isymunmanagedwriter5-interface"></a><span data-ttu-id="87fd3-103">ISymUnmanagedWriter5 接口</span><span class="sxs-lookup"><span data-stu-id="87fd3-103">ISymUnmanagedWriter5 Interface</span></span>

<span data-ttu-id="87fd3-104">ISymUnmanagedWriter5 接口。</span><span class="sxs-lookup"><span data-stu-id="87fd3-104">ISymUnmanagedWriter5 interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="87fd3-105">语法</span><span class="sxs-lookup"><span data-stu-id="87fd3-105">Syntax</span></span>  
  
```idl  
[object,uuid(DCF7780D-BDE9-45DF-ACFE-21731A32000C),pointer_default(unique)]interface ISymUnmanagedWriter5 : ISymUnmanagedWriter4  
```  
  
## <a name="methods"></a><span data-ttu-id="87fd3-106">方法</span><span class="sxs-lookup"><span data-stu-id="87fd3-106">Methods</span></span>  

 <span data-ttu-id="87fd3-107">此接口包含下列方法：</span><span class="sxs-lookup"><span data-stu-id="87fd3-107">This interface contains the following methods:</span></span>  
  
|<span data-ttu-id="87fd3-108">方法</span><span class="sxs-lookup"><span data-stu-id="87fd3-108">Method</span></span>|<span data-ttu-id="87fd3-109">说明</span><span class="sxs-lookup"><span data-stu-id="87fd3-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="87fd3-110">CloseMapTokensToSourceSpans 方法</span><span class="sxs-lookup"><span data-stu-id="87fd3-110">CloseMapTokensToSourceSpans Method</span></span>](isymunmanagedwriter5-closemaptokenstosourcespans-method.md)|<span data-ttu-id="87fd3-111">关闭 "特定自定义数据" 部分以获取令牌到源范围的映射信息。</span><span class="sxs-lookup"><span data-stu-id="87fd3-111">Close the special custom data section for token-to- source span mapping information.</span></span> <span data-ttu-id="87fd3-112">关闭后，不能再添加映射信息。</span><span class="sxs-lookup"><span data-stu-id="87fd3-112">After it is closed, no more mapping information can be added.</span></span>|  
|[<span data-ttu-id="87fd3-113">MapTokenToSourceSpan 方法</span><span class="sxs-lookup"><span data-stu-id="87fd3-113">MapTokenToSourceSpan Method</span></span>](isymunmanagedwriter5-maptokentosourcespan-method.md)|<span data-ttu-id="87fd3-114">将给定的元数据标记映射到指定源文件中的给定源行范围。</span><span class="sxs-lookup"><span data-stu-id="87fd3-114">Maps the given metadata token to the given source line span in the specified source file.</span></span><br /><br /> <span data-ttu-id="87fd3-115">必须在对 [OpenMapTokensToSourceSpans 方法](isymunmanagedwriter5-openmaptokenstosourcespans-method.md) 和 [CloseMapTokensToSourceSpans 方法](isymunmanagedwriter5-closemaptokenstosourcespans-method.md)的调用之间调用。</span><span class="sxs-lookup"><span data-stu-id="87fd3-115">Must be called between calls to [OpenMapTokensToSourceSpans Method](isymunmanagedwriter5-openmaptokenstosourcespans-method.md) and [CloseMapTokensToSourceSpans Method](isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span></span>|  
|[<span data-ttu-id="87fd3-116">OpenMapTokensToSourceSpans 方法</span><span class="sxs-lookup"><span data-stu-id="87fd3-116">OpenMapTokensToSourceSpans Method</span></span>](isymunmanagedwriter5-openmaptokenstosourcespans-method.md)|<span data-ttu-id="87fd3-117">打开一个特殊的自定义数据部分，将令牌到源范围的映射信息发送到。</span><span class="sxs-lookup"><span data-stu-id="87fd3-117">Open a special custom data section to emit token-to- source span mapping information into.</span></span> <span data-ttu-id="87fd3-118">如果方法已打开（或相反），则打开此节是错误的。</span><span class="sxs-lookup"><span data-stu-id="87fd3-118">Opening this section when a method is already open, or vice versa, is an error.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="87fd3-119">要求</span><span class="sxs-lookup"><span data-stu-id="87fd3-119">Requirements</span></span>  

 <span data-ttu-id="87fd3-120">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="87fd3-120">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="87fd3-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="87fd3-121">See also</span></span>

- [<span data-ttu-id="87fd3-122">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="87fd3-122">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="87fd3-123">ISymUnmanagedWriter4 接口</span><span class="sxs-lookup"><span data-stu-id="87fd3-123">ISymUnmanagedWriter4 Interface</span></span>](isymunmanagedwriter4-interface.md)
