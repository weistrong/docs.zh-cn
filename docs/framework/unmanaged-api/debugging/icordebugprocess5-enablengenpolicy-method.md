---
description: 了解详细信息： ICorDebugProcess5：： EnableNGENPolicy 方法
title: ICorDebugProcess5::EnableNGENPolicy 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5::EnableNGenPolicy
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::EnableNGENPolicy
helpviewer_keywords:
- ICorDebugProcess5::EnableNGENPolicy method [.NET Framework debugging]
- EnableNGENPolicy method, ICorDebugProcess5 interface [.NET Framework debugging]
ms.assetid: 3b8e15ca-3c72-4685-a937-da4c739cb9e9
topic_type:
- apiref
ms.openlocfilehash: 0f3194893665bfe9fff802a293aaafed8254f2e3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649918"
---
# <a name="icordebugprocess5enablengenpolicy-method"></a><span data-ttu-id="fd04f-103">ICorDebugProcess5::EnableNGENPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="fd04f-103">ICorDebugProcess5::EnableNGENPolicy Method</span></span>

<span data-ttu-id="fd04f-104">设置一个值，该值确定应用程序在托管调试器下运行时如何加载本机映像。</span><span class="sxs-lookup"><span data-stu-id="fd04f-104">Sets a value that determines how an application loads native images while running under a managed debugger.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd04f-105">语法</span><span class="sxs-lookup"><span data-stu-id="fd04f-105">Syntax</span></span>  
  
```cpp  
HRESULT EnableNGENPolicy(  
    [in] CorDebugNGENPolicy ePolicy  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fd04f-106">参数</span><span class="sxs-lookup"><span data-stu-id="fd04f-106">Parameters</span></span>  

 `ePolicy`  
 <span data-ttu-id="fd04f-107">中确定应用程序在托管调试器下运行时如何加载本机映像的 [CorDebugNGenPolicy](cordebugngenpolicy-enumeration.md) 常量。</span><span class="sxs-lookup"><span data-stu-id="fd04f-107">[in] A [CorDebugNGenPolicy](cordebugngenpolicy-enumeration.md) constant that determines how an application loads native images while running under a managed debugger.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fd04f-108">备注</span><span class="sxs-lookup"><span data-stu-id="fd04f-108">Remarks</span></span>  

 <span data-ttu-id="fd04f-109">如果策略设置成功，则该方法将返回 `S_OK` 。</span><span class="sxs-lookup"><span data-stu-id="fd04f-109">If the policy is set successfully, the method returns `S_OK`.</span></span> <span data-ttu-id="fd04f-110">如果 `ePolicy` 超出了 [CorDebugNGenPolicy](cordebugngenpolicy-enumeration.md)定义的枚举值的范围，则方法将返回 `E_INVALIDARG` ，并且方法调用不起作用。</span><span class="sxs-lookup"><span data-stu-id="fd04f-110">If `ePolicy` is outside the range of the enumerated values defined by [CorDebugNGenPolicy](cordebugngenpolicy-enumeration.md), the method returns `E_INVALIDARG` and the method call has no effect.</span></span> <span data-ttu-id="fd04f-111">如果无法更新本地映像生成器 ( # A0) 的策略，该方法将返回 `E_FAIL` 。</span><span class="sxs-lookup"><span data-stu-id="fd04f-111">If the policy of the Native Image Generator (Ngen.exe) cannot be updated, the method returns `E_FAIL`.</span></span>  
  
 <span data-ttu-id="fd04f-112">在 `ICorDebugProcess5::EnableNGenPolicy` 进程的生存期内随时可以调用方法。</span><span class="sxs-lookup"><span data-stu-id="fd04f-112">The `ICorDebugProcess5::EnableNGenPolicy` method can be called at any time during the lifetime of the process.</span></span> <span data-ttu-id="fd04f-113">此策略对设置策略后加载的任何模块有效。</span><span class="sxs-lookup"><span data-stu-id="fd04f-113">The policy is in effect for any modules that are loaded after the policy is set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd04f-114">要求</span><span class="sxs-lookup"><span data-stu-id="fd04f-114">Requirements</span></span>  

 <span data-ttu-id="fd04f-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fd04f-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fd04f-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fd04f-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fd04f-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fd04f-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fd04f-118">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd04f-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd04f-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="fd04f-119">See also</span></span>

- [<span data-ttu-id="fd04f-120">ICorDebugProcess5 接口</span><span class="sxs-lookup"><span data-stu-id="fd04f-120">ICorDebugProcess5 Interface</span></span>](icordebugprocess5-interface.md)
- [<span data-ttu-id="fd04f-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="fd04f-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="fd04f-122">调试</span><span class="sxs-lookup"><span data-stu-id="fd04f-122">Debugging</span></span>](index.md)
