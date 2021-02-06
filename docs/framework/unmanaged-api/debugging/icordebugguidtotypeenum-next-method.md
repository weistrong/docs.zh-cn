---
description: 了解详细信息： ICorDebugGuidToTypeEnum：： Next 方法
title: ICorDebugGuidToTypeEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugGuidToTypeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGuidToTypeEnum::Next
helpviewer_keywords:
- ICorDebugGuidToTypeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugGuidToTypeEnum interface [.NET Framework debugging]
ms.assetid: c9937666-8e18-484d-9fe0-b9ac95199530
topic_type:
- apiref
ms.openlocfilehash: 0ab05cc0689c76c0bb185205ea00c5ccebfcbe03
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660994"
---
# <a name="icordebugguidtotypeenumnext-method"></a><span data-ttu-id="94042-103">ICorDebugGuidToTypeEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="94042-103">ICorDebugGuidToTypeEnum::Next Method</span></span>

<span data-ttu-id="94042-104">获取指定数量的 [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) 实例，这些实例将 guid 映射到类型信息。</span><span class="sxs-lookup"><span data-stu-id="94042-104">Gets the specified number of [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) instances that map GUIDs to type information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94042-105">语法</span><span class="sxs-lookup"><span data-stu-id="94042-105">Syntax</span></span>  
  
```cpp  
HRESULT Next(  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched] CorDebugGuidToTypeMapping values[  ],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="94042-106">参数</span><span class="sxs-lookup"><span data-stu-id="94042-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="94042-107">中要检索的 GUID 到类型的映射对象的数量。</span><span class="sxs-lookup"><span data-stu-id="94042-107">[in] The number of GUID-to-type mapping objects to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="94042-108">弄指针的数组，其中每个都指向将 Windows 运行时 GUID 映射到其对应 ICorDebugType 对象的 [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="94042-108">[out] An array of pointers, each of which points to a [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) object that maps a Windows Runtime GUID to its corresponding ICorDebugType object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="94042-109">弄一个指针，指向在中实际返回的 [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) 对象的数目 `values` 。</span><span class="sxs-lookup"><span data-stu-id="94042-109">[out] A pointer to the number of [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) objects actually returned in `values`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="94042-110">备注</span><span class="sxs-lookup"><span data-stu-id="94042-110">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="94042-111">要求</span><span class="sxs-lookup"><span data-stu-id="94042-111">Requirements</span></span>  

 <span data-ttu-id="94042-112">**平台：** Windows 运行时</span><span class="sxs-lookup"><span data-stu-id="94042-112">**Platforms:** Windows Runtime</span></span>  
  
 <span data-ttu-id="94042-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="94042-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="94042-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="94042-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="94042-115">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="94042-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94042-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="94042-116">See also</span></span>

- [<span data-ttu-id="94042-117">ICorDebugGuidToTypeEnum 接口</span><span class="sxs-lookup"><span data-stu-id="94042-117">ICorDebugGuidToTypeEnum Interface</span></span>](icordebugguidtotypeenum-interface.md)
- [<span data-ttu-id="94042-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="94042-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
