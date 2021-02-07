---
description: 了解详细信息： ICorProfilerInfo7 接口
title: ICorProfilerInfo7 接口
ms.date: 03/30/2017
ms.assetid: cf37c462-73c5-412a-a7f8-bb26ca746313
ms.openlocfilehash: 7a33472d5562ad57d38291c64f8da7021ae2fe91
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737072"
---
# <a name="icorprofilerinfo7-interface"></a><span data-ttu-id="22929-103">ICorProfilerInfo7 接口</span><span class="sxs-lookup"><span data-stu-id="22929-103">ICorProfilerInfo7 Interface</span></span>

<span data-ttu-id="22929-104">[仅在 .NET Framework 4.6.1 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="22929-104">[Supported in the .NET Framework 4.6.1 and later versions]</span></span>  
  
 <span data-ttu-id="22929-105">[ICorProfilerInfo6](icorprofilerinfo6-interface.md)的子类，它提供了一种方法，用于将新定义的元数据应用于模块，并提供对内存中符号流的访问。</span><span class="sxs-lookup"><span data-stu-id="22929-105">A subclass of [ICorProfilerInfo6](icorprofilerinfo6-interface.md) that provides a method to apply newly defined metadata to a module and that provides access to an in-memory symbol stream.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="22929-106">方法</span><span class="sxs-lookup"><span data-stu-id="22929-106">Methods</span></span>  
  
|<span data-ttu-id="22929-107">方法</span><span class="sxs-lookup"><span data-stu-id="22929-107">Method</span></span>|<span data-ttu-id="22929-108">说明</span><span class="sxs-lookup"><span data-stu-id="22929-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="22929-109">ApplyMetaData 方法</span><span class="sxs-lookup"><span data-stu-id="22929-109">ApplyMetaData Method</span></span>](icorprofilerinfo7-applymetadata-method.md)|<span data-ttu-id="22929-110">将方法的新定义的元数据应用于 `IMetadataEmit::Define*` 指定的模块。</span><span class="sxs-lookup"><span data-stu-id="22929-110">Applies the metadata newly defined by the `IMetadataEmit::Define*` methods to a specified module.</span></span>|  
|[<span data-ttu-id="22929-111">GetInMemorySymbolsLength 方法</span><span class="sxs-lookup"><span data-stu-id="22929-111">GetInMemorySymbolsLength Method</span></span>](icorprofilerinfo7-getinmemorysymbolslength-method.md)|<span data-ttu-id="22929-112">返回内存中符号流的长度。</span><span class="sxs-lookup"><span data-stu-id="22929-112">Returns the length of an in-memory symbol stream.</span></span>|  
|[<span data-ttu-id="22929-113">ReadInMemorySymbols</span><span class="sxs-lookup"><span data-stu-id="22929-113">ReadInMemorySymbols</span></span>](icorprofilerinfo7-readinmemorysymbols.md)|<span data-ttu-id="22929-114">从内存中的符号流中读取字节。</span><span class="sxs-lookup"><span data-stu-id="22929-114">Reads bytes from an in-memory symbol stream.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="22929-115">要求</span><span class="sxs-lookup"><span data-stu-id="22929-115">Requirements</span></span>  

 <span data-ttu-id="22929-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="22929-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22929-117">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="22929-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="22929-118">**.NET Framework 版本：**[!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22929-118">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22929-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="22929-119">See also</span></span>

- [<span data-ttu-id="22929-120">分析接口</span><span class="sxs-lookup"><span data-stu-id="22929-120">Profiling Interfaces</span></span>](profiling-interfaces.md)
