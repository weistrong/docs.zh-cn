---
description: 了解详细信息： IAssemblyCache：： InstallAssembly 方法
title: IAssemblyCache::InstallAssembly 方法
ms.date: 03/30/2017
api_name:
- IAssemblyCache.InstallAssembly
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache::InstallAssembly
helpviewer_keywords:
- InstallAssembly method [.NET Framework fusion]
- IAssemblyCache::InstallAssembly method [.NET Framework fusion]
ms.assetid: 33c1d269-c85e-4cb1-b0e6-1c510c8fb5fa
topic_type:
- apiref
ms.openlocfilehash: 0bb9fe31467506a03f5e81e5a29a6b1fb65f5804
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760935"
---
# <a name="iassemblycacheinstallassembly-method"></a><span data-ttu-id="f8107-103">IAssemblyCache::InstallAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="f8107-103">IAssemblyCache::InstallAssembly Method</span></span>

<span data-ttu-id="f8107-104">在全局程序集缓存中安装指定的程序集。</span><span class="sxs-lookup"><span data-stu-id="f8107-104">Installs the specified assembly in the global assembly cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8107-105">语法</span><span class="sxs-lookup"><span data-stu-id="f8107-105">Syntax</span></span>  
  
```cpp  
HRESULT InstallAssembly (  
    [in] DWORD dwFlags,  
    [in] LPCWSTR pszManifestFilePath,  
    [in] LPCFUSION_INSTALL_REFERENCE pRefData  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f8107-106">参数</span><span class="sxs-lookup"><span data-stu-id="f8107-106">Parameters</span></span>  

 `dwFlags`  
 <span data-ttu-id="f8107-107">中在合成 .idl 中定义的标志。</span><span class="sxs-lookup"><span data-stu-id="f8107-107">[in] Flags defined in Fusion.idl.</span></span> <span data-ttu-id="f8107-108">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="f8107-108">The following values are supported:</span></span>  
  
- <span data-ttu-id="f8107-109"> (0x00000001) IASSEMBLYCACHE_INSTALL_FLAG_REFRESH</span><span class="sxs-lookup"><span data-stu-id="f8107-109">IASSEMBLYCACHE_INSTALL_FLAG_REFRESH (0x00000001)</span></span>  
  
- <span data-ttu-id="f8107-110">IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="f8107-110">IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH (0x00000002)</span></span>  
  
 `pszManifestFilePath`  
 <span data-ttu-id="f8107-111">中要安装的程序集的清单的路径。</span><span class="sxs-lookup"><span data-stu-id="f8107-111">[in] The path to the manifest for the assembly to install.</span></span>  
  
 `pRefData`  
 <span data-ttu-id="f8107-112">中一个 [FUSION_INSTALL_REFERENCE](fusion-install-reference-structure.md) 结构，它包含安装的数据。</span><span class="sxs-lookup"><span data-stu-id="f8107-112">[in] A [FUSION_INSTALL_REFERENCE](fusion-install-reference-structure.md) structure that contains data for the installation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f8107-113">要求</span><span class="sxs-lookup"><span data-stu-id="f8107-113">Requirements</span></span>  

 <span data-ttu-id="f8107-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f8107-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f8107-115">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="f8107-115">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="f8107-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f8107-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8107-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="f8107-117">See also</span></span>

- [<span data-ttu-id="f8107-118">IAssemblyCache 接口</span><span class="sxs-lookup"><span data-stu-id="f8107-118">IAssemblyCache Interface</span></span>](iassemblycache-interface.md)
