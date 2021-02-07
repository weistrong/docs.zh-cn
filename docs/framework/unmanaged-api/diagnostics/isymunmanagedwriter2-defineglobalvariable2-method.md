---
description: 了解详细信息： ISymUnmanagedWriter2：:D efineGlobalVariable2 方法
title: ISymUnmanagedWriter2::DefineGlobalVariable2 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter2.DefineGlobalVariable2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter2::DefineGlobalVariable2
helpviewer_keywords:
- ISymUnmanagedWriter2::DefineGlobalVariable2 method [.NET Framework debugging]
- DefineGlobalVariable2 method [.NET Framework debugging]
ms.assetid: 04d569d6-a151-4957-9872-f3f694c3e4a9
topic_type:
- apiref
ms.openlocfilehash: 9a33ff8d452419ff103c9f4402620bd28196ae54
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761897"
---
# <a name="isymunmanagedwriter2defineglobalvariable2-method"></a><span data-ttu-id="4b5e1-103">ISymUnmanagedWriter2::DefineGlobalVariable2 方法</span><span class="sxs-lookup"><span data-stu-id="4b5e1-103">ISymUnmanagedWriter2::DefineGlobalVariable2 Method</span></span>

<span data-ttu-id="4b5e1-104">定义单个全局变量。</span><span class="sxs-lookup"><span data-stu-id="4b5e1-104">Defines a single global variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b5e1-105">语法</span><span class="sxs-lookup"><span data-stu-id="4b5e1-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineGlobalVariable2(  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] mdSignature  sigToken,  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4b5e1-106">参数</span><span class="sxs-lookup"><span data-stu-id="4b5e1-106">Parameters</span></span>  

 `name`  
 <span data-ttu-id="4b5e1-107">中全局变量名称。</span><span class="sxs-lookup"><span data-stu-id="4b5e1-107">[in] The global variable name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="4b5e1-108">中全局变量特性。</span><span class="sxs-lookup"><span data-stu-id="4b5e1-108">[in] The global variable attributes.</span></span>  
  
 `sigToken`  
 <span data-ttu-id="4b5e1-109">中签名的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="4b5e1-109">[in] The metadata token of the signature.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="4b5e1-110">中地址类型。</span><span class="sxs-lookup"><span data-stu-id="4b5e1-110">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="4b5e1-111">中参数规范的第一个地址。</span><span class="sxs-lookup"><span data-stu-id="4b5e1-111">[in] The first address for the parameter specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="4b5e1-112">中参数规范的第二个地址。</span><span class="sxs-lookup"><span data-stu-id="4b5e1-112">[in] The second address for the parameter specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="4b5e1-113">中参数规范的第三个地址。</span><span class="sxs-lookup"><span data-stu-id="4b5e1-113">[in] The third address for the parameter specification.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4b5e1-114">返回值</span><span class="sxs-lookup"><span data-stu-id="4b5e1-114">Return Value</span></span>  

 <span data-ttu-id="4b5e1-115">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="4b5e1-115">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4b5e1-116">要求</span><span class="sxs-lookup"><span data-stu-id="4b5e1-116">Requirements</span></span>  

 <span data-ttu-id="4b5e1-117">**标头：** CorSym .idl</span><span class="sxs-lookup"><span data-stu-id="4b5e1-117">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b5e1-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="4b5e1-118">See also</span></span>

- [<span data-ttu-id="4b5e1-119">ISymUnmanagedWriter2 接口</span><span class="sxs-lookup"><span data-stu-id="4b5e1-119">ISymUnmanagedWriter2 Interface</span></span>](isymunmanagedwriter2-interface.md)
- [<span data-ttu-id="4b5e1-120">DefineGlobalVariable 方法</span><span class="sxs-lookup"><span data-stu-id="4b5e1-120">DefineGlobalVariable Method</span></span>](isymunmanagedwriter-defineglobalvariable-method.md)
