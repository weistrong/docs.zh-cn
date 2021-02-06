---
description: 了解详细信息： ICorDebugManagedCallback：： LoadClass 方法
title: ICorDebugManagedCallback::LoadClass 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.LoadClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::LoadClass
helpviewer_keywords:
- ICorDebugManagedCallback::LoadClass method [.NET Framework debugging]
- LoadClass method [.NET Framework debugging]
ms.assetid: e58dac7b-85c3-41ca-b9aa-3a7fc9ae6680
topic_type:
- apiref
ms.openlocfilehash: 6f670a2f0798c7edfdc4292334cf9534e59a3007
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660601"
---
# <a name="icordebugmanagedcallbackloadclass-method"></a><span data-ttu-id="d0098-103">ICorDebugManagedCallback::LoadClass 方法</span><span class="sxs-lookup"><span data-stu-id="d0098-103">ICorDebugManagedCallback::LoadClass Method</span></span>

<span data-ttu-id="d0098-104">通知调试器已加载某个类。</span><span class="sxs-lookup"><span data-stu-id="d0098-104">Notifies the debugger that a class has been loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d0098-105">语法</span><span class="sxs-lookup"><span data-stu-id="d0098-105">Syntax</span></span>  
  
```cpp  
HRESULT LoadClass (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugClass     *c  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d0098-106">参数</span><span class="sxs-lookup"><span data-stu-id="d0098-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="d0098-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示要将该类加载到其中的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="d0098-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain into which the class has been loaded.</span></span>  
  
 `c`  
 <span data-ttu-id="d0098-108">中指向 ICorDebugClass 对象的指针，该对象表示类。</span><span class="sxs-lookup"><span data-stu-id="d0098-108">[in] A pointer to an ICorDebugClass object that represents the class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d0098-109">备注</span><span class="sxs-lookup"><span data-stu-id="d0098-109">Remarks</span></span>  

 <span data-ttu-id="d0098-110">只有在为包含类的模块启用了类加载的情况下，才会发生此回调。</span><span class="sxs-lookup"><span data-stu-id="d0098-110">This callback occurs only if class loading has been enabled for the module that contains the class.</span></span> <span data-ttu-id="d0098-111">对于动态模块，始终启用类加载。</span><span class="sxs-lookup"><span data-stu-id="d0098-111">Class loading is always enabled for dynamic modules.</span></span>  
  
 <span data-ttu-id="d0098-112">`LoadClass`回调提供适当的时间将断点绑定到动态模块中新生成的类。</span><span class="sxs-lookup"><span data-stu-id="d0098-112">The `LoadClass` callback provides an appropriate time to bind breakpoints to newly generated classes in dynamic modules.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d0098-113">要求</span><span class="sxs-lookup"><span data-stu-id="d0098-113">Requirements</span></span>  

 <span data-ttu-id="d0098-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d0098-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d0098-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d0098-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d0098-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d0098-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d0098-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d0098-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0098-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="d0098-118">See also</span></span>

- [<span data-ttu-id="d0098-119">UnloadClass 方法</span><span class="sxs-lookup"><span data-stu-id="d0098-119">UnloadClass Method</span></span>](icordebugmanagedcallback-unloadclass-method.md)
- [<span data-ttu-id="d0098-120">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="d0098-120">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
