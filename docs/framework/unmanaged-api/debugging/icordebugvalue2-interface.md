---
description: 了解详细信息： ICorDebugValue2 接口
title: ICorDebugValue2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugValue2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue2
helpviewer_keywords:
- ICorDebugValue2 interface [.NET Framework debugging]
ms.assetid: 3ff2ad2a-da5a-461b-8627-1a8eba49df9c
topic_type:
- apiref
ms.openlocfilehash: b408bb5d1732a60fc9aa8ffb93321d3542f2cab7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690257"
---
# <a name="icordebugvalue2-interface"></a><span data-ttu-id="5bcc7-103">ICorDebugValue2 接口</span><span class="sxs-lookup"><span data-stu-id="5bcc7-103">ICorDebugValue2 Interface</span></span>

<span data-ttu-id="5bcc7-104">扩展 "ICorDebugValue" 接口，以提供对 "ICorDebugType" 对象的支持。</span><span class="sxs-lookup"><span data-stu-id="5bcc7-104">Extends the "ICorDebugValue" interface to provide support for "ICorDebugType" objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5bcc7-105">方法</span><span class="sxs-lookup"><span data-stu-id="5bcc7-105">Methods</span></span>  
  
|<span data-ttu-id="5bcc7-106">方法</span><span class="sxs-lookup"><span data-stu-id="5bcc7-106">Method</span></span>|<span data-ttu-id="5bcc7-107">说明</span><span class="sxs-lookup"><span data-stu-id="5bcc7-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5bcc7-108">GetExactType 方法</span><span class="sxs-lookup"><span data-stu-id="5bcc7-108">GetExactType Method</span></span>](icordebugvalue2-getexacttype-method.md)|<span data-ttu-id="5bcc7-109">获取一个接口指针，该指针指向 `ICorDebugType` 表示 <xref:System.Type> 此值的的对象。</span><span class="sxs-lookup"><span data-stu-id="5bcc7-109">Gets an interface pointer to an `ICorDebugType` object that represents the <xref:System.Type> of this value.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5bcc7-110">备注</span><span class="sxs-lookup"><span data-stu-id="5bcc7-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="5bcc7-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="5bcc7-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5bcc7-112">要求</span><span class="sxs-lookup"><span data-stu-id="5bcc7-112">Requirements</span></span>  

 <span data-ttu-id="5bcc7-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5bcc7-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5bcc7-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5bcc7-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5bcc7-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5bcc7-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5bcc7-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5bcc7-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5bcc7-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="5bcc7-117">See also</span></span>

- [<span data-ttu-id="5bcc7-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="5bcc7-118">Debugging Interfaces</span></span>](debugging-interfaces.md)

- [<span data-ttu-id="5bcc7-119">ICorDebugValue3 接口</span><span class="sxs-lookup"><span data-stu-id="5bcc7-119">ICorDebugValue3 Interface</span></span>](icordebugvalue3-interface.md)
