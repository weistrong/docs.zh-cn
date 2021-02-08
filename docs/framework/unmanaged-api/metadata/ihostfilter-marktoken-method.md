---
description: 了解详细信息： IHostFilter：： MarkToken 方法
title: IHostFilter::MarkToken 方法
ms.date: 03/30/2017
api_name:
- IHostFilter.MarkToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostFilter::MarkToken
helpviewer_keywords:
- MarkToken method, IHostFilter interface [.NET Framework metadata]
- IHostFilter::MarkToken method [.NET Framework metadata]
ms.assetid: d7061343-d0a3-4fd5-b312-61974f98bd62
topic_type:
- apiref
ms.openlocfilehash: c8f5ecdef56b77e1b0031a93d6d8f7de79de4c3b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784179"
---
# <a name="ihostfiltermarktoken-method"></a><span data-ttu-id="ac6bf-103">IHostFilter::MarkToken 方法</span><span class="sxs-lookup"><span data-stu-id="ac6bf-103">IHostFilter::MarkToken Method</span></span>

<span data-ttu-id="ac6bf-104">指示将处理指定的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="ac6bf-104">Indicates that the specified metadata token will be processed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac6bf-105">语法</span><span class="sxs-lookup"><span data-stu-id="ac6bf-105">Syntax</span></span>  
  
```cpp  
HRESULT MarkToken (  
    [in]  mdToken         tk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ac6bf-106">参数</span><span class="sxs-lookup"><span data-stu-id="ac6bf-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="ac6bf-107">中要处理的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="ac6bf-107">[in] The metadata token to be processed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ac6bf-108">备注</span><span class="sxs-lookup"><span data-stu-id="ac6bf-108">Remarks</span></span>  

 <span data-ttu-id="ac6bf-109">通常，如果令牌在元数据范围内，则需要对其进行处理。</span><span class="sxs-lookup"><span data-stu-id="ac6bf-109">Typically, you want a token to be processed if it is in the metadata scope.</span></span> <span data-ttu-id="ac6bf-110">`MarkToken`方法通过[IMetaDataEmit：： SetHandler](imetadataemit-sethandler-method.md)方法传递给元数据引擎。</span><span class="sxs-lookup"><span data-stu-id="ac6bf-110">The `MarkToken` method is passed to the metadata engine via the [IMetaDataEmit::SetHandler](imetadataemit-sethandler-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ac6bf-111">要求</span><span class="sxs-lookup"><span data-stu-id="ac6bf-111">Requirements</span></span>  

 <span data-ttu-id="ac6bf-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ac6bf-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ac6bf-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="ac6bf-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ac6bf-114">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="ac6bf-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ac6bf-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ac6bf-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac6bf-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="ac6bf-116">See also</span></span>

- [<span data-ttu-id="ac6bf-117">元数据接口</span><span class="sxs-lookup"><span data-stu-id="ac6bf-117">Metadata Interfaces</span></span>](metadata-interfaces.md)
- [<span data-ttu-id="ac6bf-118">IHostFilter 接口</span><span class="sxs-lookup"><span data-stu-id="ac6bf-118">IHostFilter Interface</span></span>](ihostfilter-interface.md)
