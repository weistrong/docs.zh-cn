---
description: 了解详细信息： ICorDebugDataTarget2：： EnumerateThreadIDs 方法
title: ICorDebugDataTarget2::EnumerateThreadIDs 方法
ms.date: 03/30/2017
ms.assetid: af02460f-2a45-496e-bc4e-a1ac4f80fe11
ms.openlocfilehash: 5bbda67e6c6de81e9de566a68f772f324d79b92f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710551"
---
# <a name="icordebugdatatarget2enumeratethreadids-method"></a><span data-ttu-id="22285-103">ICorDebugDataTarget2::EnumerateThreadIDs 方法</span><span class="sxs-lookup"><span data-stu-id="22285-103">ICorDebugDataTarget2::EnumerateThreadIDs Method</span></span>

<span data-ttu-id="22285-104">返回一组活动线程 ID。</span><span class="sxs-lookup"><span data-stu-id="22285-104">Returns a list of active thread IDs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22285-105">语法</span><span class="sxs-lookup"><span data-stu-id="22285-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateThreadIDs(  
    [in] ULONG32 cThreadIds,
    [out] ULONG32 *pcThreadIds,
    [out, size_is(cThreadIds), length_is(*pcThreadIds)] ULONG32 pThreadIds[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="22285-106">参数</span><span class="sxs-lookup"><span data-stu-id="22285-106">Parameters</span></span>  

 <span data-ttu-id="22285-107">cThreadID</span><span class="sxs-lookup"><span data-stu-id="22285-107">cThreadIDs</span></span>  
 <span data-ttu-id="22285-108">[输入] 线程 ID 可返回的上限数。</span><span class="sxs-lookup"><span data-stu-id="22285-108">[in] The maximum number of threads whose IDs can be returned.</span></span>  
  
 <span data-ttu-id="22285-109">pcThreadID</span><span class="sxs-lookup"><span data-stu-id="22285-109">pcThreadIds</span></span>  
 <span data-ttu-id="22285-110">[输出] `ULONG32` 指针显示写入 `pThreadIds` 阵列的线程 ID 的实际数目。</span><span class="sxs-lookup"><span data-stu-id="22285-110">[out] A pointer to a `ULONG32` that indicates the actual number of thread IDs written to the `pThreadIds` array.</span></span>  
  
 <span data-ttu-id="22285-111">pThreadID</span><span class="sxs-lookup"><span data-stu-id="22285-111">pThreadIDs</span></span>  
 <span data-ttu-id="22285-112">一组线程标识符。</span><span class="sxs-lookup"><span data-stu-id="22285-112">An array of thread identifiers.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="22285-113">备注</span><span class="sxs-lookup"><span data-stu-id="22285-113">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="22285-114">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="22285-114">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="22285-115">要求</span><span class="sxs-lookup"><span data-stu-id="22285-115">Requirements</span></span>  

 <span data-ttu-id="22285-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。**标头：** Cordebug.idl，Cordebug.idl</span><span class="sxs-lookup"><span data-stu-id="22285-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="22285-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="22285-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="22285-118">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22285-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22285-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="22285-119">See also</span></span>

- [<span data-ttu-id="22285-120">“ICor调试数据目标2”接口</span><span class="sxs-lookup"><span data-stu-id="22285-120">ICorDebugDataTarget2 Interface</span></span>](icordebugdatatarget2-interface.md)
- [<span data-ttu-id="22285-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="22285-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
