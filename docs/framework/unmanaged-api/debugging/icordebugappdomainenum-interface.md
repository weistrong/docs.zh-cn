---
description: 了解详细信息： ICorDebugAppDomainEnum 接口
title: ICorDebugAppDomainEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomainEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomainEnum
helpviewer_keywords:
- ICorDebugAppDomainEnum interface [.NET Framework debugging]
ms.assetid: e9226e6e-ca2c-428e-bb38-0c099210f507
topic_type:
- apiref
ms.openlocfilehash: dfea6254e6cf4f162e44d057fb4126a67a087b61
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754151"
---
# <a name="icordebugappdomainenum-interface"></a><span data-ttu-id="ca072-103">ICorDebugAppDomainEnum 接口</span><span class="sxs-lookup"><span data-stu-id="ca072-103">ICorDebugAppDomainEnum Interface</span></span>

<span data-ttu-id="ca072-104">提供 `Next` 方法，该方法 `ICorDebugAppDomainEnum` 从枚举中的下一个位置开始返回指定数目的值。</span><span class="sxs-lookup"><span data-stu-id="ca072-104">Provides the `Next` method, which returns a specified number of `ICorDebugAppDomainEnum` values starting at the next location in the enumeration.</span></span> <span data-ttu-id="ca072-105">此接口是 "ICorDebugEnum" 的子类。</span><span class="sxs-lookup"><span data-stu-id="ca072-105">This interface is a subclass of "ICorDebugEnum".</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ca072-106">方法</span><span class="sxs-lookup"><span data-stu-id="ca072-106">Methods</span></span>  
  
|<span data-ttu-id="ca072-107">方法</span><span class="sxs-lookup"><span data-stu-id="ca072-107">Method</span></span>|<span data-ttu-id="ca072-108">说明</span><span class="sxs-lookup"><span data-stu-id="ca072-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ca072-109">下一方法</span><span class="sxs-lookup"><span data-stu-id="ca072-109">Next Method</span></span>](icordebugappdomainenum-next-method.md)|<span data-ttu-id="ca072-110">从当前游标位置开始，获取集合中指定数量的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="ca072-110">Gets the specified number of application domains from the collection, starting at the current cursor position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ca072-111">备注</span><span class="sxs-lookup"><span data-stu-id="ca072-111">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ca072-112">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="ca072-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca072-113">要求</span><span class="sxs-lookup"><span data-stu-id="ca072-113">Requirements</span></span>  

 <span data-ttu-id="ca072-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ca072-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca072-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ca072-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ca072-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ca072-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ca072-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca072-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca072-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="ca072-118">See also</span></span>

- [<span data-ttu-id="ca072-119">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="ca072-119">ICorDebug Interface</span></span>](icordebug-interface.md)
- [<span data-ttu-id="ca072-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="ca072-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
