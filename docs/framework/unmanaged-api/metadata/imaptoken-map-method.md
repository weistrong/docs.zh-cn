---
description: 了解详细信息： IMapToken：： Map 方法
title: IMapToken::Map 方法
ms.date: 03/30/2017
api_name:
- IMapToken.Map
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMapToken::Map
helpviewer_keywords:
- IMapToken::Map method [.NET Framework metadata]
- Map method [.NET Framework metadata]
ms.assetid: b9b4bf2f-1098-43d6-9619-a99b4bda1940
topic_type:
- apiref
ms.openlocfilehash: da78f22e944a0e4ec25adcd7cdf97b69131a6612
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706729"
---
# <a name="imaptokenmap-method"></a><span data-ttu-id="e50b6-103">IMapToken::Map 方法</span><span class="sxs-lookup"><span data-stu-id="e50b6-103">IMapToken::Map Method</span></span>

<span data-ttu-id="e50b6-104">使用元数据签名映射程序集之间的关系。</span><span class="sxs-lookup"><span data-stu-id="e50b6-104">Maps a relationship between the assemblies using metadata signatures.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e50b6-105">语法</span><span class="sxs-lookup"><span data-stu-id="e50b6-105">Syntax</span></span>  
  
```cpp  
HRESULT Map (  
    [in]  mdToken tkImp,
    [in]  mdToken tkEmit  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e50b6-106">参数</span><span class="sxs-lookup"><span data-stu-id="e50b6-106">Parameters</span></span>  

 `tkImp`  
 <span data-ttu-id="e50b6-107">中表示导入的代码对象的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e50b6-107">[in] The metadata token that represents the imported code object.</span></span>  
  
 `tkEmit`  
 <span data-ttu-id="e50b6-108">中表示发出的代码对象的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e50b6-108">[in] The metadata token that represents the emitted code object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e50b6-109">备注</span><span class="sxs-lookup"><span data-stu-id="e50b6-109">Remarks</span></span>  

 <span data-ttu-id="e50b6-110">如果在合并过程中发生令牌重新映射，则原始令牌的范围将在导入的 (源) 元数据范围内，并且新令牌的范围限定为发出的 (目标) 元数据范围。</span><span class="sxs-lookup"><span data-stu-id="e50b6-110">When the token re-map occurs during a merge, the original token is scoped in the imported (source) metadata scope and the new token is scoped in the emitted (target) metadata scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e50b6-111">要求</span><span class="sxs-lookup"><span data-stu-id="e50b6-111">Requirements</span></span>  

 <span data-ttu-id="e50b6-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e50b6-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e50b6-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="e50b6-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e50b6-114">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="e50b6-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e50b6-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e50b6-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e50b6-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="e50b6-116">See also</span></span>

- [<span data-ttu-id="e50b6-117">IMapToken 接口</span><span class="sxs-lookup"><span data-stu-id="e50b6-117">IMapToken Interface</span></span>](imaptoken-interface.md)
