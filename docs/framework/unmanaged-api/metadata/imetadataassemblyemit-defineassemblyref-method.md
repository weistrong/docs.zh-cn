---
description: 了解详细信息： IMetaDataAssemblyEmit：:D efineAssemblyRef 方法
title: IMetaDataAssemblyEmit::DefineAssemblyRef 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.DefineAssemblyRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::DefineAssemblyRef
helpviewer_keywords:
- DefineAssemblyRef method [.NET Framework metadata]
- IMetaDataAssemblyEmit::DefineAssemblyRef method [.NET Framework metadata]
ms.assetid: 0b284b18-0084-4b3a-912a-5ebe9f29c88b
topic_type:
- apiref
ms.openlocfilehash: e3c3acce77e6b0cb2943d66f3477898c90ea6251
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706690"
---
# <a name="imetadataassemblyemitdefineassemblyref-method"></a><span data-ttu-id="da28b-103">IMetaDataAssemblyEmit::DefineAssemblyRef 方法</span><span class="sxs-lookup"><span data-stu-id="da28b-103">IMetaDataAssemblyEmit::DefineAssemblyRef Method</span></span>

<span data-ttu-id="da28b-104">创建包含此程序集引用的程序集的元数据的 `AssemblyRef` 结构，并返回关联的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="da28b-104">Creates an `AssemblyRef` structure containing metadata for the assembly that this assembly references, and returns the associated metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da28b-105">语法</span><span class="sxs-lookup"><span data-stu-id="da28b-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineAssemblyRef (  
    [in]  void                *pbPublicKeyOrToken,  
    [in]  ULONG               cbPublicKeyOrToken,  
    [in]  LPCWSTR             szName,  
    [in]  ASSEMBLYMETADATA    pMetaData,  
    [in]  void                *pbHashValue,  
    [in]  ULONG               cbHashValue,  
    [in]  DWORD               dwAssemblyRefFlags,  
    [out] mdAssemblyRef       *pmdar  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="da28b-106">参数</span><span class="sxs-lookup"><span data-stu-id="da28b-106">Parameters</span></span>  

 `pbPublicKeyOrToken`  
 <span data-ttu-id="da28b-107">中所引用程序集的发行者的公钥。</span><span class="sxs-lookup"><span data-stu-id="da28b-107">[in] The public key of the publisher of the referenced assembly.</span></span> <span data-ttu-id="da28b-108">Helper 函数 [StrongNameTokenFromAssembly](../strong-naming/strongnametokenfromassembly-function.md) 可用于获取公钥哈希作为此参数传递。</span><span class="sxs-lookup"><span data-stu-id="da28b-108">The helper function [StrongNameTokenFromAssembly](../strong-naming/strongnametokenfromassembly-function.md) can be used to get the hash of the public key to pass as this parameter.</span></span>  
  
 `cbPublicKeyOrToken`  
 <span data-ttu-id="da28b-109">中的大小（以字节为单位） `pbPublicKeyOrToken` 。</span><span class="sxs-lookup"><span data-stu-id="da28b-109">[in] The size in bytes of `pbPublicKeyOrToken`.</span></span>  
  
 `szName`  
 <span data-ttu-id="da28b-110">中程序集的用户可读文本名称。</span><span class="sxs-lookup"><span data-stu-id="da28b-110">[in] The human-readable text name of the assembly.</span></span> <span data-ttu-id="da28b-111">此值不能超过1024个字符。</span><span class="sxs-lookup"><span data-stu-id="da28b-111">This value must not exceed 1024 characters.</span></span>  
  
 `pMetaData`  
 <span data-ttu-id="da28b-112">中一个 ASSEMBLYMETADATA 实例，其中包含所引用程序集的版本、平台和区域设置信息。</span><span class="sxs-lookup"><span data-stu-id="da28b-112">[in] An ASSEMBLYMETADATA instance that contains the version, platform and locale information of the referenced assembly.</span></span>  
  
 `pbHashValue`  
 <span data-ttu-id="da28b-113">中与所引用的程序集关联的哈希数据。</span><span class="sxs-lookup"><span data-stu-id="da28b-113">[in] The hash data associated with the referenced assembly.</span></span> <span data-ttu-id="da28b-114">可选。</span><span class="sxs-lookup"><span data-stu-id="da28b-114">Optional.</span></span>  
  
 `cbHashValue`  
 <span data-ttu-id="da28b-115">中的大小（以字节为单位） `pbHashValue` 。</span><span class="sxs-lookup"><span data-stu-id="da28b-115">[in] The size in bytes of `pbHashValue`.</span></span>  
  
 `dwAssemblyRefFlags`  
 <span data-ttu-id="da28b-116">中影响执行引擎行为的 [CorAssemblyFlags](corassemblyflags-enumeration.md) 值的按位组合。</span><span class="sxs-lookup"><span data-stu-id="da28b-116">[in] A bitwise combination of [CorAssemblyFlags](corassemblyflags-enumeration.md) values that influence the behavior of the execution engine.</span></span>  
  
 `pmdar`  
 <span data-ttu-id="da28b-117">弄指向返回的 `AssemblyRef` 元数据标记的指针。</span><span class="sxs-lookup"><span data-stu-id="da28b-117">[out] A pointer to the returned `AssemblyRef` metadata token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="da28b-118">备注</span><span class="sxs-lookup"><span data-stu-id="da28b-118">Remarks</span></span>  

 <span data-ttu-id="da28b-119">`AssemblyRef`必须为此程序集引用的每个程序集定义一个元数据结构。</span><span class="sxs-lookup"><span data-stu-id="da28b-119">One `AssemblyRef` metadata structure must be defined for each assembly that this assembly references.</span></span>  
  
 <span data-ttu-id="da28b-120">在运行时，被引用程序集的详细信息将传递给程序集解析程序，并指示它们表示 "生成的" 信息。</span><span class="sxs-lookup"><span data-stu-id="da28b-120">At run time, the details of a referenced assembly are passed to the assembly resolver with an indication that they represent the "as built" information.</span></span> <span data-ttu-id="da28b-121">然后，程序集冲突解决程序将应用策略。</span><span class="sxs-lookup"><span data-stu-id="da28b-121">The assembly resolver then applies policy.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="da28b-122">要求</span><span class="sxs-lookup"><span data-stu-id="da28b-122">Requirements</span></span>  

 <span data-ttu-id="da28b-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="da28b-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="da28b-124">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="da28b-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="da28b-125">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="da28b-125">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="da28b-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="da28b-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da28b-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="da28b-127">See also</span></span>

- [<span data-ttu-id="da28b-128">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="da28b-128">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
