---
description: 了解详细信息： ICorDebugAppDomain2 接口
title: ICorDebugAppDomain2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain2
helpviewer_keywords:
- ICorDebugAppDomain2 interface [.NET Framework debugging]
ms.assetid: 314d29f3-feb0-4a92-9530-b569c280cc31
topic_type:
- apiref
ms.openlocfilehash: 2f2fcc4166a0c825abaa04392f9905d17e286803
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754181"
---
# <a name="icordebugappdomain2-interface"></a><span data-ttu-id="91972-103">ICorDebugAppDomain2 接口</span><span class="sxs-lookup"><span data-stu-id="91972-103">ICorDebugAppDomain2 Interface</span></span>

<span data-ttu-id="91972-104">提供使用数组、指针、函数指针和引用类型的方法。</span><span class="sxs-lookup"><span data-stu-id="91972-104">Provides methods to work with arrays, pointers, function pointers, and reference types.</span></span> <span data-ttu-id="91972-105">此接口是 ICorDebugAppDomain 接口的扩展。</span><span class="sxs-lookup"><span data-stu-id="91972-105">This interface is an extension of the ICorDebugAppDomain interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="91972-106">方法</span><span class="sxs-lookup"><span data-stu-id="91972-106">Methods</span></span>  
  
|<span data-ttu-id="91972-107">方法</span><span class="sxs-lookup"><span data-stu-id="91972-107">Method</span></span>|<span data-ttu-id="91972-108">说明</span><span class="sxs-lookup"><span data-stu-id="91972-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="91972-109">GetArrayOrPointerType 方法</span><span class="sxs-lookup"><span data-stu-id="91972-109">GetArrayOrPointerType Method</span></span>](icordebugappdomain2-getarrayorpointertype-method.md)|<span data-ttu-id="91972-110">获取指定类型的数组，或指定类型的指针或引用。</span><span class="sxs-lookup"><span data-stu-id="91972-110">Gets an array of the specified type, or a pointer or reference to the specified type.</span></span>|  
|[<span data-ttu-id="91972-111">GetFunctionPointerType</span><span class="sxs-lookup"><span data-stu-id="91972-111">GetFunctionPointerType</span></span>](icordebugappdomain2-getfunctionpointertype-method.md)|<span data-ttu-id="91972-112">获取一个指针，该指针指向具有给定签名的函数。</span><span class="sxs-lookup"><span data-stu-id="91972-112">Gets a pointer to a function that has a given signature.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="91972-113">备注</span><span class="sxs-lookup"><span data-stu-id="91972-113">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="91972-114">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="91972-114">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="91972-115">要求</span><span class="sxs-lookup"><span data-stu-id="91972-115">Requirements</span></span>  

 <span data-ttu-id="91972-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="91972-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="91972-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="91972-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="91972-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="91972-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="91972-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="91972-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="91972-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="91972-120">See also</span></span>

- [<span data-ttu-id="91972-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="91972-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
