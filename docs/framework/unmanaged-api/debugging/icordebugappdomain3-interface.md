---
description: 了解详细信息： ICorDebugAppDomain3 接口
title: ICorDebugAppDomain3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain3
helpviewer_keywords:
- ICorDebugAppDomain3 interface [.NET Framework debugging]
ms.assetid: 875ef5be-c1e7-4d95-97e9-d3a667aeaba0
topic_type:
- apiref
ms.openlocfilehash: 6575aa685759102443babeaf82774e6221b80693
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772206"
---
# <a name="icordebugappdomain3-interface"></a><span data-ttu-id="3ca78-103">ICorDebugAppDomain3 接口</span><span class="sxs-lookup"><span data-stu-id="3ca78-103">ICorDebugAppDomain3 Interface</span></span>

<span data-ttu-id="3ca78-104">提供方法以检索有关应用程序域中当前加载的 Windows 运行时类型的托管表示形式的信息。</span><span class="sxs-lookup"><span data-stu-id="3ca78-104">Provides methods to retrieve information about the managed representations of Windows Runtime types currently loaded in an application domain.</span></span> <span data-ttu-id="3ca78-105">此接口是 ICorDebugAppDomain 和 ICorDebugAppDomain2 接口的扩展。</span><span class="sxs-lookup"><span data-stu-id="3ca78-105">This interface is an extension of the ICorDebugAppDomain and ICorDebugAppDomain2 interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3ca78-106">方法</span><span class="sxs-lookup"><span data-stu-id="3ca78-106">Methods</span></span>  
  
|<span data-ttu-id="3ca78-107">方法</span><span class="sxs-lookup"><span data-stu-id="3ca78-107">Method</span></span>|<span data-ttu-id="3ca78-108">说明</span><span class="sxs-lookup"><span data-stu-id="3ca78-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3ca78-109">ICorDebugAppDomain3：： GetCachedWinRTTypes</span><span class="sxs-lookup"><span data-stu-id="3ca78-109">ICorDebugAppDomain3::GetCachedWinRTTypes</span></span>](icordebugappdomain3-getcachedwinrttypes-method.md)|<span data-ttu-id="3ca78-110">获取所有缓存 Windows 运行时类型的枚举器。</span><span class="sxs-lookup"><span data-stu-id="3ca78-110">Gets an enumerator for all cached Windows Runtime types.</span></span>|  
|[<span data-ttu-id="3ca78-111">ICorDebugAppDomain3：： GetCachedWinRTTypesForIIDs</span><span class="sxs-lookup"><span data-stu-id="3ca78-111">ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs</span></span>](icordebugappdomain3-getcachedwinrttypesforiids-method.md)|<span data-ttu-id="3ca78-112">基于其接口标识符获取应用程序域中缓存的 Windows 运行时类型的枚举器。</span><span class="sxs-lookup"><span data-stu-id="3ca78-112">Gets an enumerator for cached Windows Runtime types in an application domain based on their interface identifiers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3ca78-113">备注</span><span class="sxs-lookup"><span data-stu-id="3ca78-113">Remarks</span></span>  

 <span data-ttu-id="3ca78-114">此接口旨在由调试器结合使用，并与函数计算调用一起使用 `M:System.Runtime.InteropServices.Marshal.GetInspectableIIDs(System.Object)` 。</span><span class="sxs-lookup"><span data-stu-id="3ca78-114">This interface is meant to be used by a debugger in conjunction with a function evaluation call to `M:System.Runtime.InteropServices.Marshal.GetInspectableIIDs(System.Object)`.</span></span> <span data-ttu-id="3ca78-115">当方法检索 Windows 运行时 server 对象支持的接口标识符时，调试器可以使用在此接口中定义的方法，将它们映射到与这些接口相对应的托管类型。</span><span class="sxs-lookup"><span data-stu-id="3ca78-115">When the method retrieves the interface identifiers supported by a Windows Runtime server object, the debugger may use the methods defined in this interface to map them to managed types that correspond to those interfaces.</span></span>  
  
 <span data-ttu-id="3ca78-116">若要检索此接口的实例，请 `QueryInterface` 在 ICorDebugAppDomain 或 ICorDebugAppDomain2 接口的实例上运行。</span><span class="sxs-lookup"><span data-stu-id="3ca78-116">To retrieve an instance of this interface, run `QueryInterface` on an instance of the ICorDebugAppDomain or ICorDebugAppDomain2 interface.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3ca78-117">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="3ca78-117">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3ca78-118">要求</span><span class="sxs-lookup"><span data-stu-id="3ca78-118">Requirements</span></span>  

 <span data-ttu-id="3ca78-119">**平台：** Windows 运行时</span><span class="sxs-lookup"><span data-stu-id="3ca78-119">**Platforms:** Windows Runtime</span></span>  
  
 <span data-ttu-id="3ca78-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3ca78-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3ca78-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3ca78-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3ca78-122">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3ca78-122">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ca78-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="3ca78-123">See also</span></span>

- [<span data-ttu-id="3ca78-124">调试接口</span><span class="sxs-lookup"><span data-stu-id="3ca78-124">Debugging Interfaces</span></span>](debugging-interfaces.md)
