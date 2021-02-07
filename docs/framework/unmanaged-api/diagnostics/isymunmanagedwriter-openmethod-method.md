---
description: 了解详细信息： ISymUnmanagedWriter：： OpenMethod 方法
title: ISymUnmanagedWriter::OpenMethod 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.OpenMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::OpenMethod
helpviewer_keywords:
- ISymUnmanagedWriter::OpenMethod method [.NET Framework debugging]
- OpenMethod method [.NET Framework debugging]
ms.assetid: fb90cb7f-af88-45e8-a99f-80a0bbddb08b
topic_type:
- apiref
ms.openlocfilehash: 2cf7e6bf7c632449c25a2b49c7658fa7b1cc287e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762222"
---
# <a name="isymunmanagedwriteropenmethod-method"></a><span data-ttu-id="c4755-103">ISymUnmanagedWriter::OpenMethod 方法</span><span class="sxs-lookup"><span data-stu-id="c4755-103">ISymUnmanagedWriter::OpenMethod Method</span></span>

<span data-ttu-id="c4755-104">打开要在其中发出符号信息的方法。</span><span class="sxs-lookup"><span data-stu-id="c4755-104">Opens a method into which symbol information is emitted.</span></span> <span data-ttu-id="c4755-105">给定方法将成为定义序列点、参数和词法范围的调用的当前方法。</span><span class="sxs-lookup"><span data-stu-id="c4755-105">The given method becomes the current method for calls to define sequence points, parameters, and lexical scopes.</span></span> <span data-ttu-id="c4755-106">围绕整个方法，存在一个隐式词法范围。</span><span class="sxs-lookup"><span data-stu-id="c4755-106">There is an implicit lexical scope around the entire method.</span></span> <span data-ttu-id="c4755-107">重新打开先前关闭的方法将会清除以前为该方法定义的所有符号。</span><span class="sxs-lookup"><span data-stu-id="c4755-107">Reopening a method that was previously closed erases any previously defined symbols for that method.</span></span> <span data-ttu-id="c4755-108">一次只能有一个 open 方法。</span><span class="sxs-lookup"><span data-stu-id="c4755-108">There can be only one open method at a time.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4755-109">语法</span><span class="sxs-lookup"><span data-stu-id="c4755-109">Syntax</span></span>  
  
```cpp  
HRESULT OpenMethod(  
    [in] mdMethodDef method);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c4755-110">参数</span><span class="sxs-lookup"><span data-stu-id="c4755-110">Parameters</span></span>  

 `method`  
 <span data-ttu-id="c4755-111">中要打开的方法的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="c4755-111">[in] The metadata token for the method to be opened.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c4755-112">返回值</span><span class="sxs-lookup"><span data-stu-id="c4755-112">Return Value</span></span>  

 <span data-ttu-id="c4755-113">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="c4755-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4755-114">要求</span><span class="sxs-lookup"><span data-stu-id="c4755-114">Requirements</span></span>  

 <span data-ttu-id="c4755-115">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="c4755-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4755-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="c4755-116">See also</span></span>

- [<span data-ttu-id="c4755-117">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="c4755-117">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="c4755-118">CloseMethod 方法</span><span class="sxs-lookup"><span data-stu-id="c4755-118">CloseMethod Method</span></span>](isymunmanagedwriter-closemethod-method.md)
- [<span data-ttu-id="c4755-119">OpenMethod2 方法</span><span class="sxs-lookup"><span data-stu-id="c4755-119">OpenMethod2 Method</span></span>](isymunmanagedwriter3-openmethod2-method.md)
