---
description: 了解详细信息： ISymUnmanagedWriter2 接口
title: ISymUnmanagedWriter2 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter2
helpviewer_keywords:
- ISymUnmanagedWriter2 interface [.NET Framework debugging]
ms.assetid: 8e78faa4-cf43-44fb-a91d-94d6df692a25
topic_type:
- apiref
ms.openlocfilehash: 228bae40e12376b3b5e8ca3bbd3463ba70a6d67b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761770"
---
# <a name="isymunmanagedwriter2-interface"></a><span data-ttu-id="9f7df-103">ISymUnmanagedWriter2 接口</span><span class="sxs-lookup"><span data-stu-id="9f7df-103">ISymUnmanagedWriter2 Interface</span></span>

<span data-ttu-id="9f7df-104">表示符号编写器，并提供定义文档、序列点、词法范围和变量的方法。</span><span class="sxs-lookup"><span data-stu-id="9f7df-104">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="9f7df-105">此接口扩展 [ISymUnmanagedWriter](isymunmanagedwriter-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="9f7df-105">This interface extends the [ISymUnmanagedWriter](isymunmanagedwriter-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9f7df-106">方法</span><span class="sxs-lookup"><span data-stu-id="9f7df-106">Methods</span></span>  
  
|<span data-ttu-id="9f7df-107">方法</span><span class="sxs-lookup"><span data-stu-id="9f7df-107">Method</span></span>|<span data-ttu-id="9f7df-108">说明</span><span class="sxs-lookup"><span data-stu-id="9f7df-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9f7df-109">DefineConstant2 方法</span><span class="sxs-lookup"><span data-stu-id="9f7df-109">DefineConstant2 Method</span></span>](isymunmanagedwriter2-defineconstant2-method.md)|<span data-ttu-id="9f7df-110">定义常数值的名称。</span><span class="sxs-lookup"><span data-stu-id="9f7df-110">Defines a name for a constant value.</span></span>|  
|[<span data-ttu-id="9f7df-111">DefineGlobalVariable2 方法</span><span class="sxs-lookup"><span data-stu-id="9f7df-111">DefineGlobalVariable2 Method</span></span>](isymunmanagedwriter2-defineglobalvariable2-method.md)|<span data-ttu-id="9f7df-112">定义单个全局变量。</span><span class="sxs-lookup"><span data-stu-id="9f7df-112">Defines a single global variable.</span></span>|  
|[<span data-ttu-id="9f7df-113">DefineLocalVariable2 方法</span><span class="sxs-lookup"><span data-stu-id="9f7df-113">DefineLocalVariable2 Method</span></span>](isymunmanagedwriter2-definelocalvariable2-method.md)|<span data-ttu-id="9f7df-114">在当前词法范围内定义单个变量。</span><span class="sxs-lookup"><span data-stu-id="9f7df-114">Defines a single variable in the current lexical scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9f7df-115">要求</span><span class="sxs-lookup"><span data-stu-id="9f7df-115">Requirements</span></span>  

 <span data-ttu-id="9f7df-116">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="9f7df-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f7df-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="9f7df-117">See also</span></span>

- [<span data-ttu-id="9f7df-118">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="9f7df-118">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="9f7df-119">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="9f7df-119">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="9f7df-120">ISymUnmanagedWriter3 接口</span><span class="sxs-lookup"><span data-stu-id="9f7df-120">ISymUnmanagedWriter3 Interface</span></span>](isymunmanagedwriter3-interface.md)
