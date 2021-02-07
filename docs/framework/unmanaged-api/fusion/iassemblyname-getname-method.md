---
description: 了解详细信息： IAssemblyName：： GetName 方法
title: IAssemblyName::GetName 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetName
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetName
helpviewer_keywords:
- GetName method, IAssemblyName interface [.NET Framework debugging]
- IAssemblyName::GetName method [.NET Framework fusion]
ms.assetid: 1dee9781-1cf3-48a9-a376-d18ea1f73280
topic_type:
- apiref
ms.openlocfilehash: 04cd6258c2fc60c9fc40e1e4b731e5c04a8d3112
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760740"
---
# <a name="iassemblynamegetname-method"></a><span data-ttu-id="be03c-103">IAssemblyName::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="be03c-103">IAssemblyName::GetName Method</span></span>

<span data-ttu-id="be03c-104">获取此 [IAssemblyName](iassemblyname-interface.md) 对象所引用的程序集的简单、未加密名称。</span><span class="sxs-lookup"><span data-stu-id="be03c-104">Gets the simple, unencrypted name of the assembly referenced by this [IAssemblyName](iassemblyname-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be03c-105">语法</span><span class="sxs-lookup"><span data-stu-id="be03c-105">Syntax</span></span>  
  
```cpp  
HRESULT GetName (  
    [in, out] LPDWORD lpcwBuffer,  
    [out]     WCHAR *pwzName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="be03c-106">参数</span><span class="sxs-lookup"><span data-stu-id="be03c-106">Parameters</span></span>  

 `lpcwBuffer`  
 <span data-ttu-id="be03c-107">[in，out] `pwzName` 宽字符的大小，包括 null 终止符。</span><span class="sxs-lookup"><span data-stu-id="be03c-107">[in, out] The size of `pwzName` in wide characters, including the null terminator character.</span></span>  
  
 `pwzName`  
 <span data-ttu-id="be03c-108">弄用于保存所引用程序集的名称的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="be03c-108">[out] A buffer to hold the name of the referenced assembly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="be03c-109">要求</span><span class="sxs-lookup"><span data-stu-id="be03c-109">Requirements</span></span>  

 <span data-ttu-id="be03c-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="be03c-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="be03c-111">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="be03c-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="be03c-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="be03c-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be03c-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="be03c-113">See also</span></span>

- [<span data-ttu-id="be03c-114">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="be03c-114">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
