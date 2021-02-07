---
description: 了解详细信息： ICLRHostProtectionManager 接口
title: ICLRHostProtectionManager 接口
ms.date: 03/30/2017
api_name:
- ICLRHostProtectionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostProtectionManager
helpviewer_keywords:
- ICLRHostProtectionManager interface [.NET Framework hosting]
ms.assetid: ce2770ae-23d0-45d9-8bcf-46504ac5020e
topic_type:
- apiref
ms.openlocfilehash: 60d27a8c1a24720bbfdcde52a5495425279d5ac4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689223"
---
# <a name="iclrhostprotectionmanager-interface"></a><span data-ttu-id="aee1d-103">ICLRHostProtectionManager 接口</span><span class="sxs-lookup"><span data-stu-id="aee1d-103">ICLRHostProtectionManager Interface</span></span>

<span data-ttu-id="aee1d-104">允许宿主阻止在部分受信任的代码中运行特定的托管类、方法、属性和字段。</span><span class="sxs-lookup"><span data-stu-id="aee1d-104">Enables the host to block specific managed classes, methods, properties, and fields from running in partially trusted code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="aee1d-105">方法</span><span class="sxs-lookup"><span data-stu-id="aee1d-105">Methods</span></span>  
  
|<span data-ttu-id="aee1d-106">方法</span><span class="sxs-lookup"><span data-stu-id="aee1d-106">Method</span></span>|<span data-ttu-id="aee1d-107">说明</span><span class="sxs-lookup"><span data-stu-id="aee1d-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="aee1d-108">SetEagerSerializeGrantSets</span><span class="sxs-lookup"><span data-stu-id="aee1d-108">SetEagerSerializeGrantSets</span></span>](iclrhostprotectionmanager-seteagerserializegrantsets-method.md)|<span data-ttu-id="aee1d-109">确保某些极少数争用条件可能会导致严重的公共语言运行时 (CLR) 错误。</span><span class="sxs-lookup"><span data-stu-id="aee1d-109">Provides a guarantee that certain rare race conditions that can cause fatal common language runtime (CLR) errors will never arise.</span></span>|  
|[<span data-ttu-id="aee1d-110">SetProtectedCategories 方法</span><span class="sxs-lookup"><span data-stu-id="aee1d-110">SetProtectedCategories Method</span></span>](iclrhostprotectionmanager-setprotectedcategories-method.md)|<span data-ttu-id="aee1d-111">指定应阻止在部分受信任代码中运行的托管类型和成员的类别。</span><span class="sxs-lookup"><span data-stu-id="aee1d-111">Specifies the categories of managed types and members that should be blocked from running in partially trusted code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="aee1d-112">要求</span><span class="sxs-lookup"><span data-stu-id="aee1d-112">Requirements</span></span>  

 <span data-ttu-id="aee1d-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="aee1d-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aee1d-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="aee1d-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="aee1d-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="aee1d-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="aee1d-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aee1d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aee1d-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="aee1d-117">See also</span></span>

- [<span data-ttu-id="aee1d-118">EApiCategories 枚举</span><span class="sxs-lookup"><span data-stu-id="aee1d-118">EApiCategories Enumeration</span></span>](eapicategories-enumeration.md)
- [<span data-ttu-id="aee1d-119">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="aee1d-119">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
