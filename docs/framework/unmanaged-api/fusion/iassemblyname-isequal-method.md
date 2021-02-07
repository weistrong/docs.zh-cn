---
description: 了解详细信息： IAssemblyName：： IsEqual 方法
title: IAssemblyName::IsEqual 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.IsEqual
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::IsEqual
helpviewer_keywords:
- IsEqual method [.NET Framework fusion]
- IAssemblyName::IsEqual method [.NET Framework fusion]
ms.assetid: 6dfc220f-d0d4-45b3-bfce-5829f817766f
topic_type:
- apiref
ms.openlocfilehash: f1bb0e26a217354e904ff79b397771d727a7a661
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760677"
---
# <a name="iassemblynameisequal-method"></a><span data-ttu-id="fa37b-103">IAssemblyName::IsEqual 方法</span><span class="sxs-lookup"><span data-stu-id="fa37b-103">IAssemblyName::IsEqual Method</span></span>

<span data-ttu-id="fa37b-104">根据指定的比较标志，确定指定的 [IAssemblyName](iassemblyname-interface.md) 对象是否等于此 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="fa37b-104">Determines whether a specified [IAssemblyName](iassemblyname-interface.md) object is equal to this `IAssemblyName`, based on the specified comparison flags.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa37b-105">语法</span><span class="sxs-lookup"><span data-stu-id="fa37b-105">Syntax</span></span>  
  
```cpp  
HRESULT IsEqual (  
    [in] IAssemblyName  *pName,  
    [in] DWORD          dwCmpFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fa37b-106">参数</span><span class="sxs-lookup"><span data-stu-id="fa37b-106">Parameters</span></span>  

 `pName`  
 <span data-ttu-id="fa37b-107">中要与 `IAssemblyName` 此进行比较的对象 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="fa37b-107">[in] The `IAssemblyName` object to which to compare this `IAssemblyName`.</span></span>  
  
 `dwCmpFlags`  
 <span data-ttu-id="fa37b-108">中影响比较的 [ASM_CMP_FLAGS](asm-cmp-flags-enumeration.md) 值的按位组合。</span><span class="sxs-lookup"><span data-stu-id="fa37b-108">[in] A bitwise combination of [ASM_CMP_FLAGS](asm-cmp-flags-enumeration.md) values that influence the comparison.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fa37b-109">要求</span><span class="sxs-lookup"><span data-stu-id="fa37b-109">Requirements</span></span>  

 <span data-ttu-id="fa37b-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fa37b-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa37b-111">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="fa37b-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="fa37b-112">**NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa37b-112">**NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa37b-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="fa37b-113">See also</span></span>

- [<span data-ttu-id="fa37b-114">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="fa37b-114">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
- [<span data-ttu-id="fa37b-115">合成枚举</span><span class="sxs-lookup"><span data-stu-id="fa37b-115">Fusion Enumerations</span></span>](fusion-enumerations.md)
