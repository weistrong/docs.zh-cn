---
description: 了解详细信息： IMetaDataImport：： GetSigFromToken 方法
title: IMetaDataImport::GetSigFromToken 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetSigFromToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetSigFromToken
helpviewer_keywords:
- IMetaDataImport::GetSigFromToken method [.NET Framework metadata]
- GetSigFromToken method [.NET Framework metadata]
ms.assetid: ab894dc4-f7b6-4afc-bfcb-582a4b7e53a2
topic_type:
- apiref
ms.openlocfilehash: 16b77fe5866319e24b33ec4ce9d2d56797f04514
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789133"
---
# <a name="imetadataimportgetsigfromtoken-method"></a><span data-ttu-id="3fbdd-103">IMetaDataImport::GetSigFromToken 方法</span><span class="sxs-lookup"><span data-stu-id="3fbdd-103">IMetaDataImport::GetSigFromToken Method</span></span>

<span data-ttu-id="3fbdd-104">获取与指定标记关联的二进制元数据签名。</span><span class="sxs-lookup"><span data-stu-id="3fbdd-104">Gets the binary metadata signature associated with the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3fbdd-105">语法</span><span class="sxs-lookup"><span data-stu-id="3fbdd-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSigFromToken (
   [in]   mdSignature        mdSig,
   [out]  PCCOR_SIGNATURE    *ppvSig,
   [out]  ULONG              *pcbSig
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3fbdd-106">参数</span><span class="sxs-lookup"><span data-stu-id="3fbdd-106">Parameters</span></span>  

 `mdSig`  
 <span data-ttu-id="3fbdd-107">中要为其返回二进制元数据签名的标记。</span><span class="sxs-lookup"><span data-stu-id="3fbdd-107">[in] The token to return the binary metadata signature for.</span></span>  
  
 `ppvSig`  
 <span data-ttu-id="3fbdd-108">弄指向返回的元数据签名的指针。</span><span class="sxs-lookup"><span data-stu-id="3fbdd-108">[out] A pointer to the returned metadata signature.</span></span>  
  
 `pcbSig`  
 <span data-ttu-id="3fbdd-109">弄二进制元数据签名的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="3fbdd-109">[out] The size in bytes of the binary metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3fbdd-110">要求</span><span class="sxs-lookup"><span data-stu-id="3fbdd-110">Requirements</span></span>  

 <span data-ttu-id="3fbdd-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3fbdd-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3fbdd-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="3fbdd-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3fbdd-113">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3fbdd-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3fbdd-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3fbdd-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3fbdd-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="3fbdd-115">See also</span></span>

- [<span data-ttu-id="3fbdd-116">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="3fbdd-116">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="3fbdd-117">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="3fbdd-117">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
