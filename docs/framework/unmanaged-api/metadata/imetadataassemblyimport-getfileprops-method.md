---
description: 了解详细信息： IMetaDataAssemblyImport：： GetFileProps 方法
title: IMetaDataAssemblyImport::GetFileProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetFileProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetFileProps
helpviewer_keywords:
- GetFileProps method [.NET Framework metadata]
- IMetaDataAssemblyImport::GetFileProps method [.NET Framework metadata]
ms.assetid: c5e6216f-ae3d-4697-9688-66b69c1251ec
topic_type:
- apiref
ms.openlocfilehash: 6814fee7edf5478a1ce2cf2b81d8f16fa62cd3f3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784101"
---
# <a name="imetadataassemblyimportgetfileprops-method"></a><span data-ttu-id="1d9ed-103">IMetaDataAssemblyImport::GetFileProps 方法</span><span class="sxs-lookup"><span data-stu-id="1d9ed-103">IMetaDataAssemblyImport::GetFileProps Method</span></span>

<span data-ttu-id="1d9ed-104">获取具有指定的元数据签名的文件的属性。</span><span class="sxs-lookup"><span data-stu-id="1d9ed-104">Gets the properties of the file with the specified metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1d9ed-105">语法</span><span class="sxs-lookup"><span data-stu-id="1d9ed-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFileProps (  
    [in]  mdFile      mdf,
    [out] LPWSTR      szName,
    [in]  ULONG       cchName,
    [out] ULONG       *pchName,
    [out] const void  **ppbHashValue,
    [out] ULONG       *pcbHashValue,
    [out] DWORD       *pdwFileFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1d9ed-106">参数</span><span class="sxs-lookup"><span data-stu-id="1d9ed-106">Parameters</span></span>  

 `mdf`  
 <span data-ttu-id="1d9ed-107">中 `mdFile` 表示要获取其属性的文件的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="1d9ed-107">[in] The `mdFile` metadata token that represents the file for which to get the properties.</span></span>  
  
 `szName`  
 <span data-ttu-id="1d9ed-108">弄文件的简单名称。</span><span class="sxs-lookup"><span data-stu-id="1d9ed-108">[out] The simple name of the file.</span></span>  
  
 `cchName`  
 <span data-ttu-id="1d9ed-109">中的大小（宽字符） `szName` 。</span><span class="sxs-lookup"><span data-stu-id="1d9ed-109">[in] The size, in wide chars, of `szName`.</span></span>  
  
 `pchName`  
 <span data-ttu-id="1d9ed-110">弄中实际返回的宽字符数 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="1d9ed-110">[out] The number of wide chars actually returned in `szName`.</span></span>  
  
 `ppbHashValue`  
 <span data-ttu-id="1d9ed-111">弄指向哈希值的指针。</span><span class="sxs-lookup"><span data-stu-id="1d9ed-111">[out] A pointer to the hash value.</span></span> <span data-ttu-id="1d9ed-112">这是文件的哈希，使用 SHA-1 算法。</span><span class="sxs-lookup"><span data-stu-id="1d9ed-112">This is the hash, using the SHA-1 algorithm, of the file.</span></span>  
  
 `pcbHashValue`  
 <span data-ttu-id="1d9ed-113">弄返回的哈希值中的宽字符数。</span><span class="sxs-lookup"><span data-stu-id="1d9ed-113">[out] The number of wide chars in the returned hash value.</span></span>  
  
 `pdwFileFlags`  
 <span data-ttu-id="1d9ed-114">弄一个指针，指向描述应用于文件的元数据的标志。</span><span class="sxs-lookup"><span data-stu-id="1d9ed-114">[out] A pointer to the flags that describe the metadata applied to a file.</span></span> <span data-ttu-id="1d9ed-115">Flags 值是一个或多个 [CorFileFlags](corfileflags-enumeration.md) 值的组合。</span><span class="sxs-lookup"><span data-stu-id="1d9ed-115">The flags value is a combination of one or more [CorFileFlags](corfileflags-enumeration.md) values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1d9ed-116">要求</span><span class="sxs-lookup"><span data-stu-id="1d9ed-116">Requirements</span></span>  

 <span data-ttu-id="1d9ed-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1d9ed-117">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1d9ed-118">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="1d9ed-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1d9ed-119">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="1d9ed-119">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1d9ed-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1d9ed-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d9ed-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="1d9ed-121">See also</span></span>

- [<span data-ttu-id="1d9ed-122">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="1d9ed-122">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
