---
description: 了解详细信息： ICorDebugManagedCallback：： UnloadClass 方法
title: ICorDebugManagedCallback::UnloadClass 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.UnloadClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::UnloadClass
helpviewer_keywords:
- ICorDebugManagedCallback::UnloadClass method [.NET Framework debugging]
- UnloadClass method [.NET Framework debugging]
ms.assetid: 66a59b18-ce9a-41f4-b23b-4dd6753d6d36
topic_type:
- apiref
ms.openlocfilehash: b76caf39611b0f59c74b4ae47d167e6f232a6dbc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660196"
---
# <a name="icordebugmanagedcallbackunloadclass-method"></a><span data-ttu-id="7e98f-103">ICorDebugManagedCallback::UnloadClass 方法</span><span class="sxs-lookup"><span data-stu-id="7e98f-103">ICorDebugManagedCallback::UnloadClass Method</span></span>

<span data-ttu-id="7e98f-104">通知调试器正在卸载某个类。</span><span class="sxs-lookup"><span data-stu-id="7e98f-104">Notifies the debugger that a class is being unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7e98f-105">语法</span><span class="sxs-lookup"><span data-stu-id="7e98f-105">Syntax</span></span>  
  
```cpp  
HRESULT UnloadClass (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugClass      *c  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7e98f-106">参数</span><span class="sxs-lookup"><span data-stu-id="7e98f-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="7e98f-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含类的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="7e98f-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain containing the class.</span></span>  
  
 `c`  
 <span data-ttu-id="7e98f-108">中指向 ICorDebugClass 对象的指针，该对象表示类。</span><span class="sxs-lookup"><span data-stu-id="7e98f-108">[in] A pointer to an ICorDebugClass object that represents the class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7e98f-109">备注</span><span class="sxs-lookup"><span data-stu-id="7e98f-109">Remarks</span></span>  

 <span data-ttu-id="7e98f-110">不应在此调用后引用此类。</span><span class="sxs-lookup"><span data-stu-id="7e98f-110">The class should not be referenced after this call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7e98f-111">要求</span><span class="sxs-lookup"><span data-stu-id="7e98f-111">Requirements</span></span>  

 <span data-ttu-id="7e98f-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7e98f-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7e98f-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7e98f-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7e98f-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7e98f-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7e98f-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7e98f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e98f-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="7e98f-116">See also</span></span>

- [<span data-ttu-id="7e98f-117">LoadClass 方法</span><span class="sxs-lookup"><span data-stu-id="7e98f-117">LoadClass Method</span></span>](icordebugmanagedcallback-loadclass-method.md)
- [<span data-ttu-id="7e98f-118">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="7e98f-118">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
