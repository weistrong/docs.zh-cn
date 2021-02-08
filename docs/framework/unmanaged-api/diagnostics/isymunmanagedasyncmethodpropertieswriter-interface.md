---
description: 了解详细信息： ISymUnmanagedAsyncMethodPropertiesWriter 接口
title: ISymUnmanagedAsyncMethodPropertiesWriter 接口
ms.date: 03/30/2017
ms.assetid: caa71820-8058-4b6a-93a2-25ee757d92d3
ms.openlocfilehash: 4c8b1bc037485e22160af28b59d751859a157499
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790186"
---
# <a name="isymunmanagedasyncmethodpropertieswriter-interface"></a><span data-ttu-id="a0f27-103">ISymUnmanagedAsyncMethodPropertiesWriter 接口</span><span class="sxs-lookup"><span data-stu-id="a0f27-103">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>

<span data-ttu-id="a0f27-104">允许您为每个方法符号定义可选的异步方法信息。</span><span class="sxs-lookup"><span data-stu-id="a0f27-104">Allows you to define optional async method information for each method symbol.</span></span> <span data-ttu-id="a0f27-105">始终使用打开的方法;也就是说，在对 [OpenMethod 方法](isymunmanagedwriter-openmethod-method.md) 和 [CloseMethod 方法](isymunmanagedwriter-closemethod-method.md)的调用之间。</span><span class="sxs-lookup"><span data-stu-id="a0f27-105">Always use with an opened method; that is, between calls to the [OpenMethod Method](isymunmanagedwriter-openmethod-method.md) and the [CloseMethod Method](isymunmanagedwriter-closemethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0f27-106">语法</span><span class="sxs-lookup"><span data-stu-id="a0f27-106">Syntax</span></span>  
  
```idl  
[object,uuid(FC073774-1739-4232-BD56-A027294BEC15),pointer_default(unique)]interface ISymUnmanagedAsyncMethodPropertiesWriter : IUnknown  
```  
  
## <a name="methods"></a><span data-ttu-id="a0f27-107">方法</span><span class="sxs-lookup"><span data-stu-id="a0f27-107">Methods</span></span>  

 <span data-ttu-id="a0f27-108">此接口包含下列方法：</span><span class="sxs-lookup"><span data-stu-id="a0f27-108">This interface contains the following methods:</span></span>  
  
|<span data-ttu-id="a0f27-109">方法</span><span class="sxs-lookup"><span data-stu-id="a0f27-109">Method</span></span>|<span data-ttu-id="a0f27-110">说明</span><span class="sxs-lookup"><span data-stu-id="a0f27-110">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a0f27-111">DefineAsyncStepInfo 方法</span><span class="sxs-lookup"><span data-stu-id="a0f27-111">DefineAsyncStepInfo Method</span></span>](isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md)|<span data-ttu-id="a0f27-112">在当前方法中定义一组异步等待操作。</span><span class="sxs-lookup"><span data-stu-id="a0f27-112">Define a group of async await operations in the current method.</span></span><br /><br /> <span data-ttu-id="a0f27-113">每个 yield 偏移均与 await 的返回指令匹配，确定潜在的收益率。</span><span class="sxs-lookup"><span data-stu-id="a0f27-113">Each yield offset matches an await's return instruction, identifying a potential yield.</span></span> <span data-ttu-id="a0f27-114">每个 `breakpointMethod` / `breakpointOffset` 对都标识异步操作将恢复到的位置; 它可能采用不同的方法。</span><span class="sxs-lookup"><span data-stu-id="a0f27-114">Each `breakpointMethod`/`breakpointOffset` pair identifies where the asynchronous operation will resume; it may be in a different method.</span></span>|  
|[<span data-ttu-id="a0f27-115">DefineCatchHandlerILOffset 方法</span><span class="sxs-lookup"><span data-stu-id="a0f27-115">DefineCatchHandlerILOffset Method</span></span>](isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md)|<span data-ttu-id="a0f27-116">设置编译器生成的用于包装异步方法的 catch 处理程序的 IL 偏移量。</span><span class="sxs-lookup"><span data-stu-id="a0f27-116">Sets the IL offset for the compiler-generated catch handler that wraps an async method.</span></span><br /><br /> <span data-ttu-id="a0f27-117">调试器使用生成的 catch 的 IL 偏移量来处理 catch，就像它是非用户代码一样，即使它可能出现在用户代码方法中也是如此。</span><span class="sxs-lookup"><span data-stu-id="a0f27-117">The IL offset of the generated catch is used by the debugger to handle the catch as if it were non-user code, even though it may occur in a user code method.</span></span> <span data-ttu-id="a0f27-118">具体而言，它用于响应 **CatchHandlerFound** 异常事件。</span><span class="sxs-lookup"><span data-stu-id="a0f27-118">In particular, it is used in response to a **CatchHandlerFound** exception event.</span></span>|  
|[<span data-ttu-id="a0f27-119">DefineKickoffMethod 方法</span><span class="sxs-lookup"><span data-stu-id="a0f27-119">DefineKickoffMethod Method</span></span>](isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md)|<span data-ttu-id="a0f27-120">设置启动异步操作的启动方法。</span><span class="sxs-lookup"><span data-stu-id="a0f27-120">Sets the starting method that initiates the async operation.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a0f27-121">要求</span><span class="sxs-lookup"><span data-stu-id="a0f27-121">Requirements</span></span>  

 <span data-ttu-id="a0f27-122">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="a0f27-122">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0f27-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="a0f27-123">See also</span></span>

- [<span data-ttu-id="a0f27-124">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="a0f27-124">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
