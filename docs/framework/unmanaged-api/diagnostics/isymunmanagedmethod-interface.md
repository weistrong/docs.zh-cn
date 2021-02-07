---
description: 了解详细信息： ISymUnmanagedMethod 接口
title: ISymUnmanagedMethod 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod
helpviewer_keywords:
- ISymUnmanagedMethod interface [.NET Framework debugging]
ms.assetid: f204d74c-cc79-4092-83bb-60654be95649
topic_type:
- apiref
ms.openlocfilehash: 18f87784a959ddc62415592e51d1971ea10f90bf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709953"
---
# <a name="isymunmanagedmethod-interface"></a><span data-ttu-id="0f851-103">ISymUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="0f851-103">ISymUnmanagedMethod Interface</span></span>

<span data-ttu-id="0f851-104">表示符号存储区中的方法。</span><span class="sxs-lookup"><span data-stu-id="0f851-104">Represents a method within the symbol store.</span></span> <span data-ttu-id="0f851-105">此接口仅提供对方法的符号相关属性的访问，而不提供与类型相关的属性的访问。</span><span class="sxs-lookup"><span data-stu-id="0f851-105">This interface provides access to only the symbol-related attributes of a method, instead of the type-related attributes.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0f851-106">方法</span><span class="sxs-lookup"><span data-stu-id="0f851-106">Methods</span></span>  
  
|<span data-ttu-id="0f851-107">方法</span><span class="sxs-lookup"><span data-stu-id="0f851-107">Method</span></span>|<span data-ttu-id="0f851-108">说明</span><span class="sxs-lookup"><span data-stu-id="0f851-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0f851-109">GetNamespace 方法</span><span class="sxs-lookup"><span data-stu-id="0f851-109">GetNamespace Method</span></span>](isymunmanagedmethod-getnamespace-method.md)|<span data-ttu-id="0f851-110">获取在其中定义此方法的命名空间。</span><span class="sxs-lookup"><span data-stu-id="0f851-110">Gets the namespace within which this method is defined.</span></span>|  
|[<span data-ttu-id="0f851-111">GetOffset 方法</span><span class="sxs-lookup"><span data-stu-id="0f851-111">GetOffset Method</span></span>](isymunmanagedmethod-getoffset-method.md)|<span data-ttu-id="0f851-112">返回此方法内的偏移量，该偏移量对应于文档中的给定位置。</span><span class="sxs-lookup"><span data-stu-id="0f851-112">Returns the offset within this method that corresponds to a given position within a document.</span></span>|  
|[<span data-ttu-id="0f851-113">GetParameters 方法</span><span class="sxs-lookup"><span data-stu-id="0f851-113">GetParameters Method</span></span>](isymunmanagedmethod-getparameters-method.md)|<span data-ttu-id="0f851-114">获取此方法的参数。</span><span class="sxs-lookup"><span data-stu-id="0f851-114">Gets the parameters for this method.</span></span>|  
|[<span data-ttu-id="0f851-115">GetRanges 方法</span><span class="sxs-lookup"><span data-stu-id="0f851-115">GetRanges Method</span></span>](isymunmanagedmethod-getranges-method.md)|<span data-ttu-id="0f851-116">给定文档中的某个位置后，将返回与 Microsoft 中间语言 (MSIL 范围对应的起始和结束偏移量对的数组，) 该位置涵盖在此方法中。</span><span class="sxs-lookup"><span data-stu-id="0f851-116">Given a position in a document, returns an array of start and end offset pairs that correspond to the ranges of Microsoft intermediate language (MSIL) that the position covers within this method.</span></span>|  
|[<span data-ttu-id="0f851-117">GetRootScope 方法</span><span class="sxs-lookup"><span data-stu-id="0f851-117">GetRootScope Method</span></span>](isymunmanagedmethod-getrootscope-method.md)|<span data-ttu-id="0f851-118">获取此方法内的根词法范围。</span><span class="sxs-lookup"><span data-stu-id="0f851-118">Gets the root lexical scope within this method.</span></span> <span data-ttu-id="0f851-119">此范围包括整个方法。</span><span class="sxs-lookup"><span data-stu-id="0f851-119">This scope encloses the entire method.</span></span>|  
|[<span data-ttu-id="0f851-120">GetScopeFromOffset 方法</span><span class="sxs-lookup"><span data-stu-id="0f851-120">GetScopeFromOffset Method</span></span>](isymunmanagedmethod-getscopefromoffset-method.md)|<span data-ttu-id="0f851-121">获取此方法内包含给定偏移量的最封闭的词法范围。</span><span class="sxs-lookup"><span data-stu-id="0f851-121">Gets the most enclosing lexical scope within this method that encloses the given offset.</span></span>|  
|[<span data-ttu-id="0f851-122">GetSequencePointCount 方法</span><span class="sxs-lookup"><span data-stu-id="0f851-122">GetSequencePointCount Method</span></span>](isymunmanagedmethod-getsequencepointcount-method.md)|<span data-ttu-id="0f851-123">获取此方法中序列点的计数。</span><span class="sxs-lookup"><span data-stu-id="0f851-123">Gets the count of sequence points within this method.</span></span>|  
|[<span data-ttu-id="0f851-124">GetSequencePoints 方法</span><span class="sxs-lookup"><span data-stu-id="0f851-124">GetSequencePoints Method</span></span>](isymunmanagedmethod-getsequencepoints-method.md)|<span data-ttu-id="0f851-125">获取此方法中的所有序列点。</span><span class="sxs-lookup"><span data-stu-id="0f851-125">Gets all the sequence points within this method.</span></span>|  
|[<span data-ttu-id="0f851-126">GetSourceStartEnd 方法</span><span class="sxs-lookup"><span data-stu-id="0f851-126">GetSourceStartEnd Method</span></span>](isymunmanagedmethod-getsourcestartend-method.md)|<span data-ttu-id="0f851-127">获取此方法的源的起始和结束文档位置。</span><span class="sxs-lookup"><span data-stu-id="0f851-127">Gets the start and end document positions for the source of this method.</span></span>|  
|[<span data-ttu-id="0f851-128">GetToken 方法</span><span class="sxs-lookup"><span data-stu-id="0f851-128">GetToken Method</span></span>](isymunmanagedmethod-gettoken-method.md)|<span data-ttu-id="0f851-129">返回此方法的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="0f851-129">Returns the metadata token for this method.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0f851-130">要求</span><span class="sxs-lookup"><span data-stu-id="0f851-130">Requirements</span></span>  

 <span data-ttu-id="0f851-131">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="0f851-131">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f851-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="0f851-132">See also</span></span>

- [<span data-ttu-id="0f851-133">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="0f851-133">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
