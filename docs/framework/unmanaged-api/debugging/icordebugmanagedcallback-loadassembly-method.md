---
description: 了解详细信息： ICorDebugManagedCallback：： LoadAssembly 方法
title: ICorDebugManagedCallback::LoadAssembly 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.LoadAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::LoadAssembly
helpviewer_keywords:
- LoadAssembly method [.NET Framework debugging]
- ICorDebugManagedCallback::LoadAssembly method [.NET Framework debugging]
ms.assetid: 55cb673a-e240-43a6-a406-6912e7c0fe66
topic_type:
- apiref
ms.openlocfilehash: b90391f3c6286323db11dadae841db38f9b785a7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722797"
---
# <a name="icordebugmanagedcallbackloadassembly-method"></a><span data-ttu-id="c7567-103">ICorDebugManagedCallback::LoadAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="c7567-103">ICorDebugManagedCallback::LoadAssembly Method</span></span>

<span data-ttu-id="c7567-104">通知调试器已成功加载公共语言运行时 (CLR) 程序集。</span><span class="sxs-lookup"><span data-stu-id="c7567-104">Notifies the debugger that a common language runtime (CLR) assembly has been successfully loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7567-105">语法</span><span class="sxs-lookup"><span data-stu-id="c7567-105">Syntax</span></span>  
  
```cpp  
HRESULT LoadAssembly (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugAssembly  *pAssembly  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c7567-106">参数</span><span class="sxs-lookup"><span data-stu-id="c7567-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="c7567-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示已加载程序集的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="c7567-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain into which the assembly has been loaded.</span></span>  
  
 `pAssembly`  
 <span data-ttu-id="c7567-108">中指向表示程序集的 ICorDebugAssembly 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="c7567-108">[in] A pointer to an ICorDebugAssembly object that represents the assembly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c7567-109">要求</span><span class="sxs-lookup"><span data-stu-id="c7567-109">Requirements</span></span>  

 <span data-ttu-id="c7567-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c7567-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7567-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c7567-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c7567-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c7567-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c7567-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7567-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7567-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="c7567-114">See also</span></span>

- [<span data-ttu-id="c7567-115">UnloadAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="c7567-115">UnloadAssembly Method</span></span>](icordebugmanagedcallback-unloadassembly-method.md)
- [<span data-ttu-id="c7567-116">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="c7567-116">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
