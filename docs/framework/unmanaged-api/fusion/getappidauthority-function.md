---
description: 了解详细信息： GetAppIdAuthority 函数
title: GetAppIdAuthority 函数
ms.date: 03/30/2017
api_name:
- GetAppIdAuthority
api_location:
- fusion.dll
- clr.dll
api_type:
- COM
f1_keywords:
- GetAppIdAuthority
helpviewer_keywords:
- GetAppIdAuthority function [.NET Framework fusion]
ms.assetid: 9f968dad-0d09-47fb-bebc-94c39a0d16ad
topic_type:
- apiref
ms.openlocfilehash: a0c2a7b754c2b014b189f96fd3c27347571cc0d1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761052"
---
# <a name="getappidauthority-function"></a><span data-ttu-id="35900-103">GetAppIdAuthority 函数</span><span class="sxs-lookup"><span data-stu-id="35900-103">GetAppIdAuthority Function</span></span>

<span data-ttu-id="35900-104">获取一个指针，该指针指向管理应用程序标识和引用的密钥的 [IAppIdAuthority](iappidauthority-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="35900-104">Gets a pointer to an [IAppIdAuthority](iappidauthority-interface.md) instance that manages keys for application identities and references.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35900-105">语法</span><span class="sxs-lookup"><span data-stu-id="35900-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAppIdAuthority (  
    [out] IAppIdAuthority **ppIAppIdAuthority  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="35900-106">参数</span><span class="sxs-lookup"><span data-stu-id="35900-106">Parameters</span></span>  

 `ppIAppIdAuthority`  
 <span data-ttu-id="35900-107">弄返回的 `IAppIdAuthority` 指针。</span><span class="sxs-lookup"><span data-stu-id="35900-107">[out] The returned `IAppIdAuthority` pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="35900-108">要求</span><span class="sxs-lookup"><span data-stu-id="35900-108">Requirements</span></span>  

 <span data-ttu-id="35900-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="35900-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="35900-110">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="35900-110">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="35900-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="35900-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="35900-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="35900-112">See also</span></span>

- [<span data-ttu-id="35900-113">IAppIdAuthority 接口</span><span class="sxs-lookup"><span data-stu-id="35900-113">IAppIdAuthority Interface</span></span>](iappidauthority-interface.md)
- [<span data-ttu-id="35900-114">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="35900-114">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
