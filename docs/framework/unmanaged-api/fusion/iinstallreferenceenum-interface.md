---
description: 了解详细信息： IInstallReferenceEnum 接口
title: IInstallReferenceEnum 接口
ms.date: 03/30/2017
api_name:
- IInstallReferenceEnum
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IInstallReferenceEnum
helpviewer_keywords:
- IInstallReferenceEnum interface [.NET Framework fusion]
ms.assetid: 2863b33b-a541-462c-bbe8-702a2832898e
topic_type:
- apiref
ms.openlocfilehash: 496bd508b95b51cb23949f32f8390c7cb733b37e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800092"
---
# <a name="iinstallreferenceenum-interface"></a><span data-ttu-id="1180a-103">IInstallReferenceEnum 接口</span><span class="sxs-lookup"><span data-stu-id="1180a-103">IInstallReferenceEnum Interface</span></span>

<span data-ttu-id="1180a-104">表示安装在全局程序集缓存中的被引用程序集的枚举器。</span><span class="sxs-lookup"><span data-stu-id="1180a-104">Represents an enumerator for the referenced assemblies installed in the global assembly cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1180a-105">语法</span><span class="sxs-lookup"><span data-stu-id="1180a-105">Syntax</span></span>  
  
```cpp  
interface IInstallReferenceEnum : IUnknown {  
    HRESULT GetNextInstallReferenceItem (  
        [out] IInstallReferenceItem **ppRefItem,  
        [in]  DWORD dwFlags,  
        [in]  LPVOID pvReserved  
    );  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="1180a-106">方法</span><span class="sxs-lookup"><span data-stu-id="1180a-106">Methods</span></span>  
  
|<span data-ttu-id="1180a-107">方法</span><span class="sxs-lookup"><span data-stu-id="1180a-107">Method</span></span>|<span data-ttu-id="1180a-108">说明</span><span class="sxs-lookup"><span data-stu-id="1180a-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1180a-109">GetNextInstallReferenceItem 方法</span><span class="sxs-lookup"><span data-stu-id="1180a-109">GetNextInstallReferenceItem Method</span></span>](iinstallreferenceenum-getnextinstallreferenceitem-method.md)|<span data-ttu-id="1180a-110">获取一个指针，该指针指向 `IInstallReferenceItem` 此中包含的下一个 `IInstallReferenceEnum` 。</span><span class="sxs-lookup"><span data-stu-id="1180a-110">Gets a pointer to the next `IInstallReferenceItem` contained in this `IInstallReferenceEnum`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1180a-111">要求</span><span class="sxs-lookup"><span data-stu-id="1180a-111">Requirements</span></span>  

 <span data-ttu-id="1180a-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1180a-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1180a-113">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="1180a-113">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="1180a-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1180a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1180a-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="1180a-115">See also</span></span>

- [<span data-ttu-id="1180a-116">合成接口</span><span class="sxs-lookup"><span data-stu-id="1180a-116">Fusion Interfaces</span></span>](fusion-interfaces.md)
- [<span data-ttu-id="1180a-117">IInstallReferenceItem 接口</span><span class="sxs-lookup"><span data-stu-id="1180a-117">IInstallReferenceItem Interface</span></span>](iinstallreferenceitem-interface.md)
