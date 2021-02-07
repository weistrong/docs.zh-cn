---
description: 了解详细信息： IMetaDataAssemblyEmit：： SetAssemblyProps 方法
title: IMetaDataAssemblyEmit::SetAssemblyProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.SetAssemblyProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::SetAssemblyProps
helpviewer_keywords:
- SetAssemblyProps method [.NET Framework metadata]
- IMetaDataAssemblyEmit::SetAssemblyProps method [.NET Framework metadata]
ms.assetid: 91b633d7-9e75-43c3-a8d2-2144984e5f9e
topic_type:
- apiref
ms.openlocfilehash: d5dfb5fa472bb83863c8e4909998deeb2b9fc53b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678193"
---
# <a name="imetadataassemblyemitsetassemblyprops-method"></a><span data-ttu-id="84024-103">IMetaDataAssemblyEmit::SetAssemblyProps 方法</span><span class="sxs-lookup"><span data-stu-id="84024-103">IMetaDataAssemblyEmit::SetAssemblyProps Method</span></span>

<span data-ttu-id="84024-104">修改指定的 `Assembly` 元数据结构。</span><span class="sxs-lookup"><span data-stu-id="84024-104">Modifies the specified `Assembly` metadata structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84024-105">语法</span><span class="sxs-lookup"><span data-stu-id="84024-105">Syntax</span></span>  
  
```cpp  
HRESULT SetAssemblyProps (  
    [in] mdAssembly               pma,  
    [in] const void               *pbPublicKey,  
    [in] ULONG                    cbPublicKey,  
    [in] ULONG                    ulHashAlgId,  
    [in] LPCWSTR                  szName,  
    [in] const ASSEMBLYMETADATA   *pMetaData,  
    [in] DWORD                    dwAssemblyFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="84024-106">参数</span><span class="sxs-lookup"><span data-stu-id="84024-106">Parameters</span></span>  

 `pma`  
 <span data-ttu-id="84024-107">中 `Assembly` 用于指定要修改的元数据结构的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="84024-107">[in] The metadata token that specifies the `Assembly` metadata structure to be modified.</span></span>  
  
 `pbPublicKey`  
 <span data-ttu-id="84024-108">中指向程序集发布者的公钥的指针。</span><span class="sxs-lookup"><span data-stu-id="84024-108">[in] A pointer to the public key of the publisher of the assembly.</span></span>  
  
 `cbPublicKey`  
 <span data-ttu-id="84024-109">中的大小（以字节为单位） `pbPublicKey` 。</span><span class="sxs-lookup"><span data-stu-id="84024-109">[in] The size in bytes of `pbPublicKey`.</span></span>  
  
 `ulHashAlgId`  
 <span data-ttu-id="84024-110">中用于对程序集文件进行哈希处理的哈希算法的标识符。</span><span class="sxs-lookup"><span data-stu-id="84024-110">[in] The identifier for the hash algorithm used to hash the assembly files.</span></span>  
  
 `szName`  
 <span data-ttu-id="84024-111">中程序集的用户可读文本名称。</span><span class="sxs-lookup"><span data-stu-id="84024-111">[in] The human-readable text name of the assembly.</span></span>  
  
 `pMetaData`  
 <span data-ttu-id="84024-112">中指向包含程序集的版本、平台和区域设置信息的 ASSEMBLYMETADATA 的指针。</span><span class="sxs-lookup"><span data-stu-id="84024-112">[in] A pointer to the ASSEMBLYMETADATA that contains version, platform, and locale information for the assembly.</span></span>  
  
 `dwAssemblyFlags`  
 <span data-ttu-id="84024-113">中 [AssemblyFlags](assemblyflags-enumeration.md) 值的按位组合，用于指定程序集的各种属性。</span><span class="sxs-lookup"><span data-stu-id="84024-113">[in] A bitwise combination of [AssemblyFlags](assemblyflags-enumeration.md) values that specify various attributes of the assembly.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="84024-114">备注</span><span class="sxs-lookup"><span data-stu-id="84024-114">Remarks</span></span>  

 <span data-ttu-id="84024-115">若要创建 `Assembly` 元数据结构，请使用 [IMetaDataAssemblyEmit：:D efineassembly](imetadataassemblyemit-defineassembly-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="84024-115">To create an `Assembly` metadata structure, use the [IMetaDataAssemblyEmit::DefineAssembly](imetadataassemblyemit-defineassembly-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="84024-116">要求</span><span class="sxs-lookup"><span data-stu-id="84024-116">Requirements</span></span>  

 <span data-ttu-id="84024-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="84024-117">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="84024-118">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="84024-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="84024-119">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="84024-119">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="84024-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="84024-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84024-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="84024-121">See also</span></span>

- [<span data-ttu-id="84024-122">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="84024-122">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
