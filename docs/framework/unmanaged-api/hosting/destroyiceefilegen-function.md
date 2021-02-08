---
description: 了解详细信息： DestroyICeeFileGen 函数
title: DestroyICeeFileGen 函数
ms.date: 03/30/2017
api_name:
- DestroyICeeFileGen
api_location:
- mscoree.dll
- mscorpehost.dll
- mscorpe.dll
api_type:
- COM
f1_keywords:
- DestroyICeeFileGen
helpviewer_keywords:
- DestroyICeeFileGen function [.NET Framework hosting]
ms.assetid: dc1e2235-e721-4cb2-a0b8-6b0c030d7bab
topic_type:
- apiref
ms.openlocfilehash: 14ae990999247b90f16b10115dea3408b965a04a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785648"
---
# <a name="destroyiceefilegen-function"></a><span data-ttu-id="987f8-103">DestroyICeeFileGen 函数</span><span class="sxs-lookup"><span data-stu-id="987f8-103">DestroyICeeFileGen Function</span></span>

<span data-ttu-id="987f8-104">销毁 [ICeeFileGen](iceefilegen-class.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="987f8-104">Destroys an [ICeeFileGen](iceefilegen-class.md) object.</span></span>  
  
 <span data-ttu-id="987f8-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="987f8-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="987f8-106">语法</span><span class="sxs-lookup"><span data-stu-id="987f8-106">Syntax</span></span>  
  
```cpp  
HRESULT DestroyICeeFileGen (  
    [in] ICeeFileGen  **ceeFileGen  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="987f8-107">参数</span><span class="sxs-lookup"><span data-stu-id="987f8-107">Parameters</span></span>  

 `ceeFileGen`  
 <span data-ttu-id="987f8-108">中 `ICeeFileGen` 要销毁的对象。</span><span class="sxs-lookup"><span data-stu-id="987f8-108">[in] The `ICeeFileGen` object to destroy.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="987f8-109">返回值</span><span class="sxs-lookup"><span data-stu-id="987f8-109">Return Value</span></span>  

 <span data-ttu-id="987f8-110">此方法返回标准 COM 错误代码。</span><span class="sxs-lookup"><span data-stu-id="987f8-110">This method returns standard COM error codes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="987f8-111">备注</span><span class="sxs-lookup"><span data-stu-id="987f8-111">Remarks</span></span>  

 <span data-ttu-id="987f8-112">`DestroyICeeFileGen` 销毁 `ICeeFileGen` [CreateICeeFileGen](createiceefilegen-function.md) 函数创建的对象。</span><span class="sxs-lookup"><span data-stu-id="987f8-112">`DestroyICeeFileGen` destroys the `ICeeFileGen` object created by the [CreateICeeFileGen](createiceefilegen-function.md) function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="987f8-113">要求</span><span class="sxs-lookup"><span data-stu-id="987f8-113">Requirements</span></span>  

 <span data-ttu-id="987f8-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="987f8-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="987f8-115">**标头：** ICeeFileGen</span><span class="sxs-lookup"><span data-stu-id="987f8-115">**Header:** ICeeFileGen.h</span></span>  
  
 <span data-ttu-id="987f8-116">**库：** MSCorPE.dll</span><span class="sxs-lookup"><span data-stu-id="987f8-116">**Library:** MSCorPE.dll</span></span>  
  
 <span data-ttu-id="987f8-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="987f8-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="987f8-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="987f8-118">See also</span></span>

- [<span data-ttu-id="987f8-119">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="987f8-119">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
