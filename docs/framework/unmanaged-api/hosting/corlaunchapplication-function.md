---
description: 了解详细信息： CorLaunchApplication 函数
title: CorLaunchApplication 函数
ms.date: 03/30/2017
api_name:
- CorLaunchApplication
api_location:
- mscoree.dll
- clr.dll
api_type:
- COM
f1_keywords:
- CorLaunchApplication
helpviewer_keywords:
- CorLaunchApplication function [.NET Framework hosting]
ms.assetid: 71f362a9-8fe2-47ce-9302-05a645cf3d7d
topic_type:
- apiref
ms.openlocfilehash: 89f1f37ddde69fb5ecc24fd9dfd0d0c27d5fac40
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716947"
---
# <a name="corlaunchapplication-function"></a><span data-ttu-id="5c695-103">CorLaunchApplication 函数</span><span class="sxs-lookup"><span data-stu-id="5c695-103">CorLaunchApplication Function</span></span>

<span data-ttu-id="5c695-104">使用指定的清单和其他应用程序数据，在指定的网络路径下启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="5c695-104">Starts the application at the specified network path, using the specified manifests and other application data.</span></span>  
  
 <span data-ttu-id="5c695-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="5c695-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5c695-106">语法</span><span class="sxs-lookup"><span data-stu-id="5c695-106">Syntax</span></span>  
  
```cpp  
HRESULT CorLaunchApplication (  
    [in]  HOST_TYPE                dwClickOnceHost,  
    [in]  LPCWSTR                  pwzAppFullName,  
    [in]  DWORD                    dwManifestPaths,  
    [in]  LPCWSTR                 *ppwzManifestPaths,  
    [in]  DWORD                    dwActivationData,  
    [in]  LPCWSTR                 *ppwzActivationData,  
    [out] LPPROCESS_INFORMATION    lpProcessInformation  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5c695-107">参数</span><span class="sxs-lookup"><span data-stu-id="5c695-107">Parameters</span></span>  

 `dwClickOnceHost`  
 <span data-ttu-id="5c695-108">中一个 [HOST_TYPE](host-type-enumeration.md) 枚举的值，该值指定启动应用程序的主机的类型。</span><span class="sxs-lookup"><span data-stu-id="5c695-108">[in] A value of the [HOST_TYPE](host-type-enumeration.md) enumeration that specifies the type of host that is launching the application.</span></span>  
  
 `pwzAppFullName`  
 <span data-ttu-id="5c695-109">中正在启动的应用程序的完整名称。</span><span class="sxs-lookup"><span data-stu-id="5c695-109">[in] The full name of the application that is being launched.</span></span>  
  
 `dwManifestPaths`  
 <span data-ttu-id="5c695-110">中应用程序的清单路径数。</span><span class="sxs-lookup"><span data-stu-id="5c695-110">[in] The number of manifest paths for the application.</span></span>  
  
 `ppwzManifestPaths`  
 <span data-ttu-id="5c695-111">中一个字符串数组，其中每个字符串指定要启动的应用程序的清单的路径。</span><span class="sxs-lookup"><span data-stu-id="5c695-111">[in] An array of strings, each of which specifies a path to a manifest for the application that is being launched.</span></span>  
  
 `dwActivationData`  
 <span data-ttu-id="5c695-112">中正在启动的应用程序的激活数据项的数目。</span><span class="sxs-lookup"><span data-stu-id="5c695-112">[in] The number of activation data items for the application that is being launched.</span></span>  
  
 `ppwzActivationData`  
 <span data-ttu-id="5c695-113">中一个字符串数组，其中每个字符串都是要启动的应用程序的激活数据项。</span><span class="sxs-lookup"><span data-stu-id="5c695-113">[in] An array of strings, each of which is an activation data item for the application that is being launched.</span></span>  
  
 `lpProcessInformation`  
 <span data-ttu-id="5c695-114">弄一个指针，指向有关已加载应用程序的进程的信息。</span><span class="sxs-lookup"><span data-stu-id="5c695-114">[out] A pointer to information about the process in which the application has been loaded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5c695-115">要求</span><span class="sxs-lookup"><span data-stu-id="5c695-115">Requirements</span></span>  

 <span data-ttu-id="5c695-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5c695-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5c695-117">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5c695-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5c695-118">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5c695-118">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5c695-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5c695-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c695-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="5c695-120">See also</span></span>

- [<span data-ttu-id="5c695-121">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="5c695-121">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
