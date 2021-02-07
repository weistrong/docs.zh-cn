---
description: 了解详细信息： ISymUnmanagedWriter3 接口
title: ISymUnmanagedWriter3 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter3
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter3
helpviewer_keywords:
- ISymUnmanagedWriter3 interface [.NET Framework debugging]
ms.assetid: a034c21e-e371-4360-b470-29e88288948f
topic_type:
- apiref
ms.openlocfilehash: 586220af85f193b43acf0578706d9f67e3e83386
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761728"
---
# <a name="isymunmanagedwriter3-interface"></a><span data-ttu-id="5fbf9-103">ISymUnmanagedWriter3 接口</span><span class="sxs-lookup"><span data-stu-id="5fbf9-103">ISymUnmanagedWriter3 Interface</span></span>

<span data-ttu-id="5fbf9-104">表示符号编写器，并提供定义文档、序列点、词法范围和变量的方法。</span><span class="sxs-lookup"><span data-stu-id="5fbf9-104">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="5fbf9-105">此接口扩展 [ISymUnmanagedWriter](isymunmanagedwriter-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="5fbf9-105">This interface extends the [ISymUnmanagedWriter](isymunmanagedwriter-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5fbf9-106">方法</span><span class="sxs-lookup"><span data-stu-id="5fbf9-106">Methods</span></span>  
  
|<span data-ttu-id="5fbf9-107">方法</span><span class="sxs-lookup"><span data-stu-id="5fbf9-107">Method</span></span>|<span data-ttu-id="5fbf9-108">说明</span><span class="sxs-lookup"><span data-stu-id="5fbf9-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5fbf9-109">Commit 方法</span><span class="sxs-lookup"><span data-stu-id="5fbf9-109">Commit Method</span></span>](isymunmanagedwriter3-commit-method.md)|<span data-ttu-id="5fbf9-110">将迄今为止写入的更改提交到流。</span><span class="sxs-lookup"><span data-stu-id="5fbf9-110">Commits the changes written so far to the stream.</span></span>|  
|[<span data-ttu-id="5fbf9-111">OpenMethod2 方法</span><span class="sxs-lookup"><span data-stu-id="5fbf9-111">OpenMethod2 Method</span></span>](isymunmanagedwriter3-openmethod2-method.md)|<span data-ttu-id="5fbf9-112">打开方法并在图像中提供其实际节偏移量。</span><span class="sxs-lookup"><span data-stu-id="5fbf9-112">Opens a method and provides its real section offset in the image.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5fbf9-113">要求</span><span class="sxs-lookup"><span data-stu-id="5fbf9-113">Requirements</span></span>  

 <span data-ttu-id="5fbf9-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="5fbf9-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5fbf9-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="5fbf9-115">See also</span></span>

- [<span data-ttu-id="5fbf9-116">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="5fbf9-116">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="5fbf9-117">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="5fbf9-117">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="5fbf9-118">ISymUnmanagedWriter2 接口</span><span class="sxs-lookup"><span data-stu-id="5fbf9-118">ISymUnmanagedWriter2 Interface</span></span>](isymunmanagedwriter2-interface.md)
