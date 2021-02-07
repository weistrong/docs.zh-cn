---
description: 了解详细信息： ICorDebugCode2 接口
title: ICorDebugCode2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugCode2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode2
helpviewer_keywords:
- ICorDebugCode2 interface [.NET Framework debugging]
ms.assetid: 9321903b-7dea-40d8-ba32-99016c00cc46
topic_type:
- apiref
ms.openlocfilehash: 29fd657ec56993d47ee57aa41c81b45e75352697
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99765024"
---
# <a name="icordebugcode2-interface"></a><span data-ttu-id="a9d4d-103">ICorDebugCode2 接口</span><span class="sxs-lookup"><span data-stu-id="a9d4d-103">ICorDebugCode2 Interface</span></span>

<span data-ttu-id="a9d4d-104">提供扩展 "ICorDebugCode" 的功能的方法。</span><span class="sxs-lookup"><span data-stu-id="a9d4d-104">Provides methods that extend the capabilities of "ICorDebugCode".</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a9d4d-105">方法</span><span class="sxs-lookup"><span data-stu-id="a9d4d-105">Methods</span></span>  
  
|<span data-ttu-id="a9d4d-106">方法</span><span class="sxs-lookup"><span data-stu-id="a9d4d-106">Method</span></span>|<span data-ttu-id="a9d4d-107">说明</span><span class="sxs-lookup"><span data-stu-id="a9d4d-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a9d4d-108">GetCodeChunks 方法</span><span class="sxs-lookup"><span data-stu-id="a9d4d-108">GetCodeChunks Method</span></span>](icordebugcode2-getcodechunks-method.md)|<span data-ttu-id="a9d4d-109">获取包含此代码对象的代码块。</span><span class="sxs-lookup"><span data-stu-id="a9d4d-109">Gets the chunks of code that this code object is composed of.</span></span>|  
|[<span data-ttu-id="a9d4d-110">GetCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="a9d4d-110">GetCompilerFlags Method</span></span>](icordebugcode2-getcompilerflags-method.md)|<span data-ttu-id="a9d4d-111">获取一些标志，这些标志指定此代码对象是实时 (JIT) 使用本机映像)  ( 生成器编译或生成的。</span><span class="sxs-lookup"><span data-stu-id="a9d4d-111">Gets the flags that specify the conditions under which this code object was either just-in-time (JIT) compiled or generated using the native image generator (Ngen.exe).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a9d4d-112">备注</span><span class="sxs-lookup"><span data-stu-id="a9d4d-112">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="a9d4d-113">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="a9d4d-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9d4d-114">要求</span><span class="sxs-lookup"><span data-stu-id="a9d4d-114">Requirements</span></span>  

 <span data-ttu-id="a9d4d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a9d4d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9d4d-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a9d4d-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a9d4d-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a9d4d-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a9d4d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9d4d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9d4d-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="a9d4d-119">See also</span></span>

- [<span data-ttu-id="a9d4d-120">ICorDebugCode3 接口</span><span class="sxs-lookup"><span data-stu-id="a9d4d-120">ICorDebugCode3 Interface</span></span>](icordebugcode3-interface.md)
- [<span data-ttu-id="a9d4d-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="a9d4d-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
