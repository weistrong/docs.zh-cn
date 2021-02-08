---
description: 了解详细信息： ITypeName：： GetAssemblyName 方法
title: ITypeName::GetAssemblyName 方法
ms.date: 03/30/2017
api_name:
- ITypeName.GetAssemblyName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetAssemblyName
helpviewer_keywords:
- ITypeName::GetAssemblyName method [.NET Framework hosting]
- GetAssemblyName method [.NET Framework hosting]
ms.assetid: 97801d99-f5f1-4a30-882f-959827093fac
topic_type:
- apiref
ms.openlocfilehash: c2e84ec2fc7c6a300611643783d61b46c14997ce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789339"
---
# <a name="itypenamegetassemblyname-method"></a><span data-ttu-id="ed631-103">ITypeName::GetAssemblyName 方法</span><span class="sxs-lookup"><span data-stu-id="ed631-103">ITypeName::GetAssemblyName Method</span></span>

<span data-ttu-id="ed631-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="ed631-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed631-105">语法</span><span class="sxs-lookup"><span data-stu-id="ed631-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAssemblyName (  
    [out, retval] BSTR* rgbszAssemblyNames  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="ed631-106">要求</span><span class="sxs-lookup"><span data-stu-id="ed631-106">Requirements</span></span>  

 <span data-ttu-id="ed631-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ed631-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ed631-108">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ed631-108">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ed631-109">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ed631-109">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ed631-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ed631-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed631-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="ed631-111">See also</span></span>

- [<span data-ttu-id="ed631-112">承载接口</span><span class="sxs-lookup"><span data-stu-id="ed631-112">Hosting Interfaces</span></span>](hosting-interfaces.md)
