---
description: 了解详细信息： ISymUnmanagedWriter：:D efineGlobalVariable 方法
title: ISymUnmanagedWriter::DefineGlobalVariable 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineGlobalVariable
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineGlobalVariable
helpviewer_keywords:
- ISymUnmanagedWriter::DefineGlobalVariable method [.NET Framework debugging]
- DefineGlobalVariable method [.NET Framework debugging]
ms.assetid: 843c904a-8176-4d8f-bd47-b4d4c29f4c5c
topic_type:
- apiref
ms.openlocfilehash: 70dccfed054a9ac79baf3f28683edc9a14d3cdf7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762378"
---
# <a name="isymunmanagedwriterdefineglobalvariable-method"></a><span data-ttu-id="380b2-103">ISymUnmanagedWriter::DefineGlobalVariable 方法</span><span class="sxs-lookup"><span data-stu-id="380b2-103">ISymUnmanagedWriter::DefineGlobalVariable Method</span></span>

<span data-ttu-id="380b2-104">定义单个全局变量。</span><span class="sxs-lookup"><span data-stu-id="380b2-104">Defines a single global variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="380b2-105">语法</span><span class="sxs-lookup"><span data-stu-id="380b2-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineGlobalVariable(  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] ULONG32      cSig,  
    [in, size_is(cSig)] unsigned char signature[],  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3);  
```  
  
## <a name="parameters"></a><span data-ttu-id="380b2-106">参数</span><span class="sxs-lookup"><span data-stu-id="380b2-106">Parameters</span></span>  

 `name`  
 <span data-ttu-id="380b2-107">中指向 `WCHAR` 的指针，该指针定义全局变量名称。</span><span class="sxs-lookup"><span data-stu-id="380b2-107">[in] A pointer to a `WCHAR` that defines the global variable name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="380b2-108">中全局变量特性。</span><span class="sxs-lookup"><span data-stu-id="380b2-108">[in] The global variable attributes.</span></span>  
  
 `cSig`  
 <span data-ttu-id="380b2-109">中一个 `ULONG32` ，该值指示缓冲区的大小（以字符为字符） `signature` 。</span><span class="sxs-lookup"><span data-stu-id="380b2-109">[in] A `ULONG32` that indicates the size, in characters, of the `signature` buffer.</span></span>  
  
 `signature`  
 <span data-ttu-id="380b2-110">中全局变量签名。</span><span class="sxs-lookup"><span data-stu-id="380b2-110">[in] The global variable signature.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="380b2-111">中地址类型。</span><span class="sxs-lookup"><span data-stu-id="380b2-111">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="380b2-112">中参数规范的第一个地址。</span><span class="sxs-lookup"><span data-stu-id="380b2-112">[in] The first address for the parameter specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="380b2-113">中参数规范的第二个地址。</span><span class="sxs-lookup"><span data-stu-id="380b2-113">[in] The second address for the parameter specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="380b2-114">中参数规范的第三个地址。</span><span class="sxs-lookup"><span data-stu-id="380b2-114">[in] The third address for the parameter specification.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="380b2-115">返回值</span><span class="sxs-lookup"><span data-stu-id="380b2-115">Return Value</span></span>  

 <span data-ttu-id="380b2-116">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="380b2-116">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="380b2-117">要求</span><span class="sxs-lookup"><span data-stu-id="380b2-117">Requirements</span></span>  

 <span data-ttu-id="380b2-118">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="380b2-118">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="380b2-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="380b2-119">See also</span></span>

- [<span data-ttu-id="380b2-120">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="380b2-120">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="380b2-121">DefineLocalVariable 方法</span><span class="sxs-lookup"><span data-stu-id="380b2-121">DefineLocalVariable Method</span></span>](isymunmanagedwriter-definelocalvariable-method.md)
- [<span data-ttu-id="380b2-122">DefineGlobalVariable2 方法</span><span class="sxs-lookup"><span data-stu-id="380b2-122">DefineGlobalVariable2 Method</span></span>](isymunmanagedwriter2-defineglobalvariable2-method.md)
