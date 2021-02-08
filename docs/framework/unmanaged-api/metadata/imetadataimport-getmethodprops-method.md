---
description: 了解详细信息： IMetaDataImport：： GetMethodProps 方法
title: IMetaDataImport::GetMethodProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetMethodProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMethodProps
helpviewer_keywords:
- GetMethodProps method [.NET Framework metadata]
- IMetaDataImport::GetMethodProps method [.NET Framework metadata]
ms.assetid: e0667ef7-1d31-4c89-a2d3-d426f023f8d2
topic_type:
- apiref
ms.openlocfilehash: 5fb344d72378a806e0e71820b55a90998e497916
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783869"
---
# <a name="imetadataimportgetmethodprops-method"></a><span data-ttu-id="fac3f-103">IMetaDataImport::GetMethodProps 方法</span><span class="sxs-lookup"><span data-stu-id="fac3f-103">IMetaDataImport::GetMethodProps Method</span></span>

<span data-ttu-id="fac3f-104">获取与指定的 MethodDef 标记引用的方法关联的元数据。</span><span class="sxs-lookup"><span data-stu-id="fac3f-104">Gets the metadata associated with the method referenced by the specified MethodDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fac3f-105">语法</span><span class="sxs-lookup"><span data-stu-id="fac3f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMethodProps (  
    [in]  mdMethodDef         mb,  
    [out] mdTypeDef           *pClass,  
    [out] LPWSTR              szMethod,  
    [in]  ULONG               cchMethod,  
    [out] ULONG               *pchMethod,  
    [out] DWORD               *pdwAttr,  
    [out] PCCOR_SIGNATURE     *ppvSigBlob,  
    [out] ULONG               *pcbSigBlob,  
    [out] ULONG               *pulCodeRVA,  
    [out] DWORD               *pdwImplFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fac3f-106">参数</span><span class="sxs-lookup"><span data-stu-id="fac3f-106">Parameters</span></span>  

 `mb`  
 <span data-ttu-id="fac3f-107">中MethodDef 标记，它表示要为其返回元数据的方法。</span><span class="sxs-lookup"><span data-stu-id="fac3f-107">[in] The MethodDef token that represents the method to return metadata for.</span></span>  
  
 `pClass`  
 <span data-ttu-id="fac3f-108">弄一个指针，指向表示实现方法的类型的 TypeDef 标记。</span><span class="sxs-lookup"><span data-stu-id="fac3f-108">[out] A Pointer to a TypeDef token that represents the type that implements the method.</span></span>  
  
 `szMethod`  
 <span data-ttu-id="fac3f-109">弄指向包含方法名称的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="fac3f-109">[out] A Pointer to a buffer that has the method's name.</span></span>  
  
 `cchMethod`  
 <span data-ttu-id="fac3f-110">中请求的大小 `szMethod` 。</span><span class="sxs-lookup"><span data-stu-id="fac3f-110">[in] The requested size of `szMethod`.</span></span>  
  
 `pchMethod`  
 <span data-ttu-id="fac3f-111">弄一个指针，它指向 `szMethod` 方法名称中实际的宽字符数（以宽字符为范围），或在截断的情况下为。</span><span class="sxs-lookup"><span data-stu-id="fac3f-111">[out] A Pointer to the size in wide characters of `szMethod`, or in the case of truncation, the actual number of wide characters in the method name.</span></span>  
  
 `pdwAttr`  
 <span data-ttu-id="fac3f-112">弄一个指针，指向与方法关联的任何标志。</span><span class="sxs-lookup"><span data-stu-id="fac3f-112">[out] A pointer to any flags associated with the method.</span></span>  
  
 `ppvSigBlob`  
 <span data-ttu-id="fac3f-113">弄指向方法的二进制元数据签名的指针。</span><span class="sxs-lookup"><span data-stu-id="fac3f-113">[out] A pointer to the binary metadata signature of the method.</span></span>  
  
 `pcbSigBlob`  
 <span data-ttu-id="fac3f-114">弄一个指针，它指向的大小（以字节为单位） `ppvSigBlob` 。</span><span class="sxs-lookup"><span data-stu-id="fac3f-114">[out] A Pointer to the size in bytes of `ppvSigBlob`.</span></span>  
  
 `pulCodeRVA`  
 <span data-ttu-id="fac3f-115">弄指向方法的相对虚拟地址的指针。</span><span class="sxs-lookup"><span data-stu-id="fac3f-115">[out] A pointer to the relative virtual address of the method.</span></span>  
  
 `pdwImplFlags`  
 <span data-ttu-id="fac3f-116">弄一个指针，指向方法的任何实现标志。</span><span class="sxs-lookup"><span data-stu-id="fac3f-116">[out] A pointer to any implementation flags for the method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fac3f-117">要求</span><span class="sxs-lookup"><span data-stu-id="fac3f-117">Requirements</span></span>  

 <span data-ttu-id="fac3f-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fac3f-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fac3f-119">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="fac3f-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="fac3f-120">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fac3f-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="fac3f-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fac3f-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fac3f-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="fac3f-122">See also</span></span>

- [<span data-ttu-id="fac3f-123">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="fac3f-123">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="fac3f-124">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="fac3f-124">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
