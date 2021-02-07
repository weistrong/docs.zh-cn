---
description: 了解详细信息： IAssemblyName：： SetProperty 方法
title: IAssemblyName::SetProperty 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.SetProperty
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::SetProperty
helpviewer_keywords:
- IAssemblyName::SetProperty method [.NET Framework fusion]
- SetProperty method [.NET Framework fusion]
ms.assetid: 496c3add-f60b-4073-943f-d1bcf33330cb
topic_type:
- apiref
ms.openlocfilehash: cab132c2cd8a0744a2a946a1d8b21f49012c6eac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760676"
---
# <a name="iassemblynamesetproperty-method"></a><span data-ttu-id="e5ee7-103">IAssemblyName::SetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="e5ee7-103">IAssemblyName::SetProperty Method</span></span>

<span data-ttu-id="e5ee7-104">设置由指定的属性标识符引用的属性的值。</span><span class="sxs-lookup"><span data-stu-id="e5ee7-104">Sets the value of the property referenced by the specified property identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5ee7-105">语法</span><span class="sxs-lookup"><span data-stu-id="e5ee7-105">Syntax</span></span>  
  
```cpp  
HRESULT SetProperty (  
    [in] DWORD  PropertyId,  
    [in] LPVOID pvProperty,  
    [in] DWORD  cbProperty  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e5ee7-106">参数</span><span class="sxs-lookup"><span data-stu-id="e5ee7-106">Parameters</span></span>  

 `PropertyId`  
 <span data-ttu-id="e5ee7-107">中将设置其值的属性的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="e5ee7-107">[in] The unique identifier of the property whose value will be set.</span></span>  
  
 `pvProperty`  
 <span data-ttu-id="e5ee7-108">中要将引用的属性设置为的值 `PropertyId` 。</span><span class="sxs-lookup"><span data-stu-id="e5ee7-108">[in] The value to which to set the property referenced by `PropertyId`.</span></span>  
  
 `cbProperty`  
 <span data-ttu-id="e5ee7-109">中的大小（以字节为单位） `pvProperty` 。</span><span class="sxs-lookup"><span data-stu-id="e5ee7-109">[in] The size, in bytes, of `pvProperty`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5ee7-110">要求</span><span class="sxs-lookup"><span data-stu-id="e5ee7-110">Requirements</span></span>  

 <span data-ttu-id="e5ee7-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e5ee7-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5ee7-112">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="e5ee7-112">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="e5ee7-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5ee7-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5ee7-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="e5ee7-114">See also</span></span>

- [<span data-ttu-id="e5ee7-115">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="e5ee7-115">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
