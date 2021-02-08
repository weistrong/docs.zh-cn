---
description: 了解详细信息： ICorProfilerInfo：： GetTokenAndMetadataFromFunction 方法
title: ICorProfilerInfo::GetTokenAndMetadataFromFunction 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetTokenAndMetadataFromFunction
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetTokenAndMetadataFromFunction
helpviewer_keywords:
- ICorProfilerInfo::GetTokenAndMetadataFromFunction method [.NET Framework profiling]
- GetTokenAndMetadataFromFunction method [.NET Framework profiling]
ms.assetid: e525aa16-c923-4b16-833b-36f1f0dd70fc
topic_type:
- apiref
ms.openlocfilehash: 0cea6564df15c7a7f4c46097714cc0956002599b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783841"
---
# <a name="icorprofilerinfogettokenandmetadatafromfunction-method"></a><span data-ttu-id="a0b88-103">ICorProfilerInfo::GetTokenAndMetadataFromFunction 方法</span><span class="sxs-lookup"><span data-stu-id="a0b88-103">ICorProfilerInfo::GetTokenAndMetadataFromFunction Method</span></span>

<span data-ttu-id="a0b88-104">获取可用于指定函数的标记的元数据标记和元数据接口实例。</span><span class="sxs-lookup"><span data-stu-id="a0b88-104">Gets the metadata token and a metadata interface instance that can be used against the token for the specified function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0b88-105">语法</span><span class="sxs-lookup"><span data-stu-id="a0b88-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTokenAndMetaDataFromFunction(  
    [in]  FunctionID functionId,  
    [in]  REFIID     riid,  
    [out] IUnknown   **ppImport,  
    [out] mdToken    *pToken);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a0b88-106">参数</span><span class="sxs-lookup"><span data-stu-id="a0b88-106">Parameters</span></span>  

 `functionId`  
 <span data-ttu-id="a0b88-107">中要获取其元数据标记和元数据接口的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="a0b88-107">[in] The ID of the function for which to get the metadata token and metadata interface.</span></span>  
  
 `riid`  
 <span data-ttu-id="a0b88-108">中要获取其实例的元数据接口的引用 ID。</span><span class="sxs-lookup"><span data-stu-id="a0b88-108">[in] The reference ID of the metadata interface to get the instance of.</span></span>  
  
 `ppImport`  
 <span data-ttu-id="a0b88-109">弄一个指针，指向可用于指定函数的标记的元数据接口实例的地址。</span><span class="sxs-lookup"><span data-stu-id="a0b88-109">[out] A pointer to the address of the metadata interface instance that can be used against the token for the specified function.</span></span>  
  
 `pToken`  
 <span data-ttu-id="a0b88-110">弄指向指定函数的元数据标记的指针。</span><span class="sxs-lookup"><span data-stu-id="a0b88-110">[out] A pointer to the metadata token for the specified function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a0b88-111">要求</span><span class="sxs-lookup"><span data-stu-id="a0b88-111">Requirements</span></span>  

 <span data-ttu-id="a0b88-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a0b88-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a0b88-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a0b88-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a0b88-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a0b88-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a0b88-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a0b88-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0b88-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="a0b88-116">See also</span></span>

- [<span data-ttu-id="a0b88-117">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="a0b88-117">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
