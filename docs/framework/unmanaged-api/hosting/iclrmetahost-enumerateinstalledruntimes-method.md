---
description: 了解详细信息： ICLRMetaHost：： EnumerateInstalledRuntimes 方法
title: ICLRMetaHost::EnumerateInstalledRuntimes 方法
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.EnumerateInstalledRuntimes
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::EnumerateInstalledRuntimes
helpviewer_keywords:
- ICLRMetaHost::EnumerateInstalledRuntimes method [.NET Framework hosting]
- EnumerateInstalledRuntimes method [.NET Framework hosting]
ms.assetid: 9e359384-0d3d-451c-807e-5d7fcebf2be7
topic_type:
- apiref
ms.openlocfilehash: a1c2fe46a64339e013df0f65dc073d183036a0fb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689191"
---
# <a name="iclrmetahostenumerateinstalledruntimes-method"></a><span data-ttu-id="488b6-103">ICLRMetaHost::EnumerateInstalledRuntimes 方法</span><span class="sxs-lookup"><span data-stu-id="488b6-103">ICLRMetaHost::EnumerateInstalledRuntimes Method</span></span>

<span data-ttu-id="488b6-104">返回一个枚举，该枚举包含 (计算机上安装的 CLR) 的每个公共语言运行时版本的有效 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="488b6-104">Returns an enumeration that contains a valid [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface for each version of the common language runtime (CLR) that is installed on a computer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="488b6-105">语法</span><span class="sxs-lookup"><span data-stu-id="488b6-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateInstalledRuntimes (  
    [out, retval] IEnumUnknown **ppEnumerator);  
```  
  
## <a name="parameters"></a><span data-ttu-id="488b6-106">参数</span><span class="sxs-lookup"><span data-stu-id="488b6-106">Parameters</span></span>  

 `ppEnumerator`  
 <span data-ttu-id="488b6-107">弄与计算机上安装的每个 CLR 版本相对应的 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口的枚举。</span><span class="sxs-lookup"><span data-stu-id="488b6-107">[out] An enumeration of [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interfaces corresponding to each version of the CLR that is installed on the computer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="488b6-108">返回值</span><span class="sxs-lookup"><span data-stu-id="488b6-108">Return Value</span></span>  

 <span data-ttu-id="488b6-109">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="488b6-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="488b6-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="488b6-110">HRESULT</span></span>|<span data-ttu-id="488b6-111">说明</span><span class="sxs-lookup"><span data-stu-id="488b6-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="488b6-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="488b6-112">S_OK</span></span>|<span data-ttu-id="488b6-113">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="488b6-113">The method completed successfully.</span></span>|  
|<span data-ttu-id="488b6-114">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="488b6-114">E_POINTER</span></span>|<span data-ttu-id="488b6-115">`ppEnumerator` 为 null。</span><span class="sxs-lookup"><span data-stu-id="488b6-115">`ppEnumerator` is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="488b6-116">要求</span><span class="sxs-lookup"><span data-stu-id="488b6-116">Requirements</span></span>  

 <span data-ttu-id="488b6-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="488b6-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="488b6-118">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="488b6-118">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="488b6-119">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="488b6-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="488b6-120">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="488b6-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="488b6-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="488b6-121">See also</span></span>

- [<span data-ttu-id="488b6-122">ICLRMetaHost 接口</span><span class="sxs-lookup"><span data-stu-id="488b6-122">ICLRMetaHost Interface</span></span>](iclrmetahost-interface.md)
- [<span data-ttu-id="488b6-123">承载</span><span class="sxs-lookup"><span data-stu-id="488b6-123">Hosting</span></span>](index.md)
