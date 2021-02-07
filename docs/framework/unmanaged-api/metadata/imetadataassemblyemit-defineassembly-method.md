---
description: 了解详细信息： IMetaDataAssemblyEmit：:D efineAssembly 方法
title: IMetaDataAssemblyEmit::DefineAssembly 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.DefineAssembly
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::DefineAssembly
helpviewer_keywords:
- IMetaDataAssemblyEmit::DefineAssembly method [.NET Framework metadata]
- DefineAssembly method [.NET Framework metadata]
ms.assetid: a0637d66-74bf-4f2d-8137-9ff838bccece
topic_type:
- apiref
ms.openlocfilehash: cd53a4398f49ca96072fc5f5b6dcac35a94bdc59
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706739"
---
# <a name="imetadataassemblyemitdefineassembly-method"></a><span data-ttu-id="11913-103">IMetaDataAssemblyEmit::DefineAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="11913-103">IMetaDataAssemblyEmit::DefineAssembly Method</span></span>

<span data-ttu-id="11913-104">创建 `Assembly` 包含指定程序集的元数据的结构，并返回关联的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="11913-104">Creates an `Assembly` structure containing metadata for the specified assembly and returns the associated metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="11913-105">语法</span><span class="sxs-lookup"><span data-stu-id="11913-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineAssembly (  
    [in]  void                 *pbPublicKey,  
    [in]  ULONG                cbPublicKey,  
    [in]  ULONG                uHashAlgId,  
    [in]  LPCWSTR              szName,
    [in]  ASSEMBLYMETADATA     *pMetaData,  
    [in]  DWORD                dwAssemblyFlags,  
    [out] mdAssembly           *pmda  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="11913-106">参数</span><span class="sxs-lookup"><span data-stu-id="11913-106">Parameters</span></span>  

 `pbPublicKey`  
 <span data-ttu-id="11913-107">中标识程序集发行者的公钥; 如果程序集没有强名称，则为 NULL。</span><span class="sxs-lookup"><span data-stu-id="11913-107">[in] The public key that identifies the publisher of the assembly, or NULL if the assembly is not strongly named.</span></span>  
  
 `cbPublicKey`  
 <span data-ttu-id="11913-108">中的大小（以字节为单位） `pbPublicKey` 。</span><span class="sxs-lookup"><span data-stu-id="11913-108">[in] The size in bytes of `pbPublicKey`.</span></span>  
  
 `uHashAlgId`  
 <span data-ttu-id="11913-109">中用于对程序集中的文件进行加密的哈希算法的标识符; 如果为 NULL，则指定 SHA-1 算法。</span><span class="sxs-lookup"><span data-stu-id="11913-109">[in] The identifier of the hashing algorithm to use to encrypt the files in the assembly, or NULL to specify the SHA-1 algorithm.</span></span>  
  
 `szName`  
 <span data-ttu-id="11913-110">中程序集的用户可读文本名称。</span><span class="sxs-lookup"><span data-stu-id="11913-110">[in] The human-readable text name of the assembly.</span></span> <span data-ttu-id="11913-111">此值不能超过1024个字符。</span><span class="sxs-lookup"><span data-stu-id="11913-111">This value must not exceed 1024 characters.</span></span>  
  
 `pMetaData`  
 <span data-ttu-id="11913-112">中指向 ASSEMBLYMETADATA 实例的指针，其中包含程序集的版本、平台和区域设置信息。</span><span class="sxs-lookup"><span data-stu-id="11913-112">[in] A pointer to an ASSEMBLYMETADATA instance that contains the version, platform, and locale information for the assembly.</span></span>  
  
 `dwAssemblyFlags`  
 <span data-ttu-id="11913-113">中 [CorAssemblyFlags](corassemblyflags-enumeration.md) 值的组合，用于描述程序集的功能。</span><span class="sxs-lookup"><span data-stu-id="11913-113">[in] A combination of [CorAssemblyFlags](corassemblyflags-enumeration.md) values that describe features of the assembly.</span></span>  
  
 `pmda`  
 <span data-ttu-id="11913-114">弄指向元数据标记的指针。</span><span class="sxs-lookup"><span data-stu-id="11913-114">[out] A pointer to the metadata token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="11913-115">备注</span><span class="sxs-lookup"><span data-stu-id="11913-115">Remarks</span></span>  

 <span data-ttu-id="11913-116">`Assembly`清单中只能定义一个元数据结构。</span><span class="sxs-lookup"><span data-stu-id="11913-116">Only one `Assembly` metadata structure can be defined within a manifest.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="11913-117">要求</span><span class="sxs-lookup"><span data-stu-id="11913-117">Requirements</span></span>  

 <span data-ttu-id="11913-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="11913-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="11913-119">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="11913-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="11913-120">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="11913-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="11913-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="11913-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="11913-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="11913-122">See also</span></span>

- [<span data-ttu-id="11913-123">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="11913-123">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
