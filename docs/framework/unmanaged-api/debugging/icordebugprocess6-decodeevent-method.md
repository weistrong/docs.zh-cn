---
description: 了解详细信息： ICorDebugProcess6：:D ecodeEvent 方法
title: ICorDebugProcess6::DecodeEvent 方法
ms.date: 03/30/2017
ms.assetid: 1453bc0c-6e0d-4d5a-b176-22607f8a3e6c
ms.openlocfilehash: 241b24335f96a250156effde34683c8f32a47e3f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746212"
---
# <a name="icordebugprocess6decodeevent-method"></a><span data-ttu-id="9093c-103">ICorDebugProcess6::DecodeEvent 方法</span><span class="sxs-lookup"><span data-stu-id="9093c-103">ICorDebugProcess6::DecodeEvent Method</span></span>

<span data-ttu-id="9093c-104">对封装于特殊构造的本机异常调试事件有效载荷中的托管调试事件进行解码。</span><span class="sxs-lookup"><span data-stu-id="9093c-104">Decodes managed debug events that have been encapsulated in the payload of specially crafted native exception debug events.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9093c-105">语法</span><span class="sxs-lookup"><span data-stu-id="9093c-105">Syntax</span></span>  
  
```cpp  
HRESULT DecodeEvent(  
        [in, length_is(countBytes), size_is(countBytes)]  const BYTE pRecord[],  
        [in] DWORD countBytes,  
        [in] CorDebugRecordFormat format,  
        [in] DWORD dwFlags,
        [in] DWORD dwThreadId,
        [out] ICorDebugDebugEvent **ppEvent  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9093c-106">参数</span><span class="sxs-lookup"><span data-stu-id="9093c-106">Parameters</span></span>  

 `pRecord`  
 <span data-ttu-id="9093c-107">[输入] 包含托管调试事件相关信息的本机异常调试事件中的字节数组指针。</span><span class="sxs-lookup"><span data-stu-id="9093c-107">[in] A pointer to a byte array from a native exception debug event that includes information about a managed debug event.</span></span>  
  
 `countBytes`  
 <span data-ttu-id="9093c-108">[输入] `pRecord` 字节数组中的元素数量。</span><span class="sxs-lookup"><span data-stu-id="9093c-108">[in] The number of elements in the `pRecord` byte array.</span></span>  
  
 `format`  
 <span data-ttu-id="9093c-109">中 [CorDebugRecordFormat](cordebugrecordformat-enumeration.md) 枚举成员，用于指定非托管调试事件的格式。</span><span class="sxs-lookup"><span data-stu-id="9093c-109">[in] A [CorDebugRecordFormat](cordebugrecordformat-enumeration.md) enumeration member that specifies the format of the unmanaged debug event.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="9093c-110">[输入] 位域依赖于目标体系结构并指定调试事件相关的其他信息。</span><span class="sxs-lookup"><span data-stu-id="9093c-110">[in] A bit field that depends on the target architecture and that specifies additional information about the debug event.</span></span> <span data-ttu-id="9093c-111">对于 Windows 系统，它可以是 [CorDebugDecodeEventFlagsWindows](cordebugdecodeeventflagswindows-enumeration.md) 枚举的成员。</span><span class="sxs-lookup"><span data-stu-id="9093c-111">For Windows systems, it can be a member of the [CorDebugDecodeEventFlagsWindows](cordebugdecodeeventflagswindows-enumeration.md) enumeration.</span></span>  
  
 `dwThreadId`  
 <span data-ttu-id="9093c-112">[输入] 引发异常的线程的操作系统识别符。</span><span class="sxs-lookup"><span data-stu-id="9093c-112">[in] The operating system identifier of the thread on which the exception was thrown.</span></span>  
  
 `ppEvent`  
 <span data-ttu-id="9093c-113">弄指向表示已解码的托管调试事件的 [ICorDebugDebugEvent](icordebugdebugevent-interface.md) 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="9093c-113">[out] A pointer to the address of an [ICorDebugDebugEvent](icordebugdebugevent-interface.md) object that represents a decoded managed debug event.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9093c-114">备注</span><span class="sxs-lookup"><span data-stu-id="9093c-114">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="9093c-115">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="9093c-115">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9093c-116">要求</span><span class="sxs-lookup"><span data-stu-id="9093c-116">Requirements</span></span>  

 <span data-ttu-id="9093c-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9093c-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9093c-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9093c-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9093c-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9093c-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9093c-120">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9093c-120">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9093c-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="9093c-121">See also</span></span>

- [<span data-ttu-id="9093c-122">“ICor调试进程6”接口</span><span class="sxs-lookup"><span data-stu-id="9093c-122">ICorDebugProcess6 Interface</span></span>](icordebugprocess6-interface.md)
- [<span data-ttu-id="9093c-123">调试接口</span><span class="sxs-lookup"><span data-stu-id="9093c-123">Debugging Interfaces</span></span>](debugging-interfaces.md)
