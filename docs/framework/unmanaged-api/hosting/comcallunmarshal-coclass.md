---
description: 了解详细信息： ComCallUnmarshal 组件类
title: ComCallUnmarshal Coclass
ms.date: 03/30/2017
api_name:
- ComCallUnmarshal Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ComCallUnmarshal
helpviewer_keywords:
- ComCallUnmarshal coclass [.NET Framework hosting]
ms.assetid: 2adb5827-2268-4914-a1c6-f62b61880a45
topic_type:
- apiref
ms.openlocfilehash: 508c1183e2862a286e9db0390bc0348629a9db8e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799832"
---
# <a name="comcallunmarshal-coclass"></a><span data-ttu-id="03882-103">ComCallUnmarshal Coclass</span><span class="sxs-lookup"><span data-stu-id="03882-103">ComCallUnmarshal Coclass</span></span>

<span data-ttu-id="03882-104">提供用于管理接口指针的封送处理的接口。</span><span class="sxs-lookup"><span data-stu-id="03882-104">Provides interfaces for managing the marshaling of interface pointers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="03882-105">语法</span><span class="sxs-lookup"><span data-stu-id="03882-105">Syntax</span></span>  
  
```cpp  
coclass ComCallUnmarshal {  
    [default] interface IMarshal;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="03882-106">界面</span><span class="sxs-lookup"><span data-stu-id="03882-106">Interfaces</span></span>  
  
|<span data-ttu-id="03882-107">接口</span><span class="sxs-lookup"><span data-stu-id="03882-107">Interface</span></span>|<span data-ttu-id="03882-108">说明</span><span class="sxs-lookup"><span data-stu-id="03882-108">Description</span></span>|  
|---------------|-----------------|  
|`IMarshal`|<span data-ttu-id="03882-109">提供用于在客户端进程中创建、初始化和管理代理的方法。</span><span class="sxs-lookup"><span data-stu-id="03882-109">Provides methods for creating, initializing, and managing a proxy in a client process.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="03882-110">要求</span><span class="sxs-lookup"><span data-stu-id="03882-110">Requirements</span></span>  

 <span data-ttu-id="03882-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="03882-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="03882-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="03882-112">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="03882-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="03882-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="03882-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="03882-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03882-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="03882-115">See also</span></span>

- [<span data-ttu-id="03882-116">承载组件类</span><span class="sxs-lookup"><span data-stu-id="03882-116">Hosting Coclasses</span></span>](hosting-coclasses.md)
