---
description: 了解详细信息： IMetaDataError：： OnError 方法
title: IMetaDataError::OnError 方法
ms.date: 03/30/2017
api_name:
- IMetaDataError.OnError
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataError::OnError
helpviewer_keywords:
- IMetaDataError::OnError method [.NET Framework metadata]
- OnError method, IMetaDataError interface [.NET Framework metadata]
ms.assetid: c1e744b8-a6fb-4d9c-a971-8babc875d8f0
topic_type:
- apiref
ms.openlocfilehash: 9556f1bd7758755d9160e3a2e91a1fe5786aa562
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99670965"
---
# <a name="imetadataerroronerror-method"></a><span data-ttu-id="e281c-103">IMetaDataError::OnError 方法</span><span class="sxs-lookup"><span data-stu-id="e281c-103">IMetaDataError::OnError Method</span></span>

<span data-ttu-id="e281c-104">提供在元数据合并期间发生的错误的通知。</span><span class="sxs-lookup"><span data-stu-id="e281c-104">Provides notification of errors that occur during the metadata merge.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e281c-105">语法</span><span class="sxs-lookup"><span data-stu-id="e281c-105">Syntax</span></span>  
  
```cpp  
HRESULT OnError (  
    [in] HRESULT   hrError,
    [in] mdToken   token  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e281c-106">参数</span><span class="sxs-lookup"><span data-stu-id="e281c-106">Parameters</span></span>  

 `hrError`  
 <span data-ttu-id="e281c-107">中返回到调用方法的 HRESULT 错误值。</span><span class="sxs-lookup"><span data-stu-id="e281c-107">[in] The HRESULT error value returned to the calling method.</span></span>  
  
 `token`  
 <span data-ttu-id="e281c-108">中发生错误时正在合并的代码对象的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e281c-108">[in] The metadata token of the code object that was being merged when the error occurred.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e281c-109">要求</span><span class="sxs-lookup"><span data-stu-id="e281c-109">Requirements</span></span>  

 <span data-ttu-id="e281c-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e281c-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e281c-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="e281c-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e281c-112">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="e281c-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e281c-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e281c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e281c-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="e281c-114">See also</span></span>

- [<span data-ttu-id="e281c-115">IMetaDataError 接口</span><span class="sxs-lookup"><span data-stu-id="e281c-115">IMetaDataError Interface</span></span>](imetadataerror-interface.md)
