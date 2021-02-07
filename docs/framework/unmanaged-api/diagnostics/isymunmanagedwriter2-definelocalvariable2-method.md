---
description: 了解详细信息： ISymUnmanagedWriter2：:D efineLocalVariable2 方法
title: ISymUnmanagedWriter2::DefineLocalVariable2 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter2.DefineLocalVariable2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter2::DefineLocalVariable2
helpviewer_keywords:
- ISymUnmanagedWriter2::DefineLocalVariable2 method [.NET Framework debugging]
- DefineLocalVariable2 method [.NET Framework debugging]
ms.assetid: e774eefe-858c-4362-8d2d-28ebf2ba1a24
topic_type:
- apiref
ms.openlocfilehash: 169a086b8420b5dbe20af8e16b21d5b41a958ead
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761806"
---
# <a name="isymunmanagedwriter2definelocalvariable2-method"></a><span data-ttu-id="b5b75-103">ISymUnmanagedWriter2::DefineLocalVariable2 方法</span><span class="sxs-lookup"><span data-stu-id="b5b75-103">ISymUnmanagedWriter2::DefineLocalVariable2 Method</span></span>

<span data-ttu-id="b5b75-104">在当前词法范围内定义单个变量。</span><span class="sxs-lookup"><span data-stu-id="b5b75-104">Defines a single variable in the current lexical scope.</span></span> <span data-ttu-id="b5b75-105">对于在整个范围内具有多个住宅的同名变量，可以多次调用此方法。</span><span class="sxs-lookup"><span data-stu-id="b5b75-105">This method can be called multiple times for a variable of the same name that has multiple homes throughout a scope.</span></span> <span data-ttu-id="b5b75-106">但在这种情况下， `startOffset` 和参数的值 `endOffset` 不能重叠。</span><span class="sxs-lookup"><span data-stu-id="b5b75-106">In this case, however, the values of the `startOffset` and `endOffset` parameters must not overlap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b5b75-107">语法</span><span class="sxs-lookup"><span data-stu-id="b5b75-107">Syntax</span></span>  
  
```cpp  
HRESULT DefineLocalVariable2(  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] mdSignature  sigToken,  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3,  
    [in] ULONG32      startOffset,  
    [in] ULONG32      endOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b5b75-108">参数</span><span class="sxs-lookup"><span data-stu-id="b5b75-108">Parameters</span></span>  

 `name`  
 <span data-ttu-id="b5b75-109">中局部变量名称。</span><span class="sxs-lookup"><span data-stu-id="b5b75-109">[in] The local variable name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="b5b75-110">中局部变量特性。</span><span class="sxs-lookup"><span data-stu-id="b5b75-110">[in] The local variable attributes.</span></span>  
  
 `sigToken`  
 <span data-ttu-id="b5b75-111">中签名的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="b5b75-111">[in] The metadata token of the signature.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="b5b75-112">中地址类型。</span><span class="sxs-lookup"><span data-stu-id="b5b75-112">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="b5b75-113">中参数规范的第一个地址。</span><span class="sxs-lookup"><span data-stu-id="b5b75-113">[in] The first address for the parameter specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="b5b75-114">中参数规范的第二个地址。</span><span class="sxs-lookup"><span data-stu-id="b5b75-114">[in] The second address for the parameter specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="b5b75-115">中参数规范的第三个地址。</span><span class="sxs-lookup"><span data-stu-id="b5b75-115">[in] The third address for the parameter specification.</span></span>  
  
 `startOffset`  
 <span data-ttu-id="b5b75-116">中变量的起始偏移量。</span><span class="sxs-lookup"><span data-stu-id="b5b75-116">[in] The start offset for the variable.</span></span> <span data-ttu-id="b5b75-117">此参数可选。</span><span class="sxs-lookup"><span data-stu-id="b5b75-117">This parameter is optional.</span></span> <span data-ttu-id="b5b75-118">如果为0，则忽略此参数，并在整个范围内定义变量。</span><span class="sxs-lookup"><span data-stu-id="b5b75-118">If it is 0, this parameter is ignored and the variable is defined throughout the entire scope.</span></span> <span data-ttu-id="b5b75-119">如果它是非零值，则该变量将处于当前范围的偏移量内。</span><span class="sxs-lookup"><span data-stu-id="b5b75-119">If it is a nonzero value, the variable falls within the offsets of the current scope.</span></span>  
  
 `endOffset`  
 <span data-ttu-id="b5b75-120">中变量的结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="b5b75-120">[in] The end offset for the variable.</span></span> <span data-ttu-id="b5b75-121">此参数可选。</span><span class="sxs-lookup"><span data-stu-id="b5b75-121">This parameter is optional.</span></span> <span data-ttu-id="b5b75-122">如果为0，则忽略此参数，并在整个范围内定义变量。</span><span class="sxs-lookup"><span data-stu-id="b5b75-122">If it is 0, this parameter is ignored and the variable is defined throughout the entire scope.</span></span> <span data-ttu-id="b5b75-123">如果它是非零值，则该变量将处于当前范围的偏移量内。</span><span class="sxs-lookup"><span data-stu-id="b5b75-123">If it is a nonzero value, the variable falls within the offsets of the current scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b5b75-124">返回值</span><span class="sxs-lookup"><span data-stu-id="b5b75-124">Return Value</span></span>  

 <span data-ttu-id="b5b75-125">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="b5b75-125">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b5b75-126">要求</span><span class="sxs-lookup"><span data-stu-id="b5b75-126">Requirements</span></span>  

 <span data-ttu-id="b5b75-127">**标头：** CorSym .idl</span><span class="sxs-lookup"><span data-stu-id="b5b75-127">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5b75-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="b5b75-128">See also</span></span>

- [<span data-ttu-id="b5b75-129">ISymUnmanagedWriter2 接口</span><span class="sxs-lookup"><span data-stu-id="b5b75-129">ISymUnmanagedWriter2 Interface</span></span>](isymunmanagedwriter2-interface.md)
- [<span data-ttu-id="b5b75-130">DefineLocalVariable 方法</span><span class="sxs-lookup"><span data-stu-id="b5b75-130">DefineLocalVariable Method</span></span>](isymunmanagedwriter-definelocalvariable-method.md)
