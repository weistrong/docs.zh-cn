---
description: 了解详细信息： ICorDebugModuleDebugEvent：： GetModule 方法
title: ICorDebugModuleDebugEvent::GetModule 方法
ms.date: 03/30/2017
ms.assetid: b1141c35-4253-4e34-b3e4-ed406a9dea4f
ms.openlocfilehash: c6d7171da231576ff90f54aaefe4b473af0afd40
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790732"
---
# <a name="icordebugmoduledebugeventgetmodule-method"></a><span data-ttu-id="7bc56-103">ICorDebugModuleDebugEvent::GetModule 方法</span><span class="sxs-lookup"><span data-stu-id="7bc56-103">ICorDebugModuleDebugEvent::GetModule Method</span></span>

<span data-ttu-id="7bc56-104">获取刚加载或卸载的合并模块。</span><span class="sxs-lookup"><span data-stu-id="7bc56-104">Gets the merged module that was just loaded or unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7bc56-105">语法</span><span class="sxs-lookup"><span data-stu-id="7bc56-105">Syntax</span></span>  
  
```cpp  
HRESULT GetModule(  
   [out]ICorDebugModule **ppModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7bc56-106">参数</span><span class="sxs-lookup"><span data-stu-id="7bc56-106">Parameters</span></span>  

 `ppModule`  
 <span data-ttu-id="7bc56-107">[out] 指向 ICorDebugModule 对象地址的指针，该对象表示刚加载或卸载的合并模块。</span><span class="sxs-lookup"><span data-stu-id="7bc56-107">[out] A pointer to the address of an ICorDebugModule object that represents the merged module that was just loaded or unloaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7bc56-108">备注</span><span class="sxs-lookup"><span data-stu-id="7bc56-108">Remarks</span></span>  

 <span data-ttu-id="7bc56-109">可以调用 [GetEventKind](icordebugdebugevent-geteventkind-method.md) 方法来确定是加载还是卸载该模块。</span><span class="sxs-lookup"><span data-stu-id="7bc56-109">You can call the [GetEventKind](icordebugdebugevent-geteventkind-method.md) method to determine whether the module was loaded or unloaded.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7bc56-110">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="7bc56-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7bc56-111">要求</span><span class="sxs-lookup"><span data-stu-id="7bc56-111">Requirements</span></span>  

 <span data-ttu-id="7bc56-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7bc56-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7bc56-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7bc56-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7bc56-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7bc56-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7bc56-115">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7bc56-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7bc56-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="7bc56-116">See also</span></span>

- [<span data-ttu-id="7bc56-117">ICorDebugModuleDebugEvent 接口</span><span class="sxs-lookup"><span data-stu-id="7bc56-117">ICorDebugModuleDebugEvent Interface</span></span>](icordebugmoduledebugevent-interface.md)
- [<span data-ttu-id="7bc56-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="7bc56-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
