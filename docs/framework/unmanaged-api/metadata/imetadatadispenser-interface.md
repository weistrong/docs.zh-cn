---
description: 了解详细信息： IMetaDataDispenser 接口
title: IMetaDataDispenser 接口
ms.date: 03/30/2017
api_name:
- IMetaDataDispenser
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenser
helpviewer_keywords:
- IMetaDataDispenser interface [.NET Framework metadata]
ms.assetid: 989840b3-9822-4ce5-a6c5-b375d3340a7a
topic_type:
- apiref
ms.openlocfilehash: 5ba37fc05a4e1897b100967d32b268f91a0e4402
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721003"
---
# <a name="imetadatadispenser-interface"></a><span data-ttu-id="a1384-103">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="a1384-103">IMetaDataDispenser Interface</span></span>

<span data-ttu-id="a1384-104">提供创建新的元数据范围或打开现有元数据范围的方法。</span><span class="sxs-lookup"><span data-stu-id="a1384-104">Provides methods to create a new metadata scope, or open an existing one.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a1384-105">方法</span><span class="sxs-lookup"><span data-stu-id="a1384-105">Methods</span></span>  
  
|<span data-ttu-id="a1384-106">方法</span><span class="sxs-lookup"><span data-stu-id="a1384-106">Method</span></span>|<span data-ttu-id="a1384-107">说明</span><span class="sxs-lookup"><span data-stu-id="a1384-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a1384-108">DefineScope 方法</span><span class="sxs-lookup"><span data-stu-id="a1384-108">DefineScope Method</span></span>](imetadatadispenser-definescope-method.md)|<span data-ttu-id="a1384-109">在内存中创建新的区域，您可以在其中创建新的元数据。</span><span class="sxs-lookup"><span data-stu-id="a1384-109">Creates a new area in memory where you can create new metadata.</span></span>|  
|[<span data-ttu-id="a1384-110">OpenScope 方法</span><span class="sxs-lookup"><span data-stu-id="a1384-110">OpenScope Method</span></span>](imetadatadispenser-openscope-method.md)|<span data-ttu-id="a1384-111">打开现有的磁盘上的文件，并将其元数据映射到内存。</span><span class="sxs-lookup"><span data-stu-id="a1384-111">Opens an existing, on-disk file and maps its metadata into memory.</span></span>|  
|[<span data-ttu-id="a1384-112">OpenScopeOnMemory 方法</span><span class="sxs-lookup"><span data-stu-id="a1384-112">OpenScopeOnMemory Method</span></span>](imetadatadispenser-openscopeonmemory-method.md)|<span data-ttu-id="a1384-113">打开包含现有元数据的内存区域。</span><span class="sxs-lookup"><span data-stu-id="a1384-113">Opens an area of memory that contains existing metadata.</span></span> <span data-ttu-id="a1384-114">也就是说，此方法将打开一个指定的内存区域，其中的现有数据将被视为元数据。</span><span class="sxs-lookup"><span data-stu-id="a1384-114">That is, this method opens a specified area of memory in which the existing data is treated as metadata.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a1384-115">要求</span><span class="sxs-lookup"><span data-stu-id="a1384-115">Requirements</span></span>  

 <span data-ttu-id="a1384-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a1384-116">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1384-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="a1384-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a1384-118">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="a1384-118">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a1384-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1384-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1384-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="a1384-120">See also</span></span>

- [<span data-ttu-id="a1384-121">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="a1384-121">IMetaDataDispenserEx Interface</span></span>](imetadatadispenserex-interface.md)
- [<span data-ttu-id="a1384-122">元数据接口</span><span class="sxs-lookup"><span data-stu-id="a1384-122">Metadata Interfaces</span></span>](metadata-interfaces.md)
