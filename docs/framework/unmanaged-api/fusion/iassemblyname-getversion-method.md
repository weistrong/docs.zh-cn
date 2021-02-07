---
description: 了解详细信息： IAssemblyName：： GetVersion 方法
title: IAssemblyName::GetVersion 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetVersion
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetVersion
helpviewer_keywords:
- IAssemblyName::GetVersion method [.NET Framework fusion]
- GetVersion method, IAssemblyName interface [.NET Framework fusion]
ms.assetid: 42230928-2c33-41fd-9519-d96efef6c7af
topic_type:
- apiref
ms.openlocfilehash: 3339dda6a0b4f083655ece7bef86b080a8fcf5c8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760714"
---
# <a name="iassemblynamegetversion-method"></a><span data-ttu-id="f04e8-103">IAssemblyName::GetVersion 方法</span><span class="sxs-lookup"><span data-stu-id="f04e8-103">IAssemblyName::GetVersion Method</span></span>

<span data-ttu-id="f04e8-104">获取此 [IAssemblyName](iassemblyname-interface.md) 对象所引用的程序集的版本信息。</span><span class="sxs-lookup"><span data-stu-id="f04e8-104">Gets the version information for the assembly referenced by this [IAssemblyName](iassemblyname-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f04e8-105">语法</span><span class="sxs-lookup"><span data-stu-id="f04e8-105">Syntax</span></span>  
  
```cpp  
HRESULT GetVersion (  
    [out] LPDWORD pdwVersionHi,  
    [out] LPDWORD pdwVersionLow  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f04e8-106">参数</span><span class="sxs-lookup"><span data-stu-id="f04e8-106">Parameters</span></span>  

 `pdwVersionHi`  
 <span data-ttu-id="f04e8-107">弄版本的高32位。</span><span class="sxs-lookup"><span data-stu-id="f04e8-107">[out] The high 32 bits of the version.</span></span>  
  
 `pdwVersionLow`  
 <span data-ttu-id="f04e8-108">弄版本的低32位。</span><span class="sxs-lookup"><span data-stu-id="f04e8-108">[out] The low 32 bits of the version.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f04e8-109">要求</span><span class="sxs-lookup"><span data-stu-id="f04e8-109">Requirements</span></span>  

 <span data-ttu-id="f04e8-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f04e8-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f04e8-111">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="f04e8-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="f04e8-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f04e8-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f04e8-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="f04e8-113">See also</span></span>

- [<span data-ttu-id="f04e8-114">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="f04e8-114">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
