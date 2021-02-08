---
description: 了解详细信息： ICorDebugManagedCallback：： ExitThread 方法
title: ICorDebugManagedCallback::ExitThread 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.ExitThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::ExitThread
helpviewer_keywords:
- ExitThread method [.NET Framework debugging]
- ICorDebugManagedCallback::ExitThread method [.NET Framework debugging]
ms.assetid: 62db708b-6cf0-45c5-b897-4b5c75bd2505
topic_type:
- apiref
ms.openlocfilehash: 4c9472d6377246833c7c30f072549da9c44f05d8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790940"
---
# <a name="icordebugmanagedcallbackexitthread-method"></a><span data-ttu-id="38ab1-103">ICorDebugManagedCallback::ExitThread 方法</span><span class="sxs-lookup"><span data-stu-id="38ab1-103">ICorDebugManagedCallback::ExitThread Method</span></span>

<span data-ttu-id="38ab1-104">通知调试器已退出正在执行的托管代码的线程。</span><span class="sxs-lookup"><span data-stu-id="38ab1-104">Notifies the debugger that a thread that was executing managed code has exited.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38ab1-105">语法</span><span class="sxs-lookup"><span data-stu-id="38ab1-105">Syntax</span></span>  
  
```cpp  
HRESULT ExitThread (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *thread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="38ab1-106">参数</span><span class="sxs-lookup"><span data-stu-id="38ab1-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="38ab1-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含托管线程的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="38ab1-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain containing the managed thread.</span></span>  
  
 `thread`  
 <span data-ttu-id="38ab1-108">中指向 ICorDebugThread 对象的指针，该对象表示托管线程。</span><span class="sxs-lookup"><span data-stu-id="38ab1-108">[in] A pointer to an ICorDebugThread object that represents the managed thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="38ab1-109">备注</span><span class="sxs-lookup"><span data-stu-id="38ab1-109">Remarks</span></span>  

 <span data-ttu-id="38ab1-110">`ExitThread`引发回调后，线程将不再出现在线程枚举中。</span><span class="sxs-lookup"><span data-stu-id="38ab1-110">Once the `ExitThread` callback is fired, the thread will no longer appear in thread enumerations.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="38ab1-111">要求</span><span class="sxs-lookup"><span data-stu-id="38ab1-111">Requirements</span></span>  

 <span data-ttu-id="38ab1-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="38ab1-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="38ab1-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="38ab1-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="38ab1-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="38ab1-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="38ab1-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="38ab1-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38ab1-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="38ab1-116">See also</span></span>

- [<span data-ttu-id="38ab1-117">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="38ab1-117">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
