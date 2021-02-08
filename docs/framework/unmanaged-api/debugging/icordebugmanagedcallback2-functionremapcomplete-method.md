---
description: 了解详细信息： ICorDebugManagedCallback2：： FunctionRemapComplete 方法
title: ICorDebugManagedCallback2::FunctionRemapComplete 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2.FunctionRemapComplete
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2::FunctionRemapComplete
helpviewer_keywords:
- FunctionRemapComplete method [.NET Framework debugging]
- ICorDebugManagedCallback2::FunctionRemapComplete method [.NET Framework debugging]
ms.assetid: 5396c4c3-4ec3-4e3a-a38d-d65b21f0a2fc
topic_type:
- apiref
ms.openlocfilehash: fcb4388185de17d602c1e3dbc725e104a0a48b3b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790838"
---
# <a name="icordebugmanagedcallback2functionremapcomplete-method"></a><span data-ttu-id="9fea9-103">ICorDebugManagedCallback2::FunctionRemapComplete 方法</span><span class="sxs-lookup"><span data-stu-id="9fea9-103">ICorDebugManagedCallback2::FunctionRemapComplete Method</span></span>

<span data-ttu-id="9fea9-104">通知调试器，代码执行已切换到已编辑函数的新版本。</span><span class="sxs-lookup"><span data-stu-id="9fea9-104">Notifies the debugger that code execution has switched to a new version of an edited function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9fea9-105">语法</span><span class="sxs-lookup"><span data-stu-id="9fea9-105">Syntax</span></span>  
  
```cpp  
HRESULT FunctionRemapComplete (  
    [in] ICorDebugAppDomain   *pAppDomain,  
    [in] ICorDebugThread      *pThread,  
    [in] ICorDebugFunction    *pFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9fea9-106">参数</span><span class="sxs-lookup"><span data-stu-id="9fea9-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="9fea9-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含已编辑函数的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="9fea9-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain containing the edited function.</span></span>  
  
 `pThread`  
 <span data-ttu-id="9fea9-108">中指向 ICorDebugThread 对象的指针，该对象表示遇到重新映射断点的线程。</span><span class="sxs-lookup"><span data-stu-id="9fea9-108">[in] A pointer to an ICorDebugThread object that represents the thread on which the remap breakpoint was encountered.</span></span>  
  
 `pFunction`  
 <span data-ttu-id="9fea9-109">中指向 ICorDebugFunction 对象的指针，该对象表示线程上当前正在运行的函数的版本。</span><span class="sxs-lookup"><span data-stu-id="9fea9-109">[in] A pointer to an ICorDebugFunction object that represents the version of the function currently running on the thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9fea9-110">备注</span><span class="sxs-lookup"><span data-stu-id="9fea9-110">Remarks</span></span>  

 <span data-ttu-id="9fea9-111">此回调使调试器有机会重新创建以前存在的任何 steppers。</span><span class="sxs-lookup"><span data-stu-id="9fea9-111">This callback gives the debugger an opportunity to recreate any steppers that previously existed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9fea9-112">要求</span><span class="sxs-lookup"><span data-stu-id="9fea9-112">Requirements</span></span>  

 <span data-ttu-id="9fea9-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9fea9-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9fea9-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9fea9-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9fea9-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9fea9-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9fea9-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9fea9-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9fea9-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="9fea9-117">See also</span></span>

- [<span data-ttu-id="9fea9-118">ICorDebugManagedCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="9fea9-118">ICorDebugManagedCallback2 Interface</span></span>](icordebugmanagedcallback2-interface.md)
- [<span data-ttu-id="9fea9-119">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="9fea9-119">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
