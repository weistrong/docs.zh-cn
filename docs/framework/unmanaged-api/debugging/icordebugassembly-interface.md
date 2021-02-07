---
description: 了解详细信息： ICorDebugAssembly 接口
title: ICorDebugAssembly 接口
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly
helpviewer_keywords:
- ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: 9d657a28-6984-4c5e-8a54-89d20080baff
topic_type:
- apiref
ms.openlocfilehash: 746b5f4b2f26550788708d93bf0dd50f5f495041
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711942"
---
# <a name="icordebugassembly-interface"></a><span data-ttu-id="46400-103">ICorDebugAssembly 接口</span><span class="sxs-lookup"><span data-stu-id="46400-103">ICorDebugAssembly Interface</span></span>

<span data-ttu-id="46400-104">表示一个程序集。</span><span class="sxs-lookup"><span data-stu-id="46400-104">Represents an assembly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="46400-105">方法</span><span class="sxs-lookup"><span data-stu-id="46400-105">Methods</span></span>  
  
|<span data-ttu-id="46400-106">方法</span><span class="sxs-lookup"><span data-stu-id="46400-106">Method</span></span>|<span data-ttu-id="46400-107">说明</span><span class="sxs-lookup"><span data-stu-id="46400-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="46400-108">EnumerateModules 方法</span><span class="sxs-lookup"><span data-stu-id="46400-108">EnumerateModules Method</span></span>](icordebugassembly-enumeratemodules-method.md)|<span data-ttu-id="46400-109">获取包含在程序集中的模块的枚举器。</span><span class="sxs-lookup"><span data-stu-id="46400-109">Gets an enumerator for the modules contained in the assembly.</span></span>|  
|[<span data-ttu-id="46400-110">GetAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="46400-110">GetAppDomain Method</span></span>](icordebugassembly-getappdomain-method.md)|<span data-ttu-id="46400-111">获取一个接口指针，该指针指向包含此实例的应用程序域 `ICorDebugAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="46400-111">Gets an interface pointer to the application domain that contains this `ICorDebugAssembly` instance.</span></span>|  
|[<span data-ttu-id="46400-112">GetCodeBase 方法</span><span class="sxs-lookup"><span data-stu-id="46400-112">GetCodeBase Method</span></span>](icordebugassembly-getcodebase-method.md)|<span data-ttu-id="46400-113">未在 .NET Framework 的当前版本中实现。</span><span class="sxs-lookup"><span data-stu-id="46400-113">Not implemented in the current version of the .NET Framework.</span></span>|  
|[<span data-ttu-id="46400-114">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="46400-114">GetName Method</span></span>](icordebugassembly-getname-method.md)|<span data-ttu-id="46400-115">获取程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="46400-115">Gets the name of the assembly.</span></span>|  
|[<span data-ttu-id="46400-116">GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="46400-116">GetProcess Method</span></span>](icordebugassembly-getprocess-method.md)|<span data-ttu-id="46400-117">获取在其中运行程序集的 ICorDebugProcess 实例。</span><span class="sxs-lookup"><span data-stu-id="46400-117">Gets the ICorDebugProcess instance in which the assembly is running.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="46400-118">备注</span><span class="sxs-lookup"><span data-stu-id="46400-118">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="46400-119">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="46400-119">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="46400-120">要求</span><span class="sxs-lookup"><span data-stu-id="46400-120">Requirements</span></span>  

 <span data-ttu-id="46400-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="46400-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46400-122">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="46400-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="46400-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="46400-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="46400-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46400-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46400-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="46400-125">See also</span></span>

- [<span data-ttu-id="46400-126">调试接口</span><span class="sxs-lookup"><span data-stu-id="46400-126">Debugging Interfaces</span></span>](debugging-interfaces.md)
