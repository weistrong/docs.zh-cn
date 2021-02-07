---
description: 了解详细信息： ISymUnmanagedAsyncMethodPropertiesWriter：:D efineCatchHandlerILOffset 方法
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset 方法
ms.date: 03/30/2017
ms.assetid: 92af7896-2201-408d-8b1b-23e28001eeac
ms.openlocfilehash: fcb2c6efa7ea83252a46a9b08cdfa7b2c14f09d1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737787"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinecatchhandleriloffset-method"></a><span data-ttu-id="86a4d-103">ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset 方法</span><span class="sxs-lookup"><span data-stu-id="86a4d-103">ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset Method</span></span>

<span data-ttu-id="86a4d-104">设置编译器生成的用于包装异步方法的 catch 处理程序的 IL 偏移量。</span><span class="sxs-lookup"><span data-stu-id="86a4d-104">Sets the IL offset for the compiler-generated catch handler that wraps an async method.</span></span>  
  
 <span data-ttu-id="86a4d-105">调试器使用生成的 catch 的 IL 偏移量来处理 catch，就像它是非用户代码，即使它可能出现在用户代码方法中也是如此。</span><span class="sxs-lookup"><span data-stu-id="86a4d-105">The IL offset of the generated catch is used by the debugger to handle the catch as if it were non-user code even though it might occur in a user code method.</span></span> <span data-ttu-id="86a4d-106">具体而言，它用于响应 **CatchHandlerFound** 异常事件。</span><span class="sxs-lookup"><span data-stu-id="86a4d-106">In particular, it is used in response to a **CatchHandlerFound** exception event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86a4d-107">语法</span><span class="sxs-lookup"><span data-stu-id="86a4d-107">Syntax</span></span>  
  
```idl  
HRESULT DefineCatchHandlerILOffset(    [in] ULONG32 catchHandlerOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="86a4d-108">参数</span><span class="sxs-lookup"><span data-stu-id="86a4d-108">Parameters</span></span>  
  
|<span data-ttu-id="86a4d-109">参数</span><span class="sxs-lookup"><span data-stu-id="86a4d-109">Parameter</span></span>|<span data-ttu-id="86a4d-110">说明</span><span class="sxs-lookup"><span data-stu-id="86a4d-110">Description</span></span>|  
|---------------|-----------------|  
|`catchHandlerOffset`||  
  
## <a name="return-value"></a><span data-ttu-id="86a4d-111">返回值</span><span class="sxs-lookup"><span data-stu-id="86a4d-111">Return Value</span></span>  

 <span data-ttu-id="86a4d-112">返回 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="86a4d-112">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86a4d-113">要求</span><span class="sxs-lookup"><span data-stu-id="86a4d-113">Requirements</span></span>  

 <span data-ttu-id="86a4d-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="86a4d-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86a4d-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="86a4d-115">See also</span></span>

- [<span data-ttu-id="86a4d-116">ISymUnmanagedAsyncMethodPropertiesWriter 接口</span><span class="sxs-lookup"><span data-stu-id="86a4d-116">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](isymunmanagedasyncmethodpropertieswriter-interface.md)
