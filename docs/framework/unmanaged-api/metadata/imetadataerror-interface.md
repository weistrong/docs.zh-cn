---
description: 了解详细信息： IMetaDataError 接口
title: IMetaDataError 接口
ms.date: 03/30/2017
api_name:
- IMetaDataError
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataError
helpviewer_keywords:
- IMetaDataError interface [.NET Framework metadata]
ms.assetid: 0020b62c-ea88-40c7-a9ee-16b064f81624
topic_type:
- apiref
ms.openlocfilehash: f32c8abc3cccce770b86ce47016d9b7e18acad23
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771686"
---
# <a name="imetadataerror-interface"></a><span data-ttu-id="ae966-103">IMetaDataError 接口</span><span class="sxs-lookup"><span data-stu-id="ae966-103">IMetaDataError Interface</span></span>

<span data-ttu-id="ae966-104">提供用于在元数据合并期间报告错误的回调机制。</span><span class="sxs-lookup"><span data-stu-id="ae966-104">Provides a callback mechanism for reporting errors during the metadata merge.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ae966-105">`IMetaDataError`接口必须由客户端实现。</span><span class="sxs-lookup"><span data-stu-id="ae966-105">The `IMetaDataError` interface must be implemented by the client.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ae966-106">方法</span><span class="sxs-lookup"><span data-stu-id="ae966-106">Methods</span></span>  
  
|<span data-ttu-id="ae966-107">方法</span><span class="sxs-lookup"><span data-stu-id="ae966-107">Method</span></span>|<span data-ttu-id="ae966-108">说明</span><span class="sxs-lookup"><span data-stu-id="ae966-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ae966-109">OnError 方法</span><span class="sxs-lookup"><span data-stu-id="ae966-109">OnError Method</span></span>](imetadataerror-onerror-method.md)|<span data-ttu-id="ae966-110">提供在元数据合并期间发生的错误的通知。</span><span class="sxs-lookup"><span data-stu-id="ae966-110">Provides notification of errors that occur during the metadata merge.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ae966-111">要求</span><span class="sxs-lookup"><span data-stu-id="ae966-111">Requirements</span></span>  

 <span data-ttu-id="ae966-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ae966-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae966-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="ae966-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ae966-114">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="ae966-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ae966-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae966-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae966-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="ae966-116">See also</span></span>

- [<span data-ttu-id="ae966-117">元数据接口</span><span class="sxs-lookup"><span data-stu-id="ae966-117">Metadata Interfaces</span></span>](metadata-interfaces.md)
