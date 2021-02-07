---
description: 了解详细信息： ITypeName：： GetTypeArgumentCount 方法
title: ITypeName::GetTypeArgumentCount 方法
ms.date: 03/30/2017
api_name:
- ITypeName.GetTypeArgumentCount
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetTypeArgumentCount
helpviewer_keywords:
- GetTypeArgumentCount method [.NET Framework hosting]
- ITypeName::GetTypeArgumentCount method [.NET Framework hosting]
ms.assetid: ecb5480c-761a-4b02-83e0-b79abc67fd08
topic_type:
- apiref
ms.openlocfilehash: dc628194a949c46711193df78f1a384a9a1098bb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753674"
---
# <a name="itypenamegettypeargumentcount-method"></a><span data-ttu-id="ead8d-103">ITypeName::GetTypeArgumentCount 方法</span><span class="sxs-lookup"><span data-stu-id="ead8d-103">ITypeName::GetTypeArgumentCount Method</span></span>

<span data-ttu-id="ead8d-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="ead8d-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ead8d-105">语法</span><span class="sxs-lookup"><span data-stu-id="ead8d-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTypeArgumentCount (  
    [out, retval] DWORD* pCount  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="ead8d-106">要求</span><span class="sxs-lookup"><span data-stu-id="ead8d-106">Requirements</span></span>  

 <span data-ttu-id="ead8d-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ead8d-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ead8d-108">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ead8d-108">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ead8d-109">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ead8d-109">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ead8d-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ead8d-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ead8d-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="ead8d-111">See also</span></span>

- [<span data-ttu-id="ead8d-112">承载接口</span><span class="sxs-lookup"><span data-stu-id="ead8d-112">Hosting Interfaces</span></span>](hosting-interfaces.md)
