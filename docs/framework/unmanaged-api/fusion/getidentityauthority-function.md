---
description: 了解详细信息： GetIdentityAuthority 函数
title: GetIdentityAuthority 函数
ms.date: 03/30/2017
api_name:
- GetIdentityAuthority
api_location:
- fusion.dll
- clr.dll
api_type:
- COM
f1_keywords:
- GetIdentityAuthority
helpviewer_keywords:
- GetIdentityAuthority function [.NET Framework fusion]
ms.assetid: 843cd5ab-d2b7-4ff6-86bd-e68c7a91c098
topic_type:
- apiref
ms.openlocfilehash: 5126aa9b319af41f7ecd30845a9f74ba69016588
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760987"
---
# <a name="getidentityauthority-function"></a><span data-ttu-id="0c365-103">GetIdentityAuthority 函数</span><span class="sxs-lookup"><span data-stu-id="0c365-103">GetIdentityAuthority Function</span></span>

<span data-ttu-id="0c365-104">获取一个指针，该指针指向管理代码对象的键的 [IIdentityAuthority](iidentityauthority-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="0c365-104">Gets a pointer to an [IIdentityAuthority](iidentityauthority-interface.md) instance that manages keys for code objects.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c365-105">语法</span><span class="sxs-lookup"><span data-stu-id="0c365-105">Syntax</span></span>  
  
```cpp  
HRESULT GetIdentityAuthority (  
    [out] IIdentityAuthority   **ppIIdentityAuthority  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="0c365-106">参数</span><span class="sxs-lookup"><span data-stu-id="0c365-106">Parameters</span></span>  

 `ppIIdentityAuthority`  
 <span data-ttu-id="0c365-107">弄返回的 `IIdentityAuthority` 指针。</span><span class="sxs-lookup"><span data-stu-id="0c365-107">[out] The returned `IIdentityAuthority` pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c365-108">要求</span><span class="sxs-lookup"><span data-stu-id="0c365-108">Requirements</span></span>  

 <span data-ttu-id="0c365-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0c365-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c365-110">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="0c365-110">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="0c365-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c365-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c365-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="0c365-112">See also</span></span>

- [<span data-ttu-id="0c365-113">IIdentityAuthority 接口</span><span class="sxs-lookup"><span data-stu-id="0c365-113">IIdentityAuthority Interface</span></span>](iidentityauthority-interface.md)
- [<span data-ttu-id="0c365-114">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="0c365-114">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
