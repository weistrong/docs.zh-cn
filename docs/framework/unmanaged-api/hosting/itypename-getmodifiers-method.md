---
description: 了解详细信息： ITypeName：： GetModifiers 方法
title: ITypeName::GetModifiers 方法
ms.date: 03/30/2017
api_name:
- ITypeName.GetModifiers
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetModifiers
helpviewer_keywords:
- ITypeName::GetModifiers method [.NET Framework hosting]
- GetModifiers method [.NET Framework hosting]
ms.assetid: 75508c55-3e09-4135-80da-cc811003fa82
topic_type:
- apiref
ms.openlocfilehash: 3c44d569255656f95ccceec0462d09044b46679b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753713"
---
# <a name="itypenamegetmodifiers-method"></a><span data-ttu-id="5279a-103">ITypeName::GetModifiers 方法</span><span class="sxs-lookup"><span data-stu-id="5279a-103">ITypeName::GetModifiers Method</span></span>

<span data-ttu-id="5279a-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="5279a-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5279a-105">语法</span><span class="sxs-lookup"><span data-stu-id="5279a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetModifiers (  
    [in] DWORD           count,  
    [out] DWORD*         rgModifiers,  
    [out, retval] DWORD* pCount  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="5279a-106">要求</span><span class="sxs-lookup"><span data-stu-id="5279a-106">Requirements</span></span>  

 <span data-ttu-id="5279a-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5279a-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5279a-108">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5279a-108">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5279a-109">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5279a-109">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5279a-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5279a-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5279a-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="5279a-111">See also</span></span>

- [<span data-ttu-id="5279a-112">承载接口</span><span class="sxs-lookup"><span data-stu-id="5279a-112">Hosting Interfaces</span></span>](hosting-interfaces.md)
