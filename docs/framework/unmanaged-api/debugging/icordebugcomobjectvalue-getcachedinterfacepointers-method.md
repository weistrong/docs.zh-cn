---
description: 了解详细信息： ICorDebugComObjectValue：： GetCachedInterfacePointers 方法
title: ICorDebugComObjectValue::GetCachedInterfacePointers 方法
ms.date: 03/30/2017
api_name:
- ICorDebugComObjectValue::GetCachedInterfacePointers
api_location:
- mscordbi.dll
f1_keywords:
- ICorDebugComObjectValue::GetCachedInterfacePointers
helpviewer_keywords:
- ICorDebugComObjectValue::GetCachedInterfacePointers method [.NET Framework debugging]
- GetCachedInterfacePointers method, ICorDebugComObjectValue interface [.NET Framework debugging]
ms.assetid: 08dbd558-bd39-4263-94c2-71e70687aaf0
topic_type:
- apiref
ms.openlocfilehash: 737d71f6aa903a3dfa97f583b47a322ec074147f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710850"
---
# <a name="icordebugcomobjectvaluegetcachedinterfacepointers-method"></a><span data-ttu-id="3b879-103">ICorDebugComObjectValue::GetCachedInterfacePointers 方法</span><span class="sxs-lookup"><span data-stu-id="3b879-103">ICorDebugComObjectValue::GetCachedInterfacePointers Method</span></span>

<span data-ttu-id="3b879-104">获取 (RCW) 缓存在当前运行时可调用包装上的原始接口指针。</span><span class="sxs-lookup"><span data-stu-id="3b879-104">Gets the raw interface pointers cached on the current runtime callable wrapper (RCW).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b879-105">语法</span><span class="sxs-lookup"><span data-stu-id="3b879-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCachedInterfacePointers(  
    [in] BOOL bIInspectableOnly,  
    [in] ULONG32 celt,  
    [out] ULONG32 *pceltFetched,  
    [out, size_is(celt), length_is(*pceltFetched) CORDB_ADDRESS *ptrs);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3b879-106">参数</span><span class="sxs-lookup"><span data-stu-id="3b879-106">Parameters</span></span>  

 `bIInspectableOnly`  
 <span data-ttu-id="3b879-107">中一个值，该值指示方法是只返回 (接口) 的 Windows 运行时接口 `IInspectable` ，还是返回由运行时可调用包装 (RCW) 缓存的所有 COM 接口。</span><span class="sxs-lookup"><span data-stu-id="3b879-107">[in] A value that indicates whether the method will return only Windows Runtime interfaces (`IInspectable` interfaces) or all COM interfaces that are cached by the runtime callable wrapper (RCW).</span></span>  
  
 `celt`  
 <span data-ttu-id="3b879-108">中要检索其地址的对象的数目。</span><span class="sxs-lookup"><span data-stu-id="3b879-108">[in] The number of objects whose addresses are to be retrieved.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="3b879-109">弄一个指针，指向 `CORDB_ADDRESS` 中实际返回的值的数目 `ptrs` 。</span><span class="sxs-lookup"><span data-stu-id="3b879-109">[out] A pointer to the number of `CORDB_ADDRESS` values actually returned in `ptrs`.</span></span>  
  
 `ptrs`  
 <span data-ttu-id="3b879-110">一个指针，指向 `CORDB_ADDRESS` 包含缓存接口对象地址的值数组的起始地址。</span><span class="sxs-lookup"><span data-stu-id="3b879-110">A pointer to the starting address of an array of `CORDB_ADDRESS` values that contain the addresses of cached interface objects.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3b879-111">备注</span><span class="sxs-lookup"><span data-stu-id="3b879-111">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b879-112">要求</span><span class="sxs-lookup"><span data-stu-id="3b879-112">Requirements</span></span>  

 <span data-ttu-id="3b879-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3b879-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3b879-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3b879-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3b879-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3b879-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3b879-116">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3b879-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b879-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="3b879-117">See also</span></span>

- [<span data-ttu-id="3b879-118">ICorDebugComObjectValue 接口</span><span class="sxs-lookup"><span data-stu-id="3b879-118">ICorDebugComObjectValue Interface</span></span>](icordebugcomobjectvalue-interface.md)
- [<span data-ttu-id="3b879-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="3b879-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
