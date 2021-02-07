---
description: 了解详细信息： IMetaDataDispenserEx：： FindAssembly 方法
title: IMetaDataDispenserEx::FindAssembly 方法
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.FindAssembly
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::FindAssembly
helpviewer_keywords:
- FindAssembly method [.NET Framework metadata]
- IMetaDataDispenserEx::FindAssembly method [.NET Framework metadata]
ms.assetid: 3afe7252-5f28-48d9-a74d-1927566c404c
topic_type:
- apiref
ms.openlocfilehash: 6bed016e9235281b42f5a3231ef2aff284b6cc3b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753596"
---
# <a name="imetadatadispenserexfindassembly-method"></a><span data-ttu-id="2793d-103">IMetaDataDispenserEx::FindAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="2793d-103">IMetaDataDispenserEx::FindAssembly Method</span></span>

<span data-ttu-id="2793d-104">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="2793d-104">This method is not implemented.</span></span> <span data-ttu-id="2793d-105">如果调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="2793d-105">If called, it returns E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2793d-106">语法</span><span class="sxs-lookup"><span data-stu-id="2793d-106">Syntax</span></span>  
  
```cpp  
HRESULT FindAssembly(  
    [in]  LPCWSTR  szAppBase,  
    [in]  LPCWSTR  szPrivateBin,  
    [in]  LPCWSTR  szGlobalBin,  
    [in]  LPCWSTR  szAssemblyName,  
    [out] LPCWSTR  szName,  
    [in]  ULONG    cchName,  
    [out] ULONG    *pcName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2793d-107">参数</span><span class="sxs-lookup"><span data-stu-id="2793d-107">Parameters</span></span>  

 `szAppBase`  
 <span data-ttu-id="2793d-108">中不使用。</span><span class="sxs-lookup"><span data-stu-id="2793d-108">[in] Not used.</span></span>  
  
 `szPrivateBin`  
 <span data-ttu-id="2793d-109">中不使用。</span><span class="sxs-lookup"><span data-stu-id="2793d-109">[in] Not used.</span></span>  
  
 `szGlobalBin`  
 <span data-ttu-id="2793d-110">中不使用。</span><span class="sxs-lookup"><span data-stu-id="2793d-110">[in] Not used.</span></span>  
  
 `szAssemblyName`  
 <span data-ttu-id="2793d-111">中要查找的程序集。</span><span class="sxs-lookup"><span data-stu-id="2793d-111">[in] The assembly to be found.</span></span>  
  
 `szName`  
 <span data-ttu-id="2793d-112">弄程序集的简单名称。</span><span class="sxs-lookup"><span data-stu-id="2793d-112">[out] The simple name of the assembly.</span></span>  
  
 `cchName`  
 <span data-ttu-id="2793d-113">中的大小（以字节为单位） `szName` 。</span><span class="sxs-lookup"><span data-stu-id="2793d-113">[in] The size, in bytes, of `szName`.</span></span>  
  
 `pcName`  
 <span data-ttu-id="2793d-114">弄中实际返回的字符数 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="2793d-114">[out] The number of characters actually returned in `szName`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2793d-115">要求</span><span class="sxs-lookup"><span data-stu-id="2793d-115">Requirements</span></span>  

 <span data-ttu-id="2793d-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2793d-116">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2793d-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="2793d-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="2793d-118">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="2793d-118">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="2793d-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2793d-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2793d-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="2793d-120">See also</span></span>

- [<span data-ttu-id="2793d-121">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="2793d-121">IMetaDataDispenserEx Interface</span></span>](imetadatadispenserex-interface.md)
- [<span data-ttu-id="2793d-122">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="2793d-122">IMetaDataDispenser Interface</span></span>](imetadatadispenser-interface.md)
