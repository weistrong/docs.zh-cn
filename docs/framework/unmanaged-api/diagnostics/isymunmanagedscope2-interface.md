---
description: 了解详细信息： ISymUnmanagedScope2 接口
title: ISymUnmanagedScope2 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope2
helpviewer_keywords:
- ISymUnmanagedScope2 interface [.NET Framework debugging]
ms.assetid: 2ed6a387-ba45-483e-9a1e-b0c69f67998b
topic_type:
- apiref
ms.openlocfilehash: a15094da68b00dbec454b2f6a642ac333f9a34ed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763145"
---
# <a name="isymunmanagedscope2-interface"></a><span data-ttu-id="ac323-103">ISymUnmanagedScope2 接口</span><span class="sxs-lookup"><span data-stu-id="ac323-103">ISymUnmanagedScope2 Interface</span></span>

<span data-ttu-id="ac323-104">表示方法中的词法范围。</span><span class="sxs-lookup"><span data-stu-id="ac323-104">Represents a lexical scope within a method.</span></span> <span data-ttu-id="ac323-105">此接口扩展了 [ISymUnmanagedScope](isymunmanagedscope-interface.md) 接口，其中包含获取有关范围内定义的常量的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="ac323-105">This interface extends the [ISymUnmanagedScope](isymunmanagedscope-interface.md) interface with methods that get information about constants defined within the scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ac323-106">方法</span><span class="sxs-lookup"><span data-stu-id="ac323-106">Methods</span></span>  
  
|<span data-ttu-id="ac323-107">方法</span><span class="sxs-lookup"><span data-stu-id="ac323-107">Method</span></span>|<span data-ttu-id="ac323-108">说明</span><span class="sxs-lookup"><span data-stu-id="ac323-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ac323-109">GetConstantCount 方法</span><span class="sxs-lookup"><span data-stu-id="ac323-109">GetConstantCount Method</span></span>](isymunmanagedscope2-getconstantcount-method.md)|<span data-ttu-id="ac323-110">获取在此范围中定义的常量的计数。</span><span class="sxs-lookup"><span data-stu-id="ac323-110">Gets a count of the constants defined within this scope.</span></span>|  
|[<span data-ttu-id="ac323-111">GetConstants 方法</span><span class="sxs-lookup"><span data-stu-id="ac323-111">GetConstants Method</span></span>](isymunmanagedscope2-getconstants-method.md)|<span data-ttu-id="ac323-112">获取在此范围内定义的局部变量。</span><span class="sxs-lookup"><span data-stu-id="ac323-112">Gets the local constants defined within this scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ac323-113">要求</span><span class="sxs-lookup"><span data-stu-id="ac323-113">Requirements</span></span>  

 <span data-ttu-id="ac323-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="ac323-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac323-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="ac323-115">See also</span></span>

- [<span data-ttu-id="ac323-116">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="ac323-116">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="ac323-117">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="ac323-117">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
