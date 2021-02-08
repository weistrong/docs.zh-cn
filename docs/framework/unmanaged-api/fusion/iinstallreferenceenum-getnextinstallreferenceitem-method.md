---
description: 了解详细信息： IInstallReferenceEnum：： GetNextInstallReferenceItem 方法
title: IInstallReferenceEnum::GetNextInstallReferenceItem 方法
ms.date: 03/30/2017
api_name:
- IInstallReferenceEnum.GetNextInstallReferenceItem
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IInstallReferenceEnum::GetNextInstallReferenceItem
helpviewer_keywords:
- IInstallReferenceEnum::GetNextInstallReferenceItem method [.NET Framework fusion]
- GetNextInstallReferenceItem method [.NET Framework fusion]
ms.assetid: ce969c9d-6538-4c34-8784-148ffd99fe7a
topic_type:
- apiref
ms.openlocfilehash: d410407fe16a46b45786ff74f694aaa8931be542
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800106"
---
# <a name="iinstallreferenceenumgetnextinstallreferenceitem-method"></a><span data-ttu-id="77471-103">IInstallReferenceEnum::GetNextInstallReferenceItem 方法</span><span class="sxs-lookup"><span data-stu-id="77471-103">IInstallReferenceEnum::GetNextInstallReferenceItem Method</span></span>

<span data-ttu-id="77471-104">获取一个指针，该指针指向此[IInstallReferenceEnum](iinstallreferenceenum-interface.md)对象中包含的下一个[IInstallReferenceItem](iinstallreferenceitem-interface.md)对象。</span><span class="sxs-lookup"><span data-stu-id="77471-104">Gets a pointer to the next [IInstallReferenceItem](iinstallreferenceitem-interface.md) object contained in this [IInstallReferenceEnum](iinstallreferenceenum-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77471-105">语法</span><span class="sxs-lookup"><span data-stu-id="77471-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNextInstallReferenceItem (  
    [out] IInstallReferenceItem **ppRefItem,  
    [in]  DWORD dwFlags,  
    [in]  LPVOID pvReserved  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="77471-106">参数</span><span class="sxs-lookup"><span data-stu-id="77471-106">Parameters</span></span>  

 `ppRefItem`  
 <span data-ttu-id="77471-107">弄返回的 `IInstallReferenceItem` 指针。</span><span class="sxs-lookup"><span data-stu-id="77471-107">[out] The returned `IInstallReferenceItem` pointer.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="77471-108">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="77471-108">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="77471-109">`dwFlags` 必须为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="77471-109">`dwFlags` must be 0 (zero).</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="77471-110">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="77471-110">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="77471-111">`pvReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="77471-111">`pvReserved` must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="77471-112">要求</span><span class="sxs-lookup"><span data-stu-id="77471-112">Requirements</span></span>  

 <span data-ttu-id="77471-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="77471-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77471-114">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="77471-114">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="77471-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="77471-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77471-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="77471-116">See also</span></span>

- [<span data-ttu-id="77471-117">IInstallReferenceItem 接口</span><span class="sxs-lookup"><span data-stu-id="77471-117">IInstallReferenceItem Interface</span></span>](iinstallreferenceitem-interface.md)
- [<span data-ttu-id="77471-118">IInstallReferenceEnum 接口</span><span class="sxs-lookup"><span data-stu-id="77471-118">IInstallReferenceEnum Interface</span></span>](iinstallreferenceenum-interface.md)
