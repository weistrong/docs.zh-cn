---
description: 了解详细信息： IAssemblyCache：： UninstallAssembly 方法
title: IAssemblyCache::UninstallAssembly 方法
ms.date: 03/30/2017
api_name:
- IAssemblyCache.UninstallAssembly
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache::UninstallAssembly
helpviewer_keywords:
- UninstallAssembly method [.NET Framework fusion]
- IAssemblyCache::UninstallAssembly method [.NET Framework fusion]
ms.assetid: 973b2c44-8dfc-40c1-9035-10f4846627e9
topic_type:
- apiref
ms.openlocfilehash: d50108b9090b4250e8a6cec1d9b5c54bb78dee9c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760896"
---
# <a name="iassemblycacheuninstallassembly-method"></a><span data-ttu-id="a7461-103">IAssemblyCache::UninstallAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="a7461-103">IAssemblyCache::UninstallAssembly Method</span></span>

<span data-ttu-id="a7461-104">从全局程序集缓存中卸载指定的程序集。</span><span class="sxs-lookup"><span data-stu-id="a7461-104">Uninstalls the specified assembly from the global assembly cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a7461-105">语法</span><span class="sxs-lookup"><span data-stu-id="a7461-105">Syntax</span></span>  
  
```cpp  
HRESULT UninstallAssembly (  
    [in] DWORD dwFlags,  
    [in] LPCWSTR pszAssemblyName,  
    [in] LPCFUSION_INSTALL_REFERENCE pRefData,  
    [out, optional] ULONG *pulDisposition  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a7461-106">参数</span><span class="sxs-lookup"><span data-stu-id="a7461-106">Parameters</span></span>  

 `dwFlags`  
 <span data-ttu-id="a7461-107">中在合成 .idl 中定义的标志。</span><span class="sxs-lookup"><span data-stu-id="a7461-107">[in] Flags defined in Fusion.idl.</span></span>  
  
 `pszAssemblyName`  
 <span data-ttu-id="a7461-108">中要卸载的程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="a7461-108">[in] The name of the assembly to uninstall.</span></span>  
  
 `pRefData`  
 <span data-ttu-id="a7461-109">中一个 [FUSION_INSTALL_REFERENCE](fusion-install-reference-structure.md) 结构，它包含程序集的安装数据。</span><span class="sxs-lookup"><span data-stu-id="a7461-109">[in] A [FUSION_INSTALL_REFERENCE](fusion-install-reference-structure.md) structure that contains the installation data for the assembly.</span></span>  
  
 `pulDisposition`  
 <span data-ttu-id="a7461-110">[out，optional]在合成 .idl 中定义的一个处置值。</span><span class="sxs-lookup"><span data-stu-id="a7461-110">[out, optional] One of the disposition values defined in Fusion.idl.</span></span> <span data-ttu-id="a7461-111">可能的值如下所示：</span><span class="sxs-lookup"><span data-stu-id="a7461-111">Possible values include the following:</span></span>  
  
- <span data-ttu-id="a7461-112">IASSEMBLYCACHE_UNINSTALL_DISPOSITION_UNINSTALLED (1) </span><span class="sxs-lookup"><span data-stu-id="a7461-112">IASSEMBLYCACHE_UNINSTALL_DISPOSITION_UNINSTALLED (1)</span></span>  
  
- <span data-ttu-id="a7461-113">IASSEMBLYCACHE_UNINSTALL_DISPOSITION_STILL_IN_USE (2) </span><span class="sxs-lookup"><span data-stu-id="a7461-113">IASSEMBLYCACHE_UNINSTALL_DISPOSITION_STILL_IN_USE (2)</span></span>  
  
- <span data-ttu-id="a7461-114">IASSEMBLYCACHE_UNINSTALL_DISPOSITION_ALREADY_UNINSTALLED (3) </span><span class="sxs-lookup"><span data-stu-id="a7461-114">IASSEMBLYCACHE_UNINSTALL_DISPOSITION_ALREADY_UNINSTALLED (3)</span></span>  
  
- <span data-ttu-id="a7461-115">IASSEMBLYCACHE_UNINSTALL_DISPOSITION_DELETE_PENDING (4) </span><span class="sxs-lookup"><span data-stu-id="a7461-115">IASSEMBLYCACHE_UNINSTALL_DISPOSITION_DELETE_PENDING (4)</span></span>  
  
- <span data-ttu-id="a7461-116">IASSEMBLYCACHE_UNINSTALL_DISPOSITION_HAS_INSTALL_REFERENCES (5) </span><span class="sxs-lookup"><span data-stu-id="a7461-116">IASSEMBLYCACHE_UNINSTALL_DISPOSITION_HAS_INSTALL_REFERENCES (5)</span></span>  
  
- <span data-ttu-id="a7461-117">IASSEMBLYCACHE_UNINSTALL_DISPOSITION_REFERENCE_NOT_FOUND (6) </span><span class="sxs-lookup"><span data-stu-id="a7461-117">IASSEMBLYCACHE_UNINSTALL_DISPOSITION_REFERENCE_NOT_FOUND (6)</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a7461-118">要求</span><span class="sxs-lookup"><span data-stu-id="a7461-118">Requirements</span></span>  

 <span data-ttu-id="a7461-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a7461-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a7461-120">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="a7461-120">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="a7461-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a7461-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a7461-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="a7461-122">See also</span></span>

- [<span data-ttu-id="a7461-123">IAssemblyCache 接口</span><span class="sxs-lookup"><span data-stu-id="a7461-123">IAssemblyCache Interface</span></span>](iassemblycache-interface.md)
