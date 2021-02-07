---
description: 了解详细信息： IMetaDataFilter 接口
title: IMetaDataFilter 接口
ms.date: 03/30/2017
api_name:
- IMetaDataFilter
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataFilter
helpviewer_keywords:
- IMetaDataFilter interface [.NET Framework metadata]
ms.assetid: ec0856ef-8c56-40ba-bf60-86e0ce8b337f
topic_type:
- apiref
ms.openlocfilehash: c994574207ccb26a5cb317e1673145a41f0d837d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677920"
---
# <a name="imetadatafilter-interface"></a><span data-ttu-id="a5b46-103">IMetaDataFilter 接口</span><span class="sxs-lookup"><span data-stu-id="a5b46-103">IMetaDataFilter Interface</span></span>

<span data-ttu-id="a5b46-104">提供用于标记和筛选元数据标记以避免重复已进行的操作的方法。</span><span class="sxs-lookup"><span data-stu-id="a5b46-104">Provides methods for marking and filtering metadata tokens to avoid repeating actions that have already been taken.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a5b46-105">方法</span><span class="sxs-lookup"><span data-stu-id="a5b46-105">Methods</span></span>  
  
|<span data-ttu-id="a5b46-106">方法</span><span class="sxs-lookup"><span data-stu-id="a5b46-106">Method</span></span>|<span data-ttu-id="a5b46-107">说明</span><span class="sxs-lookup"><span data-stu-id="a5b46-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a5b46-108">IsTokenMarked 方法</span><span class="sxs-lookup"><span data-stu-id="a5b46-108">IsTokenMarked Method</span></span>](imetadatafilter-istokenmarked-method.md)|<span data-ttu-id="a5b46-109">获取一个值，该值指示是否已处理指定的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="a5b46-109">Gets a value indicating whether the specified metadata token has been processed.</span></span>|  
|[<span data-ttu-id="a5b46-110">MarkToken 方法</span><span class="sxs-lookup"><span data-stu-id="a5b46-110">MarkToken Method</span></span>](imetadatafilter-marktoken-method.md)|<span data-ttu-id="a5b46-111">设置一个值，该值指示已处理指定的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="a5b46-111">Sets a value indicating that the specified metadata token has been processed.</span></span>|  
|[<span data-ttu-id="a5b46-112">UnmarkAll 方法</span><span class="sxs-lookup"><span data-stu-id="a5b46-112">UnmarkAll Method</span></span>](imetadatafilter-unmarkall-method.md)|<span data-ttu-id="a5b46-113">从当前元数据范围内的所有标记中删除处理标记。</span><span class="sxs-lookup"><span data-stu-id="a5b46-113">Removes the processing marks from all the tokens in the current metadata scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a5b46-114">要求</span><span class="sxs-lookup"><span data-stu-id="a5b46-114">Requirements</span></span>  

 <span data-ttu-id="a5b46-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a5b46-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a5b46-116">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="a5b46-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a5b46-117">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="a5b46-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a5b46-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a5b46-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a5b46-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="a5b46-119">See also</span></span>

- [<span data-ttu-id="a5b46-120">元数据接口</span><span class="sxs-lookup"><span data-stu-id="a5b46-120">Metadata Interfaces</span></span>](metadata-interfaces.md)
