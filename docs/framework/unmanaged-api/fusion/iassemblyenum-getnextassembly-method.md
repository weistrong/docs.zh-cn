---
description: 了解详细信息： IAssemblyEnum：： GetNextAssembly 方法
title: IAssemblyEnum::GetNextAssembly 方法
ms.date: 03/30/2017
api_name:
- IAssemblyEnum.GetNextAssembly
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyEnum::GetNextAssembly
helpviewer_keywords:
- GetNextAssembly method [.NET Framework fusion]
- IAssemblyEnum::GetNextAssembly method [.NET Framework fusion]
ms.assetid: 5d7a4ca2-5f46-4ef1-a9a2-257884e9dc11
topic_type:
- apiref
ms.openlocfilehash: 52b264b1d8efad54168a6bf69fd0c715cbfa7e2a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760806"
---
# <a name="iassemblyenumgetnextassembly-method"></a><span data-ttu-id="01ffe-103">IAssemblyEnum::GetNextAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="01ffe-103">IAssemblyEnum::GetNextAssembly Method</span></span>

<span data-ttu-id="01ffe-104">获取一个指针，该指针指向此[IAssemblyEnum](iassemblyenum-interface.md)对象中包含的下一个[IAssemblyName](iassemblyname-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="01ffe-104">Gets a pointer to the next [IAssemblyName](iassemblyname-interface.md) contained in this [IAssemblyEnum](iassemblyenum-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="01ffe-105">语法</span><span class="sxs-lookup"><span data-stu-id="01ffe-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNextAssembly (  
    [in]  LPVOID          pvReserved,  
    [out] IAssemblyName   **ppName,  
    [in]  DWORD           dwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="01ffe-106">参数</span><span class="sxs-lookup"><span data-stu-id="01ffe-106">Parameters</span></span>  

 `pvReserved`  
 <span data-ttu-id="01ffe-107">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="01ffe-107">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="01ffe-108">`pvReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="01ffe-108">`pvReserved` must be a null reference.</span></span>  
  
 `ppName`  
 <span data-ttu-id="01ffe-109">弄返回的 `IAssemblyName` 指针。</span><span class="sxs-lookup"><span data-stu-id="01ffe-109">[out] The returned `IAssemblyName` pointer.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="01ffe-110">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="01ffe-110">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="01ffe-111">`dwFlags` 必须为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="01ffe-111">`dwFlags` must be 0 (zero).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="01ffe-112">要求</span><span class="sxs-lookup"><span data-stu-id="01ffe-112">Requirements</span></span>  

 <span data-ttu-id="01ffe-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="01ffe-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="01ffe-114">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="01ffe-114">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="01ffe-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="01ffe-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01ffe-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="01ffe-116">See also</span></span>

- [<span data-ttu-id="01ffe-117">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="01ffe-117">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
- [<span data-ttu-id="01ffe-118">IAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="01ffe-118">IAssemblyEnum Interface</span></span>](iassemblyenum-interface.md)
