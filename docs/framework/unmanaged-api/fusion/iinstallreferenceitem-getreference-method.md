---
description: 了解详细信息： IInstallReferenceItem：： GetReference 方法
title: IInstallReferenceItem::GetReference 方法
ms.date: 03/30/2017
api_name:
- IInstallReferenceItem.GetReference
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IInstallReferenceItem::GetReference
helpviewer_keywords:
- IInstallReferenceItem::GetReference method [.NET Framework fusion]
- GetReference method [.NET Framework fusion]
ms.assetid: 8960332f-c98a-405a-ba92-7003de0c1187
topic_type:
- apiref
ms.openlocfilehash: 88f5ca21b6f3494031e1cd232f71253e39d9e648
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800098"
---
# <a name="iinstallreferenceitemgetreference-method"></a><span data-ttu-id="54fbf-103">IInstallReferenceItem::GetReference 方法</span><span class="sxs-lookup"><span data-stu-id="54fbf-103">IInstallReferenceItem::GetReference Method</span></span>

<span data-ttu-id="54fbf-104">获取一个指针，该指针指向此[IInstallReferenceItem](iinstallreferenceitem-interface.md)对象表示的[FUSION_INSTALL_REFERENCE](fusion-install-reference-structure.md)结构。</span><span class="sxs-lookup"><span data-stu-id="54fbf-104">Gets a pointer to the [FUSION_INSTALL_REFERENCE](fusion-install-reference-structure.md) structure represented by this [IInstallReferenceItem](iinstallreferenceitem-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="54fbf-105">语法</span><span class="sxs-lookup"><span data-stu-id="54fbf-105">Syntax</span></span>  
  
```cpp  
HRESULT GetReference (  
    [out] LPFUSION_INSTALL_REFERENCE *ppRefData,  
    [in]  DWORD dwFlags,  
    [in]  LPVOID pvReserved  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="54fbf-106">参数</span><span class="sxs-lookup"><span data-stu-id="54fbf-106">Parameters</span></span>  

 `ppRefData`  
 <span data-ttu-id="54fbf-107">弄返回的 `FUSION_INSTALL_REFERENCE` 指针。</span><span class="sxs-lookup"><span data-stu-id="54fbf-107">[out] The returned `FUSION_INSTALL_REFERENCE` pointer.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="54fbf-108">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="54fbf-108">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="54fbf-109">`dwFlags` 必须为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="54fbf-109">`dwFlags` must be 0 (zero).</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="54fbf-110">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="54fbf-110">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="54fbf-111">`pvReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="54fbf-111">`pvReserved` must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="54fbf-112">要求</span><span class="sxs-lookup"><span data-stu-id="54fbf-112">Requirements</span></span>  

 <span data-ttu-id="54fbf-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="54fbf-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="54fbf-114">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="54fbf-114">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="54fbf-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="54fbf-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="54fbf-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="54fbf-116">See also</span></span>

- [<span data-ttu-id="54fbf-117">IInstallReferenceItem 接口</span><span class="sxs-lookup"><span data-stu-id="54fbf-117">IInstallReferenceItem Interface</span></span>](iinstallreferenceitem-interface.md)
- [<span data-ttu-id="54fbf-118">FUSION_INSTALL_REFERENCE 结构</span><span class="sxs-lookup"><span data-stu-id="54fbf-118">FUSION_INSTALL_REFERENCE Structure</span></span>](fusion-install-reference-structure.md)
