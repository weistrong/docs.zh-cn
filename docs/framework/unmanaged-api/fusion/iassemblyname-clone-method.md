---
description: 了解详细信息： IAssemblyName：： Clone 方法
title: IAssemblyName::Clone 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.Clone
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::Clone
helpviewer_keywords:
- Clone method, IAssemblyName interface [.NET Framework fusion]
- IAssemblyName::Clone method [.NET Framework fusion]
ms.assetid: 7b345e08-5e16-4e3d-a044-4e19d0892943
topic_type:
- apiref
ms.openlocfilehash: b1d8ba2aec73565e9f6acaa44a5ef3731baa3af9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760779"
---
# <a name="iassemblynameclone-method"></a><span data-ttu-id="d3bf4-103">IAssemblyName::Clone 方法</span><span class="sxs-lookup"><span data-stu-id="d3bf4-103">IAssemblyName::Clone Method</span></span>

<span data-ttu-id="d3bf4-104">创建此 [IAssemblyName](iassemblyname-interface.md) 对象的浅表副本。</span><span class="sxs-lookup"><span data-stu-id="d3bf4-104">Creates a shallow copy of this [IAssemblyName](iassemblyname-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3bf4-105">语法</span><span class="sxs-lookup"><span data-stu-id="d3bf4-105">Syntax</span></span>  
  
```cpp  
HRESULT Clone (  
    [out] IAssemblyName **pName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d3bf4-106">参数</span><span class="sxs-lookup"><span data-stu-id="d3bf4-106">Parameters</span></span>  

 `pName`  
 <span data-ttu-id="d3bf4-107">弄此对象的返回副本 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="d3bf4-107">[out] The returned copy of this `IAssemblyName` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d3bf4-108">要求</span><span class="sxs-lookup"><span data-stu-id="d3bf4-108">Requirements</span></span>  

 <span data-ttu-id="d3bf4-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d3bf4-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d3bf4-110">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="d3bf4-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="d3bf4-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d3bf4-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d3bf4-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="d3bf4-112">See also</span></span>

- [<span data-ttu-id="d3bf4-113">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="d3bf4-113">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
