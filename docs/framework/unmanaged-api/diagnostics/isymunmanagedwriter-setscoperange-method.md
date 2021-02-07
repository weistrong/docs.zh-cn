---
description: 了解详细信息： ISymUnmanagedWriter：： SetScopeRange 方法
title: ISymUnmanagedWriter::SetScopeRange 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.SetScopeRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::SetScopeRange
helpviewer_keywords:
- SetScopeRange method [.NET Framework debugging]
- ISymUnmanagedWriter::SetScopeRange method [.NET Framework debugging]
ms.assetid: d4d98676-444b-46ca-bfe6-0d827385cd22
topic_type:
- apiref
ms.openlocfilehash: 43cfbeaa0d366b9f2d25068cfa7b91a0fea8ac59
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762053"
---
# <a name="isymunmanagedwritersetscoperange-method"></a><span data-ttu-id="c1a15-103">ISymUnmanagedWriter::SetScopeRange 方法</span><span class="sxs-lookup"><span data-stu-id="c1a15-103">ISymUnmanagedWriter::SetScopeRange Method</span></span>

<span data-ttu-id="c1a15-104">定义指定词法范围的偏移量范围。</span><span class="sxs-lookup"><span data-stu-id="c1a15-104">Defines the offset range for the specified lexical scope.</span></span> <span data-ttu-id="c1a15-105">范围将成为新的当前范围，并推送到作用域的堆栈上。</span><span class="sxs-lookup"><span data-stu-id="c1a15-105">The scope becomes the new current scope and is pushed onto a stack of scopes.</span></span> <span data-ttu-id="c1a15-106">范围必须构成层次结构。</span><span class="sxs-lookup"><span data-stu-id="c1a15-106">Scopes must form a hierarchy.</span></span> <span data-ttu-id="c1a15-107">同级不允许重叠。</span><span class="sxs-lookup"><span data-stu-id="c1a15-107">Siblings are not allowed to overlap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c1a15-108">语法</span><span class="sxs-lookup"><span data-stu-id="c1a15-108">Syntax</span></span>  
  
```cpp  
HRESULT OpenScope(  
    [in] ULONG32  scopeID,  
    [in] ULONG32  startOffset,  
    [in] ULONG32  endOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c1a15-109">参数</span><span class="sxs-lookup"><span data-stu-id="c1a15-109">Parameters</span></span>  

 `scopeId`  
 <span data-ttu-id="c1a15-110">中作用域的作用域标识符。</span><span class="sxs-lookup"><span data-stu-id="c1a15-110">[in] The scope identifier for the scope.</span></span>  
  
 `startOffset`  
 <span data-ttu-id="c1a15-111">中词法范围中从该方法的开头开始的第一个指令的偏移量（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c1a15-111">[in] The offset, in bytes, of the first instruction in the lexical scope from the beginning of the method.</span></span>  
  
 `endOffset`  
 <span data-ttu-id="c1a15-112">中词法范围中从该方法的开头开始的最后一个指令的偏移量（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c1a15-112">[in] The offset, in bytes, of the last instruction in the lexical scope from the beginning of the method.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c1a15-113">返回值</span><span class="sxs-lookup"><span data-stu-id="c1a15-113">Return Value</span></span>  

 <span data-ttu-id="c1a15-114">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="c1a15-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c1a15-115">备注</span><span class="sxs-lookup"><span data-stu-id="c1a15-115">Remarks</span></span>  

 <span data-ttu-id="c1a15-116">[ISymUnmanagedWriter：： OpenScope](isymunmanagedwriter-openscope-method.md) 返回一个不透明的范围标识符，该标识符可与一起用于 `ISymUnmanagedWriter::SetScopeRange` 定义范围的起始和结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="c1a15-116">[ISymUnmanagedWriter::OpenScope](isymunmanagedwriter-openscope-method.md) returns an opaque scope identifier that can be used with `ISymUnmanagedWriter::SetScopeRange` to define a scope's starting and ending offset at a later time.</span></span> <span data-ttu-id="c1a15-117">在这种情况下，将忽略传递到 `ISymUnmanagedWriter::OpenScope` 和 [ISymUnmanagedWriter：： CloseScope](isymunmanagedwriter-closescope-method.md) 的偏移量。</span><span class="sxs-lookup"><span data-stu-id="c1a15-117">In this case, the offsets passed to `ISymUnmanagedWriter::OpenScope` and [ISymUnmanagedWriter::CloseScope](isymunmanagedwriter-closescope-method.md) are ignored.</span></span> <span data-ttu-id="c1a15-118">范围标识符只在当前方法中有效。</span><span class="sxs-lookup"><span data-stu-id="c1a15-118">Scope identifiers are only valid in the current method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c1a15-119">要求</span><span class="sxs-lookup"><span data-stu-id="c1a15-119">Requirements</span></span>  

 <span data-ttu-id="c1a15-120">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="c1a15-120">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1a15-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="c1a15-121">See also</span></span>

- [<span data-ttu-id="c1a15-122">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="c1a15-122">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
