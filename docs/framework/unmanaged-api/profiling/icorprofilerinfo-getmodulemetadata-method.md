---
description: 了解详细信息： ICorProfilerInfo：： GetModuleMetaData 方法
title: ICorProfilerInfo::GetModuleMetaData 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetModuleMetaData
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetModuleMetaData
helpviewer_keywords:
- GetModuleMetaData method [.NET Framework profiling]
- ICorProfilerInfo::GetModuleMetaData method [.NET Framework profiling]
ms.assetid: 7a439d92-348a-44dd-b60f-cad7cba56379
topic_type:
- apiref
ms.openlocfilehash: ff0fb0563b041fcb3cf63438874724c8236d6081
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647175"
---
# <a name="icorprofilerinfogetmodulemetadata-method"></a><span data-ttu-id="1ef93-103">ICorProfilerInfo::GetModuleMetaData 方法</span><span class="sxs-lookup"><span data-stu-id="1ef93-103">ICorProfilerInfo::GetModuleMetaData Method</span></span>

<span data-ttu-id="1ef93-104">获取映射到指定模块的元数据接口实例。</span><span class="sxs-lookup"><span data-stu-id="1ef93-104">Gets a metadata interface instance that maps to the specified module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ef93-105">语法</span><span class="sxs-lookup"><span data-stu-id="1ef93-105">Syntax</span></span>  
  
```cpp  
HRESULT GetModuleMetaData(  
    [in]  ModuleID moduleId,  
    [in]  DWORD    dwOpenFlags,  
    [in]  REFIID   riid,  
    [out] IUnknown **ppOut);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1ef93-106">参数</span><span class="sxs-lookup"><span data-stu-id="1ef93-106">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="1ef93-107">中接口实例将映射到的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="1ef93-107">[in] The ID of the module to which the interface instance will be mapped.</span></span>  
  
 `dwOpenFlags`  
 <span data-ttu-id="1ef93-108">中 [CorOpenFlags](../metadata/coropenflags-enumeration.md) 枚举的一个值，该值指定用于打开清单文件的模式。</span><span class="sxs-lookup"><span data-stu-id="1ef93-108">[in] A value of the [CorOpenFlags](../metadata/coropenflags-enumeration.md) enumeration that specifies the mode for opening manifest files.</span></span> <span data-ttu-id="1ef93-109">只有 `ofRead` 、 `ofWrite` 和 `ofNoTransform` 位有效。</span><span class="sxs-lookup"><span data-stu-id="1ef93-109">Only the `ofRead`, `ofWrite` and `ofNoTransform` bits are valid.</span></span>  
  
 `riid`  
 <span data-ttu-id="1ef93-110">中将检索其实例的元数据接口的引用 ID (GUID) 。</span><span class="sxs-lookup"><span data-stu-id="1ef93-110">[in] The reference ID (GUID) of the metadata interface whose instance will be retrieved.</span></span> <span data-ttu-id="1ef93-111">有关接口列表，请参阅 [元数据接口](../metadata/metadata-interfaces.md) 。</span><span class="sxs-lookup"><span data-stu-id="1ef93-111">See [Metadata Interfaces](../metadata/metadata-interfaces.md) for a list of the interfaces.</span></span>  
  
 `ppOut`  
 <span data-ttu-id="1ef93-112">弄指向元数据接口实例的地址的指针。</span><span class="sxs-lookup"><span data-stu-id="1ef93-112">[out] A pointer to the address of the metadata interface instance.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1ef93-113">备注</span><span class="sxs-lookup"><span data-stu-id="1ef93-113">Remarks</span></span>  

 <span data-ttu-id="1ef93-114">你可能要求在读/写模式下打开元数据，但这会导致程序的元数据执行速度变慢，因为对元数据所做的更改不会因为它们来自编译器而进行优化。</span><span class="sxs-lookup"><span data-stu-id="1ef93-114">You may ask for the metadata to be opened in read/write mode, but this will result in slower metadata execution of the program, because changes made to the metadata cannot be optimized as they were from the compiler.</span></span>  
  
 <span data-ttu-id="1ef93-115">某些模块 (例如资源模块) 没有元数据。</span><span class="sxs-lookup"><span data-stu-id="1ef93-115">Some modules (such as resource modules) have no metadata.</span></span> <span data-ttu-id="1ef93-116">在这些情况下， `GetModuleMetaData` 将返回的 HRESULT 值 S_FALSE，并在 \* 中返回 null `ppOut` 。</span><span class="sxs-lookup"><span data-stu-id="1ef93-116">In those cases, `GetModuleMetaData` will return an HRESULT value of S_FALSE, and a null in \*`ppOut`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1ef93-117">要求</span><span class="sxs-lookup"><span data-stu-id="1ef93-117">Requirements</span></span>  

 <span data-ttu-id="1ef93-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1ef93-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1ef93-119">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="1ef93-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="1ef93-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1ef93-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1ef93-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1ef93-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ef93-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="1ef93-122">See also</span></span>

- [<span data-ttu-id="1ef93-123">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="1ef93-123">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
