---
description: 了解详细信息： ICorDebugStringValue 接口
title: ICorDebugStringValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugStringValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStringValue
helpviewer_keywords:
- ICorDebugStringValue interface [.NET Framework debugging]
ms.assetid: bf84d0af-53e1-4c04-bc5b-7e5f81ba2cc2
topic_type:
- apiref
ms.openlocfilehash: b4e762d8c0a62c1b76b59364e9d29c4b8d2386fa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717324"
---
# <a name="icordebugstringvalue-interface"></a><span data-ttu-id="b28e3-103">ICorDebugStringValue 接口</span><span class="sxs-lookup"><span data-stu-id="b28e3-103">ICorDebugStringValue Interface</span></span>

<span data-ttu-id="b28e3-104">应用于字符串值的 ICorDebugHeapValue 的子类。</span><span class="sxs-lookup"><span data-stu-id="b28e3-104">A subclass of ICorDebugHeapValue that applies to string values.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b28e3-105">方法</span><span class="sxs-lookup"><span data-stu-id="b28e3-105">Methods</span></span>  
  
|<span data-ttu-id="b28e3-106">方法</span><span class="sxs-lookup"><span data-stu-id="b28e3-106">Method</span></span>|<span data-ttu-id="b28e3-107">说明</span><span class="sxs-lookup"><span data-stu-id="b28e3-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b28e3-108">GetLength 方法</span><span class="sxs-lookup"><span data-stu-id="b28e3-108">GetLength Method</span></span>](icordebugstringvalue-getlength-method.md)|<span data-ttu-id="b28e3-109">获取此引用的字符串中的字符数 `ICorDebugStringValue` 。</span><span class="sxs-lookup"><span data-stu-id="b28e3-109">Gets the number of characters in the string referenced by this `ICorDebugStringValue`.</span></span>|  
|[<span data-ttu-id="b28e3-110">GetString 方法</span><span class="sxs-lookup"><span data-stu-id="b28e3-110">GetString Method</span></span>](icordebugstringvalue-getstring-method.md)|<span data-ttu-id="b28e3-111">获取此引用的字符串 `ICorDebugStringValue` 。</span><span class="sxs-lookup"><span data-stu-id="b28e3-111">Gets the string referenced by this `ICorDebugStringValue`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b28e3-112">备注</span><span class="sxs-lookup"><span data-stu-id="b28e3-112">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b28e3-113">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="b28e3-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b28e3-114">要求</span><span class="sxs-lookup"><span data-stu-id="b28e3-114">Requirements</span></span>  

 <span data-ttu-id="b28e3-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b28e3-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b28e3-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b28e3-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b28e3-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b28e3-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b28e3-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b28e3-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b28e3-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="b28e3-119">See also</span></span>

- [<span data-ttu-id="b28e3-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="b28e3-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
