---
description: 了解详细信息： ISymUnmanagedWriter：： CloseScope 方法
title: ISymUnmanagedWriter::CloseScope 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.CloseScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::CloseScope
helpviewer_keywords:
- CloseScope method [.NET Framework debugging]
- ISymUnmanagedWriter::CloseScope method [.NET Framework debugging]
ms.assetid: 6dade525-7770-4cb4-bafd-4bb995ad0d87
topic_type:
- apiref
ms.openlocfilehash: bb41e69955632d1e4d86250a63a9f25a7d1ae807
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762547"
---
# <a name="isymunmanagedwriterclosescope-method"></a><span data-ttu-id="0ce4e-103">ISymUnmanagedWriter::CloseScope 方法</span><span class="sxs-lookup"><span data-stu-id="0ce4e-103">ISymUnmanagedWriter::CloseScope Method</span></span>

<span data-ttu-id="0ce4e-104">关闭当前词法范围。</span><span class="sxs-lookup"><span data-stu-id="0ce4e-104">Closes the current lexical scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ce4e-105">语法</span><span class="sxs-lookup"><span data-stu-id="0ce4e-105">Syntax</span></span>  
  
```cpp  
HRESULT CloseScope(  
    [in] ULONG32 endOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0ce4e-106">参数</span><span class="sxs-lookup"><span data-stu-id="0ce4e-106">Parameters</span></span>  

 `endOffset`  
 <span data-ttu-id="0ce4e-107">中词法范围中最后一个指令结束时点的方法开头的偏移量（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="0ce4e-107">[in] The offset from the beginning of the method of the point at the end of the last instruction in the lexical scope, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0ce4e-108">返回值</span><span class="sxs-lookup"><span data-stu-id="0ce4e-108">Return Value</span></span>  

 <span data-ttu-id="0ce4e-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="0ce4e-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0ce4e-110">备注</span><span class="sxs-lookup"><span data-stu-id="0ce4e-110">Remarks</span></span>  

 <span data-ttu-id="0ce4e-111">范围结束后，不能再定义更多变量。</span><span class="sxs-lookup"><span data-stu-id="0ce4e-111">Once a scope is closed, no more variables can be defined within it.</span></span>  
  
 <span data-ttu-id="0ce4e-112">[ISymUnmanagedWriter：： OpenScope](isymunmanagedwriter-openscope-method.md) 返回一个不透明的范围标识符，该标识符可与 [ISymUnmanagedWriter：： SetScopeRange](isymunmanagedwriter-setscoperange-method.md) 一起使用，以便稍后定义作用域的起始和结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="0ce4e-112">[ISymUnmanagedWriter::OpenScope](isymunmanagedwriter-openscope-method.md) returns an opaque scope identifier that can be used with [ISymUnmanagedWriter::SetScopeRange](isymunmanagedwriter-setscoperange-method.md) to later define a scope's starting and ending offset.</span></span> <span data-ttu-id="0ce4e-113">在这种情况下，忽略传递到 `ISymUnmanagedWriter::OpenScope` 和 `ISymUnmanagedWriter::CloseScope` 的偏移量。</span><span class="sxs-lookup"><span data-stu-id="0ce4e-113">In this case, the offsets passed to `ISymUnmanagedWriter::OpenScope` and `ISymUnmanagedWriter::CloseScope` are ignored.</span></span> <span data-ttu-id="0ce4e-114">范围标识符只在当前方法中有效。</span><span class="sxs-lookup"><span data-stu-id="0ce4e-114">Scope identifiers are valid only in the current method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0ce4e-115">要求</span><span class="sxs-lookup"><span data-stu-id="0ce4e-115">Requirements</span></span>  

 <span data-ttu-id="0ce4e-116">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="0ce4e-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ce4e-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="0ce4e-117">See also</span></span>

- [<span data-ttu-id="0ce4e-118">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="0ce4e-118">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
