---
description: 了解详细信息： ICorDebugMutableDataTarget：： ContinueStatusChanged 方法
title: ICorDebugMutableDataTarget::ContinueStatusChanged 方法
ms.date: 03/30/2017
ms.assetid: 5a66d3f4-dd16-4d62-9dcc-0eab7041d894
ms.openlocfilehash: 6655d6f1a115b4879c73e356faa8e8785a110078
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722498"
---
# <a name="icordebugmutabledatatargetcontinuestatuschanged-method"></a><span data-ttu-id="a1aad-103">ICorDebugMutableDataTarget::ContinueStatusChanged 方法</span><span class="sxs-lookup"><span data-stu-id="a1aad-103">ICorDebugMutableDataTarget::ContinueStatusChanged Method</span></span>

<span data-ttu-id="a1aad-104">更改指定线程上未完成的调试事件的延续状态。</span><span class="sxs-lookup"><span data-stu-id="a1aad-104">Changes the continuation status for the outstanding debug event on the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1aad-105">语法</span><span class="sxs-lookup"><span data-stu-id="a1aad-105">Syntax</span></span>  
  
```cpp  
HRESULT ContinueStatusChanged(  
   [in] DWORD dwThreadId,  
   [in] CORDB_CONTINUE_STATUS continueStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a1aad-106">参数</span><span class="sxs-lookup"><span data-stu-id="a1aad-106">Parameters</span></span>  

 `dwThreadId`  
 <span data-ttu-id="a1aad-107">由操作系统定义的线程标识符。</span><span class="sxs-lookup"><span data-stu-id="a1aad-107">The operating system-defined thread identifier.</span></span>  
  
 `continueStatus`  
 <span data-ttu-id="a1aad-108">表示新请求的延续状态的 [COREDB_CONTINUE_STATUS](../common-data-types-unmanaged-api-reference.md) 值。</span><span class="sxs-lookup"><span data-stu-id="a1aad-108">A [COREDB_CONTINUE_STATUS](../common-data-types-unmanaged-api-reference.md) value that represents the new requested continuation status.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a1aad-109">备注</span><span class="sxs-lookup"><span data-stu-id="a1aad-109">Remarks</span></span>  

 <span data-ttu-id="a1aad-110">当调试器调用需要以不同于通常处理方式的方式处理当前的调试事件的 ICorDebug 方法时，该调试器将调用 `ContinueStatusChanged` 方法。</span><span class="sxs-lookup"><span data-stu-id="a1aad-110">The debugger calls the `ContinueStatusChanged` method when it calls an ICorDebug method that requires the current debug event to be handled in a way that is potentially different from the way in which it normally would be handled.</span></span> <span data-ttu-id="a1aad-111">例如，如果存在未处理异常，并且调试器请求会取消此异常的操作（例如 [ICorDebugILFrame::SetIP](icordebugilframe-setip-method.md) 或 `FuncEval`），则此 API 将用于请求取消此异常。</span><span class="sxs-lookup"><span data-stu-id="a1aad-111">For example, if there is an outstanding exception, and the debugger requests an operation that would cancel the exception (such as [ICorDebugILFrame::SetIP](icordebugilframe-setip-method.md) or `FuncEval`), this API is used to request that the exception be cancelled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a1aad-112">要求</span><span class="sxs-lookup"><span data-stu-id="a1aad-112">Requirements</span></span>  

 <span data-ttu-id="a1aad-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a1aad-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1aad-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a1aad-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a1aad-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a1aad-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a1aad-116">**.NET Framework 版本：**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1aad-116">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1aad-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="a1aad-117">See also</span></span>

- [<span data-ttu-id="a1aad-118">ICorDebugMutableDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="a1aad-118">ICorDebugMutableDataTarget Interface</span></span>](icordebugmutabledatatarget-interface.md)
- [<span data-ttu-id="a1aad-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="a1aad-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
