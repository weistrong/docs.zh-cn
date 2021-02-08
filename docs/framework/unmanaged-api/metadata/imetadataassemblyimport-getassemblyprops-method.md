---
description: 了解详细信息： IMetaDataAssemblyImport：： GetAssemblyProps 方法
title: IMetaDataAssemblyImport::GetAssemblyProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetAssemblyProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetAssemblyProps
helpviewer_keywords:
- GetAssemblyProps method [.NET Framework metadata]
- IMetaDataAssemblyImport::GetAssemblyProps method [.NET Framework metadata]
ms.assetid: 0eaa4aa9-9441-444a-920c-e4b2a2db899e
topic_type:
- apiref
ms.openlocfilehash: 9cd3674dcd640bce27ae5d399d0f7de0c2eeca48
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784140"
---
# <a name="imetadataassemblyimportgetassemblyprops-method"></a><span data-ttu-id="b038c-103">IMetaDataAssemblyImport::GetAssemblyProps 方法</span><span class="sxs-lookup"><span data-stu-id="b038c-103">IMetaDataAssemblyImport::GetAssemblyProps Method</span></span>

<span data-ttu-id="b038c-104">获取具有指定元数据签名的程序集的属性集。</span><span class="sxs-lookup"><span data-stu-id="b038c-104">Gets the set of properties for the assembly with the specified metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b038c-105">语法</span><span class="sxs-lookup"><span data-stu-id="b038c-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAssemblyProps (  
    [in]  mdAssembly          mda,  
    [out] const void          **ppbPublicKey,
    [out] ULONG               *pcbPublicKey,  
    [out] ULONG               *pulHashAlgId,  
    [out] LPWSTR              szName,  
    [in] ULONG                cchName,  
    [out] ULONG               *pchName,  
    [out] ASSEMBLYMETADATA    *pMetaData,  
    [out] DWORD               *pdwAssemblyFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b038c-106">参数</span><span class="sxs-lookup"><span data-stu-id="b038c-106">Parameters</span></span>  

 `mda`  
 <span data-ttu-id="b038c-107">[in]。</span><span class="sxs-lookup"><span data-stu-id="b038c-107">[in].</span></span> <span data-ttu-id="b038c-108">`mdAssembly`表示要获取其属性的程序集的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="b038c-108">The `mdAssembly` metadata token that represents the assembly for which to get the properties.</span></span>  
  
 `ppbPublicKey`  
 <span data-ttu-id="b038c-109">弄指向公钥或元数据标记的指针。</span><span class="sxs-lookup"><span data-stu-id="b038c-109">[out] A pointer to the public key or the metadata token.</span></span>  
  
 `pcbPublicKey`  
 <span data-ttu-id="b038c-110">弄返回的公钥中的字节数。</span><span class="sxs-lookup"><span data-stu-id="b038c-110">[out] The number of bytes in the returned public key.</span></span>  
  
 `pulHashAlgId`  
 <span data-ttu-id="b038c-111">弄一个指针，指向用于对程序集中的文件进行哈希处理的算法。</span><span class="sxs-lookup"><span data-stu-id="b038c-111">[out] A pointer to the algorithm used to hash the files in the assembly.</span></span>  
  
 `szName`  
 <span data-ttu-id="b038c-112">弄程序集的简单名称。</span><span class="sxs-lookup"><span data-stu-id="b038c-112">[out] The simple name of the assembly.</span></span>  
  
 `cchName`  
 <span data-ttu-id="b038c-113">中的大小（宽字符） `szName` 。</span><span class="sxs-lookup"><span data-stu-id="b038c-113">[in] The size, in wide chars, of `szName`.</span></span>  
  
 `pchName`  
 <span data-ttu-id="b038c-114">弄中实际返回的宽字符数 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="b038c-114">[out] The number of wide chars actually returned in `szName`.</span></span>  
  
 `pMetaData`  
 <span data-ttu-id="b038c-115">弄指向 ASSEMBLYMETADATA 结构的指针，该结构包含程序集元数据。</span><span class="sxs-lookup"><span data-stu-id="b038c-115">[out] A pointer to an ASSEMBLYMETADATA structure that contains the assembly metadata.</span></span>  
  
 `pdwAssemblyFlags`  
 <span data-ttu-id="b038c-116">弄描述应用于程序集的元数据的标志。</span><span class="sxs-lookup"><span data-stu-id="b038c-116">[out] Flags that describe the metadata applied to an assembly.</span></span> <span data-ttu-id="b038c-117">此值是一个或多个 [CorAssemblyFlags](corassemblyflags-enumeration.md) 值的组合。</span><span class="sxs-lookup"><span data-stu-id="b038c-117">This value is a combination of one or more [CorAssemblyFlags](corassemblyflags-enumeration.md) values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b038c-118">要求</span><span class="sxs-lookup"><span data-stu-id="b038c-118">Requirements</span></span>  

 <span data-ttu-id="b038c-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b038c-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b038c-120">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="b038c-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b038c-121">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="b038c-121">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b038c-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b038c-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b038c-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="b038c-123">See also</span></span>

- [<span data-ttu-id="b038c-124">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="b038c-124">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
