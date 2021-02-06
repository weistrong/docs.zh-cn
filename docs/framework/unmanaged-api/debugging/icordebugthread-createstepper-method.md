---
description: 了解详细信息： ICorDebugThread：： CreateStepper 方法
title: ICorDebugThread::CreateStepper 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.CreateStepper
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::CreateStepper
helpviewer_keywords:
- ICorDebugThread::CreateStepper method [.NET Framework debugging]
- CreateStepper method, ICorDebugThread interface [.NET Framework debugging]
ms.assetid: 4657443f-dd12-431b-a648-175c23f13c83
topic_type:
- apiref
ms.openlocfilehash: 378ce28281f4f284c36194f993a53598a9de3854
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659356"
---
# <a name="icordebugthreadcreatestepper-method"></a><span data-ttu-id="dc280-103">ICorDebugThread::CreateStepper 方法</span><span class="sxs-lookup"><span data-stu-id="dc280-103">ICorDebugThread::CreateStepper Method</span></span>

<span data-ttu-id="dc280-104">创建一个 ICorDebugStepper 对象，该对象允许单步执行此 ICorDebugThread 的活动框架。</span><span class="sxs-lookup"><span data-stu-id="dc280-104">Creates an ICorDebugStepper object that allows stepping through the active frame of this ICorDebugThread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc280-105">语法</span><span class="sxs-lookup"><span data-stu-id="dc280-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateStepper (  
    [out] ICorDebugStepper **ppStepper  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dc280-106">参数</span><span class="sxs-lookup"><span data-stu-id="dc280-106">Parameters</span></span>  

 `ppStepper`  
 <span data-ttu-id="dc280-107">弄指向 `ICorDebugStepper` 允许单步执行此线程的活动帧的对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="dc280-107">[out] A pointer to the address of an `ICorDebugStepper` object that allows stepping through the active frame of this thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dc280-108">备注</span><span class="sxs-lookup"><span data-stu-id="dc280-108">Remarks</span></span>  

 <span data-ttu-id="dc280-109">活动框架可能是非托管代码。</span><span class="sxs-lookup"><span data-stu-id="dc280-109">The active frame may be unmanaged code.</span></span>  
  
 <span data-ttu-id="dc280-110">`ICorDebugStepper`接口必须用于执行实际步进。</span><span class="sxs-lookup"><span data-stu-id="dc280-110">The `ICorDebugStepper` interface must be used to perform the actual stepping.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dc280-111">要求</span><span class="sxs-lookup"><span data-stu-id="dc280-111">Requirements</span></span>  

 <span data-ttu-id="dc280-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dc280-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dc280-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="dc280-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="dc280-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dc280-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dc280-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dc280-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
