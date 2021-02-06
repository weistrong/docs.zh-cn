---
description: 了解详细信息： ICorDebugManagedCallback：： LoadModule 方法
title: ICorDebugManagedCallback::LoadModule 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.LoadModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::LoadModule
helpviewer_keywords:
- ICorDebugManagedCallback::LoadModule method [.NET Framework debugging]
- LoadModule method [.NET Framework debugging]
ms.assetid: 66ec04e9-87cb-42ce-9720-81522abb5d5a
topic_type:
- apiref
ms.openlocfilehash: 9a547d384b3f450054ebc70072664c6dcfb5992f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660488"
---
# <a name="icordebugmanagedcallbackloadmodule-method"></a><span data-ttu-id="ca414-103">ICorDebugManagedCallback::LoadModule 方法</span><span class="sxs-lookup"><span data-stu-id="ca414-103">ICorDebugManagedCallback::LoadModule Method</span></span>

<span data-ttu-id="ca414-104">通知调试器已成功加载公共语言运行时 (CLR) 模块。</span><span class="sxs-lookup"><span data-stu-id="ca414-104">Notifies the debugger that a common language runtime (CLR) module has been successfully loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca414-105">语法</span><span class="sxs-lookup"><span data-stu-id="ca414-105">Syntax</span></span>  
  
```cpp  
HRESULT LoadModule (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugModule    *pModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ca414-106">参数</span><span class="sxs-lookup"><span data-stu-id="ca414-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="ca414-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示已加载该模块的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="ca414-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain into which the module has been loaded.</span></span>  
  
 `pModule`  
 <span data-ttu-id="ca414-108">中指向 ICorDebugModule 对象的指针，该对象表示 CLR 模块。</span><span class="sxs-lookup"><span data-stu-id="ca414-108">[in] A pointer to an ICorDebugModule object that represents the CLR module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ca414-109">备注</span><span class="sxs-lookup"><span data-stu-id="ca414-109">Remarks</span></span>  

 <span data-ttu-id="ca414-110">`LoadModule`回调提供适当的时间来检查模块的元数据、设置实时 (JIT) 编译器标志，或者为模块启用或禁用类加载回调。</span><span class="sxs-lookup"><span data-stu-id="ca414-110">The `LoadModule` callback provides an appropriate time to examine metadata for the module, set just-in-time (JIT) compiler flags, or enable or disable class loading callbacks for the module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca414-111">要求</span><span class="sxs-lookup"><span data-stu-id="ca414-111">Requirements</span></span>  

 <span data-ttu-id="ca414-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ca414-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca414-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ca414-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ca414-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ca414-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ca414-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca414-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca414-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="ca414-116">See also</span></span>

- [<span data-ttu-id="ca414-117">UnloadModule 方法</span><span class="sxs-lookup"><span data-stu-id="ca414-117">UnloadModule Method</span></span>](icordebugmanagedcallback-unloadmodule-method.md)
- [<span data-ttu-id="ca414-118">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="ca414-118">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
