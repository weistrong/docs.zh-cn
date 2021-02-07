---
description: 了解详细信息： CreateICeeFileGen 函数
title: CreateICeeFileGen 函数
ms.date: 03/30/2017
api_name:
- CreateICeeFileGen
api_location:
- mscoree.dll
- mscorpehost.dll
- mscorpe.dll
api_type:
- COM
f1_keywords:
- CreateICeeFileGen
helpviewer_keywords:
- CreateICeeFileGen function [.NET Framework hosting]
ms.assetid: e36e1fd8-8456-4359-bdc3-3ec1765f041f
topic_type:
- apiref
ms.openlocfilehash: 10aefaad4dd1173e4ef55f727371bab508e2d40c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716921"
---
# <a name="createiceefilegen-function"></a><span data-ttu-id="76b35-103">CreateICeeFileGen 函数</span><span class="sxs-lookup"><span data-stu-id="76b35-103">CreateICeeFileGen Function</span></span>

<span data-ttu-id="76b35-104">创建 [ICeeFileGen](iceefilegen-class.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="76b35-104">Creates an [ICeeFileGen](iceefilegen-class.md) object.</span></span>  
  
 <span data-ttu-id="76b35-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="76b35-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="76b35-106">语法</span><span class="sxs-lookup"><span data-stu-id="76b35-106">Syntax</span></span>  
  
```cpp  
HRESULT CreateICeeFileGen (  
    [out] ICeeFileGen  **ceeFileGen  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="76b35-107">参数</span><span class="sxs-lookup"><span data-stu-id="76b35-107">Parameters</span></span>  

 `ceeFileGen`  
 <span data-ttu-id="76b35-108">弄指向新对象的地址的指针 `ICeeFileGen` 。</span><span class="sxs-lookup"><span data-stu-id="76b35-108">[out] A pointer to the address of a new `ICeeFileGen` object.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="76b35-109">返回值</span><span class="sxs-lookup"><span data-stu-id="76b35-109">Return Value</span></span>  

 <span data-ttu-id="76b35-110">此方法返回标准 COM 错误代码。</span><span class="sxs-lookup"><span data-stu-id="76b35-110">This method returns standard COM error codes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="76b35-111">备注</span><span class="sxs-lookup"><span data-stu-id="76b35-111">Remarks</span></span>  

 <span data-ttu-id="76b35-112">`ICeeFileGen`对象用于创建公共语言运行时 (CLR) 可移植可执行文件 (PE) 文件。</span><span class="sxs-lookup"><span data-stu-id="76b35-112">The `ICeeFileGen` object is used to create common language runtime (CLR) portable executable (PE) files.</span></span>  
  
 <span data-ttu-id="76b35-113">完成后，调用 [DestroyICeeFileGen](destroyiceefilegen-function.md) 函数以销毁 `ICeeFileGen` 对象。</span><span class="sxs-lookup"><span data-stu-id="76b35-113">Call the [DestroyICeeFileGen](destroyiceefilegen-function.md) function to destroy the `ICeeFileGen` object when finished.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="76b35-114">要求</span><span class="sxs-lookup"><span data-stu-id="76b35-114">Requirements</span></span>  

 <span data-ttu-id="76b35-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="76b35-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="76b35-116">**标头：** ICeeFileGen</span><span class="sxs-lookup"><span data-stu-id="76b35-116">**Header:** ICeeFileGen.h</span></span>  
  
 <span data-ttu-id="76b35-117">**库：** MSCorPE.dll</span><span class="sxs-lookup"><span data-stu-id="76b35-117">**Library:** MSCorPE.dll</span></span>  
  
 <span data-ttu-id="76b35-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="76b35-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76b35-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="76b35-119">See also</span></span>

- [<span data-ttu-id="76b35-120">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="76b35-120">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
