---
description: 了解详细信息： ICorProfilerInfo9：： GetILToNativeMapping3 方法
title: ICorProfilerInfo9::GetILToNativeMapping3
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo9.GetILToNativeMapping3
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: 867375d57f9d166ed08bf68ada81fb5cdbb8afe3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646512"
---
# <a name="icorprofilerinfo9getiltonativemapping3-method"></a><span data-ttu-id="546f9-103">ICorProfilerInfo9：： GetILToNativeMapping3 方法</span><span class="sxs-lookup"><span data-stu-id="546f9-103">ICorProfilerInfo9::GetILToNativeMapping3 Method</span></span>

<span data-ttu-id="546f9-104">给定本机代码起始地址，返回此实时编译版本的代码的本机到 IL 映射信息。</span><span class="sxs-lookup"><span data-stu-id="546f9-104">Given the native code start address, returns the native to IL mapping information for this jitted version of the code.</span></span>

## <a name="syntax"></a><span data-ttu-id="546f9-105">语法</span><span class="sxs-lookup"><span data-stu-id="546f9-105">Syntax</span></span>

```cpp
HRESULT GetILToNativeMapping3( [in]  UINT_PTR pNativeCodeStartAddress,
                               [in]  ULONG32 cMap,
                               [out] ULONG32 *pcMap,
                               [out] COR_DEBUG_IL_TO_NATIVE_MAP map[]);
```

## <a name="parameters"></a><span data-ttu-id="546f9-106">参数</span><span class="sxs-lookup"><span data-stu-id="546f9-106">Parameters</span></span>

- `pNativeCodeStartAddress`

  <span data-ttu-id="546f9-107">\[in] 指向本机函数开头的指针。</span><span class="sxs-lookup"><span data-stu-id="546f9-107">\[in] A pointer to the start of a native function.</span></span>

- `cMap`

  <span data-ttu-id="546f9-108">\[in] 数组的最大大小 `map` 。</span><span class="sxs-lookup"><span data-stu-id="546f9-108">\[in] The maximum size of the `map` array.</span></span>

- `pcMap`

  <span data-ttu-id="546f9-109">\[out] 可用 COR_DEBUG_IL_TO_NATIVE_MAP 结构的总数。</span><span class="sxs-lookup"><span data-stu-id="546f9-109">\[out] The total number of available COR_DEBUG_IL_TO_NATIVE_MAP structures.</span></span>

- `map`

  <span data-ttu-id="546f9-110">\[out] [COR_DEBUG_IL_TO_NATIVE_MAP](../debugging/cor-debug-il-to-native-map-structure.md) 结构的数组，其中每个结构都指定了偏移量。</span><span class="sxs-lookup"><span data-stu-id="546f9-110">\[out] An array of [COR_DEBUG_IL_TO_NATIVE_MAP](../debugging/cor-debug-il-to-native-map-structure.md) structures, each of which specifies the offsets.</span></span> <span data-ttu-id="546f9-111">`GetILToNativeMapping3` 方法返回后，`map` 将包含部分或全部 `COR_DEBUG_IL_TO_NATIVE_MAP` 结构。</span><span class="sxs-lookup"><span data-stu-id="546f9-111">After the `GetILToNativeMapping3` method returns, `map` will contain some or all of the `COR_DEBUG_IL_TO_NATIVE_MAP` structures.</span></span>

## <a name="remarks"></a><span data-ttu-id="546f9-112">备注</span><span class="sxs-lookup"><span data-stu-id="546f9-112">Remarks</span></span>

<span data-ttu-id="546f9-113">当启用分层编译时，一个方法可能有多个本机代码体。</span><span class="sxs-lookup"><span data-stu-id="546f9-113">When tiered compilation is enabled, a method may have more than one native code body.</span></span> <span data-ttu-id="546f9-114">[ICorProfilerInfo9：： GetNativeCodeStartAddresses](icorprofilerinfo9-getnativecodestartaddresses-method.md) 将返回所有本机代码正文的开始地址。</span><span class="sxs-lookup"><span data-stu-id="546f9-114">[ICorProfilerInfo9::GetNativeCodeStartAddresses](icorprofilerinfo9-getnativecodestartaddresses-method.md) will return the start addresses for all of the native code bodies.</span></span>

## <a name="requirements"></a><span data-ttu-id="546f9-115">要求</span><span class="sxs-lookup"><span data-stu-id="546f9-115">Requirements</span></span>

<span data-ttu-id="546f9-116">**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="546f9-116">**Platforms:** See [.NET Core supported operating systems](../../../core/install/windows.md?pivots=os-windows).</span></span>

<span data-ttu-id="546f9-117">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="546f9-117">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="546f9-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="546f9-118">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="546f9-119">**.NET Framework 版本：**[!INCLUDE[net_core_22](../../../../includes/net-core-22-md.md)]</span><span class="sxs-lookup"><span data-stu-id="546f9-119">**.NET Framework Versions:** [!INCLUDE[net_core_22](../../../../includes/net-core-22-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="546f9-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="546f9-120">See also</span></span>

- [<span data-ttu-id="546f9-121">ICorProfilerInfo9 接口</span><span class="sxs-lookup"><span data-stu-id="546f9-121">ICorProfilerInfo9 Interface</span></span>](icorprofilerinfo9-interface.md)
