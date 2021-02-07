---
description: 了解详细信息： ISymUnmanagedWriter：:D efineLocalVariable 方法
title: ISymUnmanagedWriter::DefineLocalVariable 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineLocalVariable
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineLocalVariable
helpviewer_keywords:
- ISymUnmanagedWriter::DefineLocalVariable method [.NET Framework debugging]
- DefineLocalVariable method [.NET Framework debugging]
ms.assetid: 6fab8a58-3883-490f-8b27-64042c90f104
topic_type:
- apiref
ms.openlocfilehash: cd817e3002c2a55fd8bbd7e565283752926f746b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762365"
---
# <a name="isymunmanagedwriterdefinelocalvariable-method"></a><span data-ttu-id="f20ef-103">ISymUnmanagedWriter::DefineLocalVariable 方法</span><span class="sxs-lookup"><span data-stu-id="f20ef-103">ISymUnmanagedWriter::DefineLocalVariable Method</span></span>

<span data-ttu-id="f20ef-104">在当前词法范围内定义单个变量。</span><span class="sxs-lookup"><span data-stu-id="f20ef-104">Defines a single variable in the current lexical scope.</span></span> <span data-ttu-id="f20ef-105">对于在整个范围内具有多个住宅的同名变量，可以多次调用此方法。</span><span class="sxs-lookup"><span data-stu-id="f20ef-105">This method can be called multiple times for a variable of the same name that has multiple homes throughout a scope.</span></span> <span data-ttu-id="f20ef-106">但在这种情况下， `startOffset` 和参数的值 `endOffset` 不能重叠。</span><span class="sxs-lookup"><span data-stu-id="f20ef-106">In this case, however, the values of the `startOffset` and `endOffset` parameters must not overlap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f20ef-107">语法</span><span class="sxs-lookup"><span data-stu-id="f20ef-107">Syntax</span></span>  
  
```cpp  
HRESULT DefineLocalVariable(  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] ULONG32      cSig,  
    [in, size_is(cSig)] unsigned char signature[],  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3,  
    [in] ULONG32      startOffset,  
    [in] ULONG32      endOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f20ef-108">参数</span><span class="sxs-lookup"><span data-stu-id="f20ef-108">Parameters</span></span>  

 `name`  
 <span data-ttu-id="f20ef-109">中指向 `WCHAR` 的指针，该指针定义局部变量的名称。</span><span class="sxs-lookup"><span data-stu-id="f20ef-109">[in] A pointer to a `WCHAR` that defines the local variable name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="f20ef-110">中局部变量特性。</span><span class="sxs-lookup"><span data-stu-id="f20ef-110">[in] The local variable attributes.</span></span>  
  
 `cSig`  
 <span data-ttu-id="f20ef-111">中一个 `ULONG32` ，该值指示缓冲区的大小（以字节为单位） `signature` 。</span><span class="sxs-lookup"><span data-stu-id="f20ef-111">[in] A `ULONG32` that indicates the size, in bytes, of the `signature` buffer.</span></span>  
  
 `signature`  
 <span data-ttu-id="f20ef-112">中局部变量签名。</span><span class="sxs-lookup"><span data-stu-id="f20ef-112">[in] The local variable signature.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="f20ef-113">中地址类型。</span><span class="sxs-lookup"><span data-stu-id="f20ef-113">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="f20ef-114">中参数规范的第一个地址。</span><span class="sxs-lookup"><span data-stu-id="f20ef-114">[in] The first address for the parameter specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="f20ef-115">中参数规范的第二个地址。</span><span class="sxs-lookup"><span data-stu-id="f20ef-115">[in] The second address for the parameter specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="f20ef-116">中参数规范的第三个地址。</span><span class="sxs-lookup"><span data-stu-id="f20ef-116">[in] The third address for the parameter specification.</span></span>  
  
 `startOffset`  
 <span data-ttu-id="f20ef-117">中变量的起始偏移量。</span><span class="sxs-lookup"><span data-stu-id="f20ef-117">[in] The start offset for the variable.</span></span> <span data-ttu-id="f20ef-118">此参数可选。</span><span class="sxs-lookup"><span data-stu-id="f20ef-118">This parameter is optional.</span></span> <span data-ttu-id="f20ef-119">如果为0，则忽略此参数，并在整个范围内定义变量。</span><span class="sxs-lookup"><span data-stu-id="f20ef-119">If it is 0, this parameter is ignored and the variable is defined throughout the entire scope.</span></span> <span data-ttu-id="f20ef-120">如果它是非零值，则该变量将处于当前范围的偏移量内。</span><span class="sxs-lookup"><span data-stu-id="f20ef-120">If it is a nonzero value, the variable falls within the offsets of the current scope.</span></span>  
  
 `endOffset`  
 <span data-ttu-id="f20ef-121">中变量的结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="f20ef-121">[in] The end offset for the variable.</span></span> <span data-ttu-id="f20ef-122">此参数可选。</span><span class="sxs-lookup"><span data-stu-id="f20ef-122">This parameter is optional.</span></span> <span data-ttu-id="f20ef-123">如果为0，则忽略此参数，并在整个范围内定义变量。</span><span class="sxs-lookup"><span data-stu-id="f20ef-123">If it is 0, this parameter is ignored and the variable is defined throughout the entire scope.</span></span> <span data-ttu-id="f20ef-124">如果它是非零值，则该变量将处于当前范围的偏移量内。</span><span class="sxs-lookup"><span data-stu-id="f20ef-124">If it is a nonzero value, the variable falls within the offsets of the current scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f20ef-125">返回值</span><span class="sxs-lookup"><span data-stu-id="f20ef-125">Return Value</span></span>  

 <span data-ttu-id="f20ef-126">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="f20ef-126">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f20ef-127">要求</span><span class="sxs-lookup"><span data-stu-id="f20ef-127">Requirements</span></span>  

 <span data-ttu-id="f20ef-128">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="f20ef-128">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f20ef-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="f20ef-129">See also</span></span>

- [<span data-ttu-id="f20ef-130">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="f20ef-130">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="f20ef-131">DefineGlobalVariable 方法</span><span class="sxs-lookup"><span data-stu-id="f20ef-131">DefineGlobalVariable Method</span></span>](isymunmanagedwriter-defineglobalvariable-method.md)
- [<span data-ttu-id="f20ef-132">DefineLocalVariable2 方法</span><span class="sxs-lookup"><span data-stu-id="f20ef-132">DefineLocalVariable2 Method</span></span>](isymunmanagedwriter2-definelocalvariable2-method.md)
