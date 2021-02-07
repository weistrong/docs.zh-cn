---
description: 了解详细信息： ISymUnmanagedScope 接口
title: ISymUnmanagedScope 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope
helpviewer_keywords:
- ISymUnmanagedScope interface [.NET Framework debugging]
ms.assetid: 3db7a220-cfe9-4810-8ca8-a094bb8e0f5b
topic_type:
- apiref
ms.openlocfilehash: f1175656fb49ee16fd1cd676d08f6ebb76f40c6d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763262"
---
# <a name="isymunmanagedscope-interface"></a><span data-ttu-id="0992e-103">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="0992e-103">ISymUnmanagedScope Interface</span></span>

<span data-ttu-id="0992e-104">表示方法中的词法范围。</span><span class="sxs-lookup"><span data-stu-id="0992e-104">Represents a lexical scope within a method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0992e-105">方法</span><span class="sxs-lookup"><span data-stu-id="0992e-105">Methods</span></span>  
  
|<span data-ttu-id="0992e-106">方法</span><span class="sxs-lookup"><span data-stu-id="0992e-106">Method</span></span>|<span data-ttu-id="0992e-107">说明</span><span class="sxs-lookup"><span data-stu-id="0992e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0992e-108">GetChildren 方法</span><span class="sxs-lookup"><span data-stu-id="0992e-108">GetChildren Method</span></span>](isymunmanagedscope-getchildren-method.md)|<span data-ttu-id="0992e-109">获取此作用域的子级。</span><span class="sxs-lookup"><span data-stu-id="0992e-109">Gets the children of this scope.</span></span>|  
|[<span data-ttu-id="0992e-110">GetEndOffset 方法</span><span class="sxs-lookup"><span data-stu-id="0992e-110">GetEndOffset Method</span></span>](isymunmanagedscope-getendoffset-method.md)|<span data-ttu-id="0992e-111">获取此范围的结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="0992e-111">Gets the end offset for this scope.</span></span>|  
|[<span data-ttu-id="0992e-112">GetLocalCount 方法</span><span class="sxs-lookup"><span data-stu-id="0992e-112">GetLocalCount Method</span></span>](isymunmanagedscope-getlocalcount-method.md)|<span data-ttu-id="0992e-113">获取在此范围内定义的局部变量的计数。</span><span class="sxs-lookup"><span data-stu-id="0992e-113">Gets a count of the local variables defined within this scope.</span></span>|  
|[<span data-ttu-id="0992e-114">GetLocals 方法</span><span class="sxs-lookup"><span data-stu-id="0992e-114">GetLocals Method</span></span>](isymunmanagedscope-getlocals-method.md)|<span data-ttu-id="0992e-115">获取在此范围内定义的局部变量。</span><span class="sxs-lookup"><span data-stu-id="0992e-115">Gets the local variables defined within this scope.</span></span>|  
|[<span data-ttu-id="0992e-116">GetMethod 方法</span><span class="sxs-lookup"><span data-stu-id="0992e-116">GetMethod Method</span></span>](isymunmanagedscope-getmethod-method.md)|<span data-ttu-id="0992e-117">获取包含此范围的方法。</span><span class="sxs-lookup"><span data-stu-id="0992e-117">Gets the method that contains this scope.</span></span>|  
|[<span data-ttu-id="0992e-118">GetNamespaces 方法</span><span class="sxs-lookup"><span data-stu-id="0992e-118">GetNamespaces Method</span></span>](isymunmanagedscope-getnamespaces-method.md)|<span data-ttu-id="0992e-119">获取正在此范围内使用的命名空间。</span><span class="sxs-lookup"><span data-stu-id="0992e-119">Gets the namespaces that are being used within this scope.</span></span>|  
|[<span data-ttu-id="0992e-120">GetParent 方法</span><span class="sxs-lookup"><span data-stu-id="0992e-120">GetParent Method</span></span>](isymunmanagedscope-getparent-method.md)|<span data-ttu-id="0992e-121">获取此范围的父范围。</span><span class="sxs-lookup"><span data-stu-id="0992e-121">Gets the parent scope of this scope.</span></span>|  
|[<span data-ttu-id="0992e-122">GetStartOffset 方法</span><span class="sxs-lookup"><span data-stu-id="0992e-122">GetStartOffset Method</span></span>](isymunmanagedscope-getstartoffset-method.md)|<span data-ttu-id="0992e-123">获取此范围的起始偏移量。</span><span class="sxs-lookup"><span data-stu-id="0992e-123">Gets the start offset for this scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0992e-124">要求</span><span class="sxs-lookup"><span data-stu-id="0992e-124">Requirements</span></span>  

 <span data-ttu-id="0992e-125">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="0992e-125">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0992e-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="0992e-126">See also</span></span>

- [<span data-ttu-id="0992e-127">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="0992e-127">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="0992e-128">ISymUnmanagedScope2 接口</span><span class="sxs-lookup"><span data-stu-id="0992e-128">ISymUnmanagedScope2 Interface</span></span>](isymunmanagedscope2-interface.md)
