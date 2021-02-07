---
description: 了解详细信息： ICorDebugComObjectValue 接口
title: ICorDebugComObjectValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugComObjectValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugComObjectValue
helpviewer_keywords:
- ICorDebugComObjectValue interface [.NET Framework debugging]
ms.assetid: 505a7f6c-d92b-42b4-b539-433f5102ea9b
topic_type:
- apiref
ms.openlocfilehash: 3c071c371ae6e330431630cfb1934b538d62efe6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710811"
---
# <a name="icordebugcomobjectvalue-interface"></a><span data-ttu-id="44ff3-103">ICorDebugComObjectValue 接口</span><span class="sxs-lookup"><span data-stu-id="44ff3-103">ICorDebugComObjectValue Interface</span></span>

<span data-ttu-id="44ff3-104">提供方法以检索与运行时可调用包装关联的信息 (RCW) 。</span><span class="sxs-lookup"><span data-stu-id="44ff3-104">Provides methods to retrieve information associated with a runtime callable wrapper (RCW).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="44ff3-105">方法</span><span class="sxs-lookup"><span data-stu-id="44ff3-105">Methods</span></span>  
  
|<span data-ttu-id="44ff3-106">方法</span><span class="sxs-lookup"><span data-stu-id="44ff3-106">Method</span></span>|<span data-ttu-id="44ff3-107">说明</span><span class="sxs-lookup"><span data-stu-id="44ff3-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="44ff3-108">GetCachedInterfacePointers 方法</span><span class="sxs-lookup"><span data-stu-id="44ff3-108">GetCachedInterfacePointers Method</span></span>](icordebugcomobjectvalue-getcachedinterfacepointers-method.md)|<span data-ttu-id="44ff3-109">获取缓存在当前 RCW 上的原始接口指针。</span><span class="sxs-lookup"><span data-stu-id="44ff3-109">Gets the raw interface pointers cached on the current RCW.</span></span>|  
|[<span data-ttu-id="44ff3-110">GetCachedInterfaceTypes 方法</span><span class="sxs-lookup"><span data-stu-id="44ff3-110">GetCachedInterfaceTypes Method</span></span>](icordebugcomobjectvalue-getcachedinterfacetypes-method.md)|<span data-ttu-id="44ff3-111">为当前对象的大小写或用作的接口类型提供枚举器。</span><span class="sxs-lookup"><span data-stu-id="44ff3-111">Provides an enumerator for the interface types that the current object has been cased to or used as.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="44ff3-112">备注</span><span class="sxs-lookup"><span data-stu-id="44ff3-112">Remarks</span></span>  

 <span data-ttu-id="44ff3-113">若要检查 "ICorDebugValue" 接口的实例是否表示 RCW，调试程序 `QueryInterface` 使用 "ICorDebugValue" 调用 `IID_ICorDebugComObjectValue` 。</span><span class="sxs-lookup"><span data-stu-id="44ff3-113">To check whether an instance of an "ICorDebugValue" interface represents an RCW, a debugger calls `QueryInterface` on "ICorDebugValue" with `IID_ICorDebugComObjectValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="44ff3-114">要求</span><span class="sxs-lookup"><span data-stu-id="44ff3-114">Requirements</span></span>  

 <span data-ttu-id="44ff3-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="44ff3-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="44ff3-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="44ff3-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="44ff3-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="44ff3-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="44ff3-118">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="44ff3-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44ff3-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="44ff3-119">See also</span></span>

- [<span data-ttu-id="44ff3-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="44ff3-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="44ff3-121">调试</span><span class="sxs-lookup"><span data-stu-id="44ff3-121">Debugging</span></span>](index.md)
