---
description: 了解详细信息： IMetaDataDispenserEx：： FindAssemblyModule 方法
title: IMetaDataDispenserEx::FindAssemblyModule 方法
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.FindAssemblyModule
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::FindAssemblyModule
helpviewer_keywords:
- FindAssemblyModule method [.NET Framework metadata]
- IMetaDataDispenserEx::FindAssemblyModule method [.NET Framework metadata]
ms.assetid: d1fb65e1-7e19-4513-85b1-44f87c294d3e
topic_type:
- apiref
ms.openlocfilehash: 39ea13a2d8f2436e86db513aaa33f990f43d8132
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753570"
---
# <a name="imetadatadispenserexfindassemblymodule-method"></a><span data-ttu-id="abde0-103">IMetaDataDispenserEx::FindAssemblyModule 方法</span><span class="sxs-lookup"><span data-stu-id="abde0-103">IMetaDataDispenserEx::FindAssemblyModule Method</span></span>

<span data-ttu-id="abde0-104">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="abde0-104">This method is not implemented.</span></span> <span data-ttu-id="abde0-105">如果调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="abde0-105">If called, it returns E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="abde0-106">语法</span><span class="sxs-lookup"><span data-stu-id="abde0-106">Syntax</span></span>  
  
```cpp  
HRESULT FindAssemblyModule(  
    [in]  LPCWSTR  szAppBase,  
    [in]  LPCWSTR  szPrivateBin,  
    [in]  LPCWSTR  szGlobalBin,  
    [in]  LPCWSTR  szAssemblyName,  
    [in]  LPCWSTR  szModuleName,  
    [out] LPCWSTR  szName,  
    [in]  ULONG    cchName,  
    [out] ULONG    *pcName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="abde0-107">参数</span><span class="sxs-lookup"><span data-stu-id="abde0-107">Parameters</span></span>  

 `szAppBase`  
 <span data-ttu-id="abde0-108">中不使用。</span><span class="sxs-lookup"><span data-stu-id="abde0-108">[in] Not used.</span></span>  
  
 `szPrivateBin`  
 <span data-ttu-id="abde0-109">中不使用。</span><span class="sxs-lookup"><span data-stu-id="abde0-109">[in] Not used.</span></span>  
  
 `szGlobalBin`  
 <span data-ttu-id="abde0-110">中不使用。</span><span class="sxs-lookup"><span data-stu-id="abde0-110">[in] Not used.</span></span>  
  
 `szAssemblyName`  
 <span data-ttu-id="abde0-111">中模块的名称。</span><span class="sxs-lookup"><span data-stu-id="abde0-111">[in] The name of the module.</span></span>  
  
 `szModuleName`  
 <span data-ttu-id="abde0-112">中要查找的程序集。</span><span class="sxs-lookup"><span data-stu-id="abde0-112">[in] The assembly to be found.</span></span>  
  
 `szName`  
 <span data-ttu-id="abde0-113">弄程序集的简单名称。</span><span class="sxs-lookup"><span data-stu-id="abde0-113">[out] The simple name of the assembly.</span></span>  
  
 `cchName`  
 <span data-ttu-id="abde0-114">中的大小（以字节为单位） `szName` 。</span><span class="sxs-lookup"><span data-stu-id="abde0-114">[in] The size, in bytes, of `szName`.</span></span>  
  
 `pcName`  
 <span data-ttu-id="abde0-115">弄中实际返回的字符数 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="abde0-115">[out] The number of characters actually returned in `szName`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="abde0-116">要求</span><span class="sxs-lookup"><span data-stu-id="abde0-116">Requirements</span></span>  

 <span data-ttu-id="abde0-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="abde0-117">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="abde0-118">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="abde0-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="abde0-119">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="abde0-119">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="abde0-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="abde0-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="abde0-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="abde0-121">See also</span></span>

- [<span data-ttu-id="abde0-122">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="abde0-122">IMetaDataDispenserEx Interface</span></span>](imetadatadispenserex-interface.md)
- [<span data-ttu-id="abde0-123">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="abde0-123">IMetaDataDispenser Interface</span></span>](imetadatadispenser-interface.md)
