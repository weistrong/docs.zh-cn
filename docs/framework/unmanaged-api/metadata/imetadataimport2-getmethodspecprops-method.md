---
description: 了解详细信息： IMetaDataImport2：： GetMethodSpecProps 方法
title: IMetaDataImport2::GetMethodSpecProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetMethodSpecProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetMethodSpecProps
helpviewer_keywords:
- GetMethodSpecProps method [.NET Framework metadata]
- IMetaDataImport2::GetMethodSpecProps method [.NET Framework metadata]
ms.assetid: 9544b711-e669-4eaf-8630-ee862e5e4489
topic_type:
- apiref
ms.openlocfilehash: 77f3f78905d1f7f44af0e9c7a75746b4e5b6e684
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688645"
---
# <a name="imetadataimport2getmethodspecprops-method"></a><span data-ttu-id="e594c-103">IMetaDataImport2::GetMethodSpecProps 方法</span><span class="sxs-lookup"><span data-stu-id="e594c-103">IMetaDataImport2::GetMethodSpecProps Method</span></span>

<span data-ttu-id="e594c-104">获取指定的 MethodSpec 标记所引用的方法的元数据签名。</span><span class="sxs-lookup"><span data-stu-id="e594c-104">Gets the metadata signature of the method referenced by the specified MethodSpec token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e594c-105">语法</span><span class="sxs-lookup"><span data-stu-id="e594c-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMethodSpecProps (  
   [in]  mdMethodSpec     mi,  
   [out] mdToken          *tkParent,  
   [out] PCCOR_SIGNATURE  *ppvSigBlob,
   [out] ULONG            *pcbSigBlob  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="e594c-106">参数</span><span class="sxs-lookup"><span data-stu-id="e594c-106">Parameters</span></span>  

 `mi`  
 <span data-ttu-id="e594c-107">中一个 MethodSpec 标记，表示方法的实例化。</span><span class="sxs-lookup"><span data-stu-id="e594c-107">[in] A MethodSpec token that represents the instantiation of the method.</span></span>  
  
 `tkParent`  
 <span data-ttu-id="e594c-108">弄一个指针，指向表示方法定义的 MethodDef 或 MethodRef 标记。</span><span class="sxs-lookup"><span data-stu-id="e594c-108">[out] A pointer to the MethodDef or MethodRef token that represents the method definition.</span></span>  
  
 `ppvSigBlob`  
 <span data-ttu-id="e594c-109">弄指向方法的二进制元数据签名的指针。</span><span class="sxs-lookup"><span data-stu-id="e594c-109">[out] A pointer to the binary metadata signature of the method.</span></span>  
  
 `pcbSigBlob`  
 <span data-ttu-id="e594c-110">弄的大小（以字节为单位） `ppvSigBlob` 。</span><span class="sxs-lookup"><span data-stu-id="e594c-110">[out] The size, in bytes, of `ppvSigBlob`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e594c-111">要求</span><span class="sxs-lookup"><span data-stu-id="e594c-111">Requirements</span></span>  

 <span data-ttu-id="e594c-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e594c-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e594c-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="e594c-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e594c-114">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="e594c-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e594c-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e594c-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e594c-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="e594c-116">See also</span></span>

- [<span data-ttu-id="e594c-117">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="e594c-117">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
- [<span data-ttu-id="e594c-118">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="e594c-118">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
