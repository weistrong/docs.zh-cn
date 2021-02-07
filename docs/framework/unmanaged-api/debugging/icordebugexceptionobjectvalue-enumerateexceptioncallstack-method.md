---
description: 了解详细信息： ICorDebugExceptionObjectValue：： EnumerateExceptionCallStack 方法
title: ICorDebugExceptionObjectValue::EnumerateExceptionCallStack 方法
ms.date: 03/30/2017
api_name:
- ICorDebugExceptionObjectValue.EnumerateExceptionCallStack
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugExceptionObjectValue::EnumerateExceptionCallStack
helpviewer_keywords:
- EnumerateExceptionCallStack method, ICorDebugExceptionObjectValue interface [.NET Framework debugging]
- ICorDebugExceptionObjectValue::EnumerateExceptionCallStack method [.NET Framework debugging]
ms.assetid: 00c64533-15dd-47f4-bb97-fe80a1ebadef
topic_type:
- apiref
ms.openlocfilehash: 97918d280299fae16eb55185baee19c27d99005b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693273"
---
# <a name="icordebugexceptionobjectvalueenumerateexceptioncallstack-method"></a><span data-ttu-id="f45cc-103">ICorDebugExceptionObjectValue::EnumerateExceptionCallStack 方法</span><span class="sxs-lookup"><span data-stu-id="f45cc-103">ICorDebugExceptionObjectValue::EnumerateExceptionCallStack Method</span></span>

<span data-ttu-id="f45cc-104">获取一个枚举器，该枚举器指向嵌入到异常对象中的调用堆栈。</span><span class="sxs-lookup"><span data-stu-id="f45cc-104">Gets an enumerator to the call stack embedded in an exception object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f45cc-105">语法</span><span class="sxs-lookup"><span data-stu-id="f45cc-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateExceptionCallStack(  
    [out] ICorDebugExceptionObjectCallStackEnum **ppCallStackEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f45cc-106">参数</span><span class="sxs-lookup"><span data-stu-id="f45cc-106">Parameters</span></span>  

 <span data-ttu-id="f45cc-107">ppCallStackEnum</span><span class="sxs-lookup"><span data-stu-id="f45cc-107">ppCallStackEnum</span></span>  
 <span data-ttu-id="f45cc-108">弄指向 [ICorDebugExceptionObjectCallStackEnum](icordebugexceptionobjectcallstackenum-interface.md) 接口对象地址的指针，该对象是托管异常对象的堆栈跟踪枚举器。</span><span class="sxs-lookup"><span data-stu-id="f45cc-108">[out] A pointer to the address of an [ICorDebugExceptionObjectCallStackEnum](icordebugexceptionobjectcallstackenum-interface.md) interface object that is a stack trace enumerator for a managed exception object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f45cc-109">备注</span><span class="sxs-lookup"><span data-stu-id="f45cc-109">Remarks</span></span>  

 <span data-ttu-id="f45cc-110">如果没有可用的调用堆栈信息，则该方法将返回 `S_OK` ，并且 [ICorDebugExceptionObjectCallStackEnum](icordebugexceptionobjectcallstackenum-interface.md) 是长度为0的有效枚举器。</span><span class="sxs-lookup"><span data-stu-id="f45cc-110">If no call stack information is available, the method returns `S_OK`, and [ICorDebugExceptionObjectCallStackEnum](icordebugexceptionobjectcallstackenum-interface.md) is a valid enumerator with a length of 0.</span></span> <span data-ttu-id="f45cc-111">如果该方法无法检索堆栈跟踪信息，则返回值为 `E_FAIL` ，并且不返回任何枚举器。</span><span class="sxs-lookup"><span data-stu-id="f45cc-111">If the method is unable to retrieve stack trace information, the return value is `E_FAIL` and no enumerator is returned.</span></span>  
  
 <span data-ttu-id="f45cc-112">[ICorDebugExceptionObjectCallStackEnum](icordebugexceptionobjectcallstackenum-interface.md)对象负责从 exception 对象的字段解码堆栈跟踪数据 `_stackTrace` 。</span><span class="sxs-lookup"><span data-stu-id="f45cc-112">The [ICorDebugExceptionObjectCallStackEnum](icordebugexceptionobjectcallstackenum-interface.md) object is responsible for decoding the stack trace data from the `_stackTrace` field of the exception object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f45cc-113">要求</span><span class="sxs-lookup"><span data-stu-id="f45cc-113">Requirements</span></span>  

 <span data-ttu-id="f45cc-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f45cc-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f45cc-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f45cc-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f45cc-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f45cc-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f45cc-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f45cc-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f45cc-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="f45cc-118">See also</span></span>

- [<span data-ttu-id="f45cc-119">ICorDebugExceptionObjectValue 接口</span><span class="sxs-lookup"><span data-stu-id="f45cc-119">ICorDebugExceptionObjectValue Interface</span></span>](icordebugexceptionobjectvalue-interface.md)
- [<span data-ttu-id="f45cc-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="f45cc-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
