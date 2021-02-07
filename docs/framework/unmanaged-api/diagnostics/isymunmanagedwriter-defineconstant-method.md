---
description: 了解详细信息： ISymUnmanagedWriter：:D efineConstant 方法
title: ISymUnmanagedWriter::DefineConstant 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineConstant
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineConstant
helpviewer_keywords:
- DefineConstant method [.NET Framework debugging]
- ISymUnmanagedWriter::DefineConstant method [.NET Framework debugging]
ms.assetid: 9e986986-2223-4d5f-b040-85d716146924
topic_type:
- apiref
ms.openlocfilehash: 4c3fd3986d42061272406150422f037236c4b9bf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762521"
---
# <a name="isymunmanagedwriterdefineconstant-method"></a><span data-ttu-id="0b157-103">ISymUnmanagedWriter::DefineConstant 方法</span><span class="sxs-lookup"><span data-stu-id="0b157-103">ISymUnmanagedWriter::DefineConstant Method</span></span>

<span data-ttu-id="0b157-104">定义常数值的名称。</span><span class="sxs-lookup"><span data-stu-id="0b157-104">Defines a name for a constant value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b157-105">语法</span><span class="sxs-lookup"><span data-stu-id="0b157-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineConstant(  
    [in] const WCHAR *name,  
    [in] VARIANT value,  
    [in] ULONG32 cSig,  
    [in, size_is(cSig)] unsigned char signature[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0b157-106">参数</span><span class="sxs-lookup"><span data-stu-id="0b157-106">Parameters</span></span>  

 `name`  
 <span data-ttu-id="0b157-107">中一个指针，指向用于 `WCHAR` 定义常量名称的。</span><span class="sxs-lookup"><span data-stu-id="0b157-107">[in] A pointer to a `WCHAR` that defines the constant name.</span></span>  
  
 `value`  
 <span data-ttu-id="0b157-108">中常量的值。</span><span class="sxs-lookup"><span data-stu-id="0b157-108">[in] The value of the constant.</span></span>  
  
 `cSig`  
 <span data-ttu-id="0b157-109">[in] `signature` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="0b157-109">[in] The size of the `signature` array.</span></span>  
  
 `signature`  
 <span data-ttu-id="0b157-110">中常数的类型签名。</span><span class="sxs-lookup"><span data-stu-id="0b157-110">[in] The type signature for the constant.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0b157-111">返回值</span><span class="sxs-lookup"><span data-stu-id="0b157-111">Return Value</span></span>  

 <span data-ttu-id="0b157-112">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="0b157-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0b157-113">要求</span><span class="sxs-lookup"><span data-stu-id="0b157-113">Requirements</span></span>  

 <span data-ttu-id="0b157-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="0b157-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b157-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="0b157-115">See also</span></span>

- [<span data-ttu-id="0b157-116">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="0b157-116">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="0b157-117">DefineConstant2 方法</span><span class="sxs-lookup"><span data-stu-id="0b157-117">DefineConstant2 Method</span></span>](isymunmanagedwriter2-defineconstant2-method.md)
