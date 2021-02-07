---
description: 了解详细信息： ICorDebugManagedCallback：： UnloadModule 方法
title: ICorDebugManagedCallback::UnloadModule 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.UnloadModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::UnloadModule
helpviewer_keywords:
- ICorDebugManagedCallback::UnloadModule method [.NET Framework debugging]
- UnloadModule method [.NET Framework debugging]
ms.assetid: b12bfcd9-1e29-48bf-9a3d-44bfae5df5e8
topic_type:
- apiref
ms.openlocfilehash: d8d37b28d7a7d11000c259f1bcde3138634b2498
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754051"
---
# <a name="icordebugmanagedcallbackunloadmodule-method"></a><span data-ttu-id="87893-103">ICorDebugManagedCallback::UnloadModule 方法</span><span class="sxs-lookup"><span data-stu-id="87893-103">ICorDebugManagedCallback::UnloadModule Method</span></span>

<span data-ttu-id="87893-104">通知调试器已卸载了公共语言运行时模块 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="87893-104">Notifies the debugger that a common language runtime module (DLL) has been unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="87893-105">语法</span><span class="sxs-lookup"><span data-stu-id="87893-105">Syntax</span></span>  
  
```cpp  
HRESULT UnloadModule (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugModule     *pModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="87893-106">参数</span><span class="sxs-lookup"><span data-stu-id="87893-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="87893-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含模块的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="87893-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contained the module.</span></span>  
  
 `pModule`  
 <span data-ttu-id="87893-108">中指向表示模块的 ICorDebugModule 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="87893-108">[in] A pointer to an ICorDebugModule object that represents the module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="87893-109">备注</span><span class="sxs-lookup"><span data-stu-id="87893-109">Remarks</span></span>  

 <span data-ttu-id="87893-110">此调用之后不应使用该模块。</span><span class="sxs-lookup"><span data-stu-id="87893-110">The module should not be used after this call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="87893-111">要求</span><span class="sxs-lookup"><span data-stu-id="87893-111">Requirements</span></span>  

 <span data-ttu-id="87893-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="87893-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="87893-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="87893-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="87893-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="87893-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="87893-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="87893-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="87893-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="87893-116">See also</span></span>

- [<span data-ttu-id="87893-117">LoadModule 方法</span><span class="sxs-lookup"><span data-stu-id="87893-117">LoadModule Method</span></span>](icordebugmanagedcallback-loadmodule-method.md)
- [<span data-ttu-id="87893-118">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="87893-118">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
