---
description: 了解详细信息： IMetaDataAssemblyImport：： GetAssemblyRefProps 方法
title: IMetaDataAssemblyImport::GetAssemblyRefProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetAssemblyRefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetAssemblyRefProps
helpviewer_keywords:
- IMetaDataAssemblyImport::GetAssemblyRefProps method [.NET Framework metadata]
- GetAssemblyRefProps method [.NET Framework metadata]
ms.assetid: 5c6b7fb4-cbca-4479-b650-ab9a99732ea0
topic_type:
- apiref
ms.openlocfilehash: f7011806920ba37ca84b1a48f12da3a5557fa464
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784127"
---
# <a name="imetadataassemblyimportgetassemblyrefprops-method"></a><span data-ttu-id="f5be1-103">IMetaDataAssemblyImport::GetAssemblyRefProps 方法</span><span class="sxs-lookup"><span data-stu-id="f5be1-103">IMetaDataAssemblyImport::GetAssemblyRefProps Method</span></span>

<span data-ttu-id="f5be1-104">获取具有指定元数据签名的程序集引用的属性集。</span><span class="sxs-lookup"><span data-stu-id="f5be1-104">Gets the set of properties for the assembly reference with the specified metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5be1-105">语法</span><span class="sxs-lookup"><span data-stu-id="f5be1-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAssemblyRefProps (  
    [in]  mdAssemblyRef        mdar,
    [out] const void          **ppbPublicKeyOrToken,
    [out] ULONG                *pcbPublicKeyOrToken,
    [out] LPWSTR               szName,
    [in]  ULONG                cchName,
    [out] ULONG                *pchName,
    [out] ASSEMBLYMETADATA     *pMetaData,
    [out] const void           **ppbHashValue,
    [out] ULONG                *pcbHashValue,
    [out] DWORD                *pdwAssemblyRefFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f5be1-106">参数</span><span class="sxs-lookup"><span data-stu-id="f5be1-106">Parameters</span></span>  

 `mdar`  
 <span data-ttu-id="f5be1-107">中 `mdAssemblyRef` 表示要获取其属性的程序集引用的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="f5be1-107">[in] The `mdAssemblyRef` metadata token that represents the assembly reference for which to get the properties.</span></span>  
  
 `ppbPublicKeyOrToken`  
 <span data-ttu-id="f5be1-108">弄指向公钥或元数据标记的指针。</span><span class="sxs-lookup"><span data-stu-id="f5be1-108">[out] A pointer to the public key or the metadata token.</span></span>  
  
 `pcbPublicKeyOrToken`  
 <span data-ttu-id="f5be1-109">弄返回的公钥或令牌中的字节数。</span><span class="sxs-lookup"><span data-stu-id="f5be1-109">[out] The number of bytes in the returned public key or token.</span></span>  
  
 `szName`  
 <span data-ttu-id="f5be1-110">弄程序集的简单名称。</span><span class="sxs-lookup"><span data-stu-id="f5be1-110">[out] The simple name of the assembly.</span></span>  
  
 `cchName`  
 <span data-ttu-id="f5be1-111">中的大小（宽字符） `szName` 。</span><span class="sxs-lookup"><span data-stu-id="f5be1-111">[in] The size, in wide chars, of `szName`.</span></span>  
  
 `pchName`  
 <span data-ttu-id="f5be1-112">弄一个指针，指向在中实际返回的宽字符数 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="f5be1-112">[out] A pointer to the number of wide chars actually returned in `szName`.</span></span>  
  
 `pMetaData`  
 <span data-ttu-id="f5be1-113">弄指向 ASSEMBLYMETADATA 结构的指针，该结构包含程序集元数据。</span><span class="sxs-lookup"><span data-stu-id="f5be1-113">[out] A pointer to an ASSEMBLYMETADATA structure that contains the assembly metadata.</span></span>  
  
 `ppbHashValue`  
 <span data-ttu-id="f5be1-114">弄指向哈希值的指针。</span><span class="sxs-lookup"><span data-stu-id="f5be1-114">[out] A pointer to the hash value.</span></span> <span data-ttu-id="f5be1-115">这是所引用程序集的属性的哈希，使用 SHA-1 算法， `PublicKey` 除非已设置 [AssemblyRefFlags](assemblyrefflags-enumeration.md) 枚举的 arfFullOriginator 标志。</span><span class="sxs-lookup"><span data-stu-id="f5be1-115">This is the hash, using the SHA-1 algorithm, of the `PublicKey` property of the assembly being referenced, unless the arfFullOriginator flag of the [AssemblyRefFlags](assemblyrefflags-enumeration.md) enumeration is set.</span></span>  
  
 `pcbHashValue`  
 <span data-ttu-id="f5be1-116">弄返回的哈希值中的宽字符数。</span><span class="sxs-lookup"><span data-stu-id="f5be1-116">[out] The number of wide chars in the returned hash value.</span></span>  
  
 `pdwAssemblyRefFlags`  
 <span data-ttu-id="f5be1-117">弄一个指针，指向用于描述应用于程序集的元数据的标志。</span><span class="sxs-lookup"><span data-stu-id="f5be1-117">[out] A pointer to flags that describe the metadata applied to an assembly.</span></span> <span data-ttu-id="f5be1-118">Flags 值是一个或多个 [CorAssemblyFlags](corassemblyflags-enumeration.md) 值的组合。</span><span class="sxs-lookup"><span data-stu-id="f5be1-118">The flags value is a combination of one or more [CorAssemblyFlags](corassemblyflags-enumeration.md) values.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f5be1-119">返回值</span><span class="sxs-lookup"><span data-stu-id="f5be1-119">Return Value</span></span>  

 <span data-ttu-id="f5be1-120">如果成功，则此方法返回 S_OK;否则，它将返回在 Winerror.h 头文件中定义的错误代码之一。</span><span class="sxs-lookup"><span data-stu-id="f5be1-120">This method returns S_OK if it succeeds; otherwise, it returns one of the error codes defined in the Winerror.h header file.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f5be1-121">要求</span><span class="sxs-lookup"><span data-stu-id="f5be1-121">Requirements</span></span>  

 <span data-ttu-id="f5be1-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f5be1-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f5be1-123">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f5be1-123">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f5be1-124">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="f5be1-124">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f5be1-125">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f5be1-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f5be1-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="f5be1-126">See also</span></span>

- [<span data-ttu-id="f5be1-127">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="f5be1-127">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
