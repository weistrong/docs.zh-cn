---
description: 了解详细信息： ICorDebugManagedCallback3：： CustomNotification 方法
title: ICorDebugManagedCallback3::CustomNotification 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback3.CustomNotification Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback3::CustomNotification
helpviewer_keywords:
- ICorDebugManagedCallback3::CustomNotification method [.NET Framework debugging]
- CustomNotification method [.NET Framework debugging]
ms.assetid: 5e5422ac-afa1-403d-a894-2d7348673e38
topic_type:
- apiref
ms.openlocfilehash: 18210e9c65afa0655374fb038d30516cfed02052
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691713"
---
# <a name="icordebugmanagedcallback3customnotification-method"></a><span data-ttu-id="1391a-103">ICorDebugManagedCallback3::CustomNotification 方法</span><span class="sxs-lookup"><span data-stu-id="1391a-103">ICorDebugManagedCallback3::CustomNotification Method</span></span>

<span data-ttu-id="1391a-104">指示已引发自定义调试器通知。</span><span class="sxs-lookup"><span data-stu-id="1391a-104">Indicates that a custom debugger notification has been raised.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1391a-105">语法</span><span class="sxs-lookup"><span data-stu-id="1391a-105">Syntax</span></span>  
  
```cpp  
HRESULT CustomNotification(ICorDebugThread *    pThread,  
                           ICorDebugAppDomain * pAppDomain);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1391a-106">参数</span><span class="sxs-lookup"><span data-stu-id="1391a-106">Parameters</span></span>  

 `pThread`  
 <span data-ttu-id="1391a-107">中指向引发通知的线程的指针。</span><span class="sxs-lookup"><span data-stu-id="1391a-107">[in] A pointer to the thread that raised the notification.</span></span>  
  
 `pAppDomain`  
 <span data-ttu-id="1391a-108">中一个指针，指向包含引发通知的线程的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="1391a-108">[in] A pointer to the application domain that contains the thread that raised the notification.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1391a-109">返回值</span><span class="sxs-lookup"><span data-stu-id="1391a-109">Return Value</span></span>  

 <span data-ttu-id="1391a-110">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="1391a-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="1391a-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1391a-111">HRESULT</span></span>|<span data-ttu-id="1391a-112">说明</span><span class="sxs-lookup"><span data-stu-id="1391a-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1391a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1391a-113">S_OK</span></span>|<span data-ttu-id="1391a-114">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="1391a-114">The method completed successfully.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="1391a-115">例外</span><span class="sxs-lookup"><span data-stu-id="1391a-115">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1391a-116">备注</span><span class="sxs-lookup"><span data-stu-id="1391a-116">Remarks</span></span>  

 <span data-ttu-id="1391a-117">对 [ICorDebugThread4：： GetCurrentCustomDebuggerNotification](icordebugthread4-getcurrentcustomdebuggernotification-method.md) 方法的后续调用将检索传递到该方法的线程对象 <xref:System.Diagnostics.Debugger.NotifyOfCrossThreadDependency%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="1391a-117">A subsequent call to the [ICorDebugThread4::GetCurrentCustomDebuggerNotification](icordebugthread4-getcurrentcustomdebuggernotification-method.md) method retrieves the thread object that was passed to the <xref:System.Diagnostics.Debugger.NotifyOfCrossThreadDependency%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="1391a-118">线程对象的类型必须以前已通过调用 [ICorDebugProcess3：： SetEnableCustomNotification](icordebugprocess3-setenablecustomnotification-method.md) 方法启用。</span><span class="sxs-lookup"><span data-stu-id="1391a-118">The thread object's type must have been previously enabled by calling the [ICorDebugProcess3::SetEnableCustomNotification](icordebugprocess3-setenablecustomnotification-method.md) method.</span></span> <span data-ttu-id="1391a-119">调试器可以从 thread 对象的字段中读取特定于类型的参数，并可以将响应存储在字段中。</span><span class="sxs-lookup"><span data-stu-id="1391a-119">The debugger can read type-specific parameters from the fields of the thread object, and can store responses into fields.</span></span>  
  
 <span data-ttu-id="1391a-120">[ICorDebug](icordebug-interface.md)接口不对通知类型或其内容施加任何策略，并且通知的语义严格地是调试器、应用程序和 .NET Framework 之间的协定。</span><span class="sxs-lookup"><span data-stu-id="1391a-120">The [ICorDebug](icordebug-interface.md) interface imposes no policy on the types of notifications or their contents, and the semantics of the notifications are strictly a contract between debuggers, applications, and the .NET Framework.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1391a-121">要求</span><span class="sxs-lookup"><span data-stu-id="1391a-121">Requirements</span></span>  

 <span data-ttu-id="1391a-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1391a-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1391a-123">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1391a-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1391a-124">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1391a-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1391a-125">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1391a-125">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1391a-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="1391a-126">See also</span></span>

- [<span data-ttu-id="1391a-127">ICorDebugManagedCallback3 接口</span><span class="sxs-lookup"><span data-stu-id="1391a-127">ICorDebugManagedCallback3 Interface</span></span>](icordebugmanagedcallback3-interface.md)
- [<span data-ttu-id="1391a-128">调试接口</span><span class="sxs-lookup"><span data-stu-id="1391a-128">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="1391a-129">调试</span><span class="sxs-lookup"><span data-stu-id="1391a-129">Debugging</span></span>](index.md)
