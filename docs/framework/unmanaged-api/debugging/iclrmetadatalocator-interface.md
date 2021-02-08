---
description: 了解详细信息： ICLRMetadataLocator 接口
title: ICLRMetadataLocator 接口
ms.date: 03/30/2017
api_name:
- ICLRMetadataLocator
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRMetadataLocator
helpviewer_keywords:
- ICLRMetadataLocator interface [.NET Framework debugging]
ms.assetid: 43c944f4-406a-4df6-981e-0eabb33dd5d0
topic_type:
- apiref
ms.openlocfilehash: 6e7fd45197294563e12da020379d1bd54b088698
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772597"
---
# <a name="iclrmetadatalocator-interface"></a><span data-ttu-id="a39f4-103">ICLRMetadataLocator 接口</span><span class="sxs-lookup"><span data-stu-id="a39f4-103">ICLRMetadataLocator Interface</span></span>

<span data-ttu-id="a39f4-104">由数据访问服务层用于在目标进程中查找程序集的元数据。</span><span class="sxs-lookup"><span data-stu-id="a39f4-104">Used by the data access services layer to locate metadata of assemblies in a target process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a39f4-105">方法</span><span class="sxs-lookup"><span data-stu-id="a39f4-105">Methods</span></span>  
  
|<span data-ttu-id="a39f4-106">方法</span><span class="sxs-lookup"><span data-stu-id="a39f4-106">Method</span></span>|<span data-ttu-id="a39f4-107">说明</span><span class="sxs-lookup"><span data-stu-id="a39f4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a39f4-108">GetMetadata 方法</span><span class="sxs-lookup"><span data-stu-id="a39f4-108">GetMetadata Method</span></span>](iclrmetadatalocator-getmetadata-method.md)|<span data-ttu-id="a39f4-109">从目标进程中检索图像的元数据。</span><span class="sxs-lookup"><span data-stu-id="a39f4-109">Retrieves the metadata of an image from the target process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a39f4-110">备注</span><span class="sxs-lookup"><span data-stu-id="a39f4-110">Remarks</span></span>  

 <span data-ttu-id="a39f4-111">API 客户端（即调试器）必须针对特定的目标进程实现此接口。</span><span class="sxs-lookup"><span data-stu-id="a39f4-111">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="a39f4-112">例如，实时过程的实现与内存转储的实现不同。</span><span class="sxs-lookup"><span data-stu-id="a39f4-112">For example, the implementation for a live process would be different from that of a memory dump.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a39f4-113">要求</span><span class="sxs-lookup"><span data-stu-id="a39f4-113">Requirements</span></span>  

 <span data-ttu-id="a39f4-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a39f4-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a39f4-115">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="a39f4-115">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="a39f4-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a39f4-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a39f4-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a39f4-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a39f4-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="a39f4-118">See also</span></span>

- [<span data-ttu-id="a39f4-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="a39f4-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
