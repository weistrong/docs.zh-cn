---
description: 了解详细信息： ICorDebugManagedCallback：： UnloadAssembly 方法
title: ICorDebugManagedCallback::UnloadAssembly 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.UnloadAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::UnloadAssembly
helpviewer_keywords:
- ICorDebugManagedCallback::UnloadAssembly method [.NET Framework debugging]
- UnloadAssembly method [.NET Framework debugging]
ms.assetid: 6734321c-c8a9-401f-a558-cad715ec4a77
topic_type:
- apiref
ms.openlocfilehash: b1860e90ba2bab1428a0f8559d18801136bbbb39
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660331"
---
# <a name="icordebugmanagedcallbackunloadassembly-method"></a><span data-ttu-id="7cfa1-103">ICorDebugManagedCallback::UnloadAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="7cfa1-103">ICorDebugManagedCallback::UnloadAssembly Method</span></span>

<span data-ttu-id="7cfa1-104">通知调试器已卸载了公共语言运行时程序集。</span><span class="sxs-lookup"><span data-stu-id="7cfa1-104">Notifies the debugger that a common language runtime assembly has been unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7cfa1-105">语法</span><span class="sxs-lookup"><span data-stu-id="7cfa1-105">Syntax</span></span>  
  
```cpp  
HRESULT UnloadAssembly (  
    [in] IcorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugAssembly   *pAssembly  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7cfa1-106">参数</span><span class="sxs-lookup"><span data-stu-id="7cfa1-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="7cfa1-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含程序集的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="7cfa1-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contained the assembly.</span></span>  
  
 `pAssembly`  
 <span data-ttu-id="7cfa1-108">中指向表示程序集的 ICorDebugAssembly 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="7cfa1-108">[in] A pointer to an ICorDebugAssembly object that represents the assembly.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7cfa1-109">备注</span><span class="sxs-lookup"><span data-stu-id="7cfa1-109">Remarks</span></span>  

 <span data-ttu-id="7cfa1-110">不应在此回调后使用该程序集。</span><span class="sxs-lookup"><span data-stu-id="7cfa1-110">The assembly should not be used after this callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7cfa1-111">要求</span><span class="sxs-lookup"><span data-stu-id="7cfa1-111">Requirements</span></span>  

 <span data-ttu-id="7cfa1-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7cfa1-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7cfa1-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7cfa1-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7cfa1-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7cfa1-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7cfa1-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7cfa1-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7cfa1-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="7cfa1-116">See also</span></span>

- [<span data-ttu-id="7cfa1-117">LoadAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="7cfa1-117">LoadAssembly Method</span></span>](icordebugmanagedcallback-loadassembly-method.md)
- [<span data-ttu-id="7cfa1-118">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="7cfa1-118">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
