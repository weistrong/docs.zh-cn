---
description: 了解详细信息： ISymUnmanagedWriter：:D efineField 方法
title: ISymUnmanagedWriter::DefineField 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineField
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineField
helpviewer_keywords:
- ISymUnmanagedWriter::DefineField method [.NET Framework debugging]
- DefineField method, ISymUnmanagedWriter interface [.NET Framework debugging]
ms.assetid: c6a1f797-dbf4-40f5-ab99-d9b4bfb26148
topic_type:
- apiref
ms.openlocfilehash: f5bb47d4691780d94baf50cc9ceb3c14b1fa16ec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762391"
---
# <a name="isymunmanagedwriterdefinefield-method"></a><span data-ttu-id="7f559-103">ISymUnmanagedWriter::DefineField 方法</span><span class="sxs-lookup"><span data-stu-id="7f559-103">ISymUnmanagedWriter::DefineField Method</span></span>

<span data-ttu-id="7f559-104">定义不在方法中的单个变量。</span><span class="sxs-lookup"><span data-stu-id="7f559-104">Defines a single variable that is not within a method.</span></span> <span data-ttu-id="7f559-105">此方法用于类中的某些字段、位域等。</span><span class="sxs-lookup"><span data-stu-id="7f559-105">This method is used for certain fields in classes, bit fields, and so on.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f559-106">语法</span><span class="sxs-lookup"><span data-stu-id="7f559-106">Syntax</span></span>  
  
```cpp  
HRESULT DefineField(  
    [in] mdTypeDef    parent,  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] ULONG32      cSig,  
    [in, size_is(cSig)] unsigned char signature[],  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7f559-107">参数</span><span class="sxs-lookup"><span data-stu-id="7f559-107">Parameters</span></span>  

 `parent`  
 <span data-ttu-id="7f559-108">中元数据类型或方法标记。</span><span class="sxs-lookup"><span data-stu-id="7f559-108">[in] The metadata type or method token.</span></span>  
  
 `name`  
 <span data-ttu-id="7f559-109">中字段名称。</span><span class="sxs-lookup"><span data-stu-id="7f559-109">[in] The field name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="7f559-110">中字段特性。</span><span class="sxs-lookup"><span data-stu-id="7f559-110">[in] The field attributes.</span></span>  
  
 `cSig`  
 <span data-ttu-id="7f559-111">中一个 `ULONG32` ，它是包含字段签名所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="7f559-111">[in] A `ULONG32` that is the size, in characters, of the buffer required to contain the field signature.</span></span>  
  
 `signature`  
 <span data-ttu-id="7f559-112">中字段签名的数组。</span><span class="sxs-lookup"><span data-stu-id="7f559-112">[in] The array of field signatures.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="7f559-113">中地址类型。</span><span class="sxs-lookup"><span data-stu-id="7f559-113">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="7f559-114">中字段规范的第一个地址。</span><span class="sxs-lookup"><span data-stu-id="7f559-114">[in] The first address for the field specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="7f559-115">中字段规格的第二个地址。</span><span class="sxs-lookup"><span data-stu-id="7f559-115">[in] The second address for the field specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="7f559-116">中字段规格的第三个地址。</span><span class="sxs-lookup"><span data-stu-id="7f559-116">[in] The third address for the field specification.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7f559-117">返回值</span><span class="sxs-lookup"><span data-stu-id="7f559-117">Return Value</span></span>  

 <span data-ttu-id="7f559-118">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="7f559-118">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f559-119">要求</span><span class="sxs-lookup"><span data-stu-id="7f559-119">Requirements</span></span>  

 <span data-ttu-id="7f559-120">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="7f559-120">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f559-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="7f559-121">See also</span></span>

- [<span data-ttu-id="7f559-122">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="7f559-122">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
