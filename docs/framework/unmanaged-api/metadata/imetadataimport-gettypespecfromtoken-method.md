---
description: 了解详细信息： IMetaDataImport：： GetTypeSpecFromToken 方法
title: IMetaDataImport::GetTypeSpecFromToken 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetTypeSpecFromToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetTypeSpecFromToken
helpviewer_keywords:
- GetTypeSpecFromToken method [.NET Framework metadata]
- IMetaDataImport::GetTypeSpecFromToken method [.NET Framework metadata]
ms.assetid: ee518bda-3296-482e-a7b7-e9d51dd1a181
topic_type:
- apiref
ms.openlocfilehash: b71f8f856da517b3e5046c20d787a555816fb728
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789107"
---
# <a name="imetadataimportgettypespecfromtoken-method"></a><span data-ttu-id="748f1-103">IMetaDataImport::GetTypeSpecFromToken 方法</span><span class="sxs-lookup"><span data-stu-id="748f1-103">IMetaDataImport::GetTypeSpecFromToken Method</span></span>

<span data-ttu-id="748f1-104">获取指定标记所表示的类型规范的二进制元数据签名。</span><span class="sxs-lookup"><span data-stu-id="748f1-104">Gets the binary metadata signature of the type specification represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="748f1-105">语法</span><span class="sxs-lookup"><span data-stu-id="748f1-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTypeSpecFromToken (
   [in]  mdTypeSpec            typespec,
   [out] PCCOR_SIGNATURE       *ppvSig,
   [out] ULONG                 *pcbSig  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="748f1-106">参数</span><span class="sxs-lookup"><span data-stu-id="748f1-106">Parameters</span></span>  

 `typespec`  
 <span data-ttu-id="748f1-107">中与请求的元数据签名关联的 TypeSpec 标记。</span><span class="sxs-lookup"><span data-stu-id="748f1-107">[in] The TypeSpec token associated with the requested metadata signature.</span></span>  
  
 `ppvSig`  
 <span data-ttu-id="748f1-108">弄指向二进制元数据签名的指针。</span><span class="sxs-lookup"><span data-stu-id="748f1-108">[out] A pointer to the binary metadata signature.</span></span>  
  
 `pcbSig`  
 <span data-ttu-id="748f1-109">弄元数据签名的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="748f1-109">[out] The size, in bytes, of the metadata signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="748f1-110">返回值</span><span class="sxs-lookup"><span data-stu-id="748f1-110">Return Value</span></span>  

 <span data-ttu-id="748f1-111">一个指示成功或失败的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="748f1-111">An HRESULT that indicates success or failure.</span></span> <span data-ttu-id="748f1-112">可以通过失败的宏测试失败。</span><span class="sxs-lookup"><span data-stu-id="748f1-112">Failures can be tested with the FAILED macro.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="748f1-113">要求</span><span class="sxs-lookup"><span data-stu-id="748f1-113">Requirements</span></span>  

 <span data-ttu-id="748f1-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="748f1-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="748f1-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="748f1-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="748f1-116">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="748f1-116">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="748f1-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="748f1-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="748f1-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="748f1-118">See also</span></span>

- [<span data-ttu-id="748f1-119">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="748f1-119">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="748f1-120">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="748f1-120">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
