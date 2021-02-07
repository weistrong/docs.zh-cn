---
description: 了解详细信息： ICorDebugAppDomain4：： GetObjectForCCW 方法
title: ICorDebugAppDomain4::GetObjectForCCW 方法
ms.date: 03/30/2017
ms.assetid: 2cacdb85-e7b8-42e7-b310-c3e8c22e5d33
ms.openlocfilehash: 5ba4923c933d02f5d6ad5c1fd8c4d0e2ddb410d3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754129"
---
# <a name="icordebugappdomain4getobjectforccw-method"></a><span data-ttu-id="3d715-103">ICorDebugAppDomain4::GetObjectForCCW 方法</span><span class="sxs-lookup"><span data-stu-id="3d715-103">ICorDebugAppDomain4::GetObjectForCCW Method</span></span>

<span data-ttu-id="3d715-104">从 COM 可调用包装器 (CCW) 指针获取托管对象。</span><span class="sxs-lookup"><span data-stu-id="3d715-104">Gets a managed object from a COM callable wrapper (CCW) pointer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3d715-105">语法</span><span class="sxs-lookup"><span data-stu-id="3d715-105">Syntax</span></span>  
  
```cpp  
HRESULT GetObjectForCCW(  
   [in]CORDB_ADDRESS ccwPointer,
   [out]ICorDebugValue **ppManagedObject  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3d715-106">参数</span><span class="sxs-lookup"><span data-stu-id="3d715-106">Parameters</span></span>  

 `ccwPointer`  
 <span data-ttu-id="3d715-107">[in] COM 可调用包装器 (CCW) 指针。</span><span class="sxs-lookup"><span data-stu-id="3d715-107">[in] A COM callable wrapper (CCW) pointer.</span></span>  
  
 `ppManagedObject`  
 <span data-ttu-id="3d715-108">弄一个指向 "ICorDebugValue" 对象地址的指针，该对象表示与给定的 CCW 指针相对应的托管对象。</span><span class="sxs-lookup"><span data-stu-id="3d715-108">[out] A pointer to the address of an "ICorDebugValue" object that represents the managed object that corresponds to the given CCW pointer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3d715-109">备注</span><span class="sxs-lookup"><span data-stu-id="3d715-109">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3d715-110">要求</span><span class="sxs-lookup"><span data-stu-id="3d715-110">Requirements</span></span>  

 <span data-ttu-id="3d715-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3d715-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3d715-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3d715-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3d715-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3d715-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3d715-114">**.NET Framework 版本：**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3d715-114">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3d715-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="3d715-115">See also</span></span>

- [<span data-ttu-id="3d715-116">ICorDebugAppDomain4 接口</span><span class="sxs-lookup"><span data-stu-id="3d715-116">ICorDebugAppDomain4 Interface</span></span>](icordebugappdomain4-interface.md)
- [<span data-ttu-id="3d715-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="3d715-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
