---
description: 了解详细信息： ICLRStrongName：： StrongNameSignatureSize 方法
title: ICLRStrongName::StrongNameSignatureSize 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameSignatureSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameSignatureSize
helpviewer_keywords:
- ICLRStrongName::StrongNameSignatureSize method [.NET Framework hosting]
- StrongNameSignatureSize method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 76d4f93a-5e25-4399-abcc-a1389549481d
topic_type:
- apiref
ms.openlocfilehash: 4c3804eea5b7c6325519b19546f25585af649866
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781852"
---
# <a name="iclrstrongnamestrongnamesignaturesize-method"></a><span data-ttu-id="98714-103">ICLRStrongName::StrongNameSignatureSize 方法</span><span class="sxs-lookup"><span data-stu-id="98714-103">ICLRStrongName::StrongNameSignatureSize Method</span></span>

<span data-ttu-id="98714-104">返回强名称签名的大小。</span><span class="sxs-lookup"><span data-stu-id="98714-104">Returns the size of the strong name signature.</span></span> <span data-ttu-id="98714-105">此方法通常由编译器用来确定在创建延迟签名程序集时要在文件中保留多少空间。</span><span class="sxs-lookup"><span data-stu-id="98714-105">This method is typically used by compilers to determine how much space to reserve in the file when creating a delay-signed assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="98714-106">语法</span><span class="sxs-lookup"><span data-stu-id="98714-106">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameSignatureSize (
    [in]  BYTE   *pbPublicKeyBlob,  
    [in]  ULONG  cbPublicKeyBlob,
    [in]  DWORD  *pcbSize  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="98714-107">参数</span><span class="sxs-lookup"><span data-stu-id="98714-107">Parameters</span></span>  

 `pbPublicKeyBlob`  
 <span data-ttu-id="98714-108">中 [PublicKeyBlob](../strong-naming/publickeyblob-structure.md) 类型的结构，它包含用于生成强名称签名的密钥对的公共部分。</span><span class="sxs-lookup"><span data-stu-id="98714-108">[in] A structure of type [PublicKeyBlob](../strong-naming/publickeyblob-structure.md) that contains the public portion of the key pair used to generate the strong name signature.</span></span>  
  
 `cbPublicKeyBlob`  
 <span data-ttu-id="98714-109">中的大小（以字节为单位） `pbPublicKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="98714-109">[in] The size, in bytes, of `pbPublicKeyBlob`.</span></span>  
  
 `pcbSize`  
 <span data-ttu-id="98714-110">中存储强名称签名所需的字节数。</span><span class="sxs-lookup"><span data-stu-id="98714-110">[in] The number of bytes required to store the strong name signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="98714-111">返回值</span><span class="sxs-lookup"><span data-stu-id="98714-111">Return Value</span></span>  

 <span data-ttu-id="98714-112">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="98714-112">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="98714-113">要求</span><span class="sxs-lookup"><span data-stu-id="98714-113">Requirements</span></span>  

 <span data-ttu-id="98714-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="98714-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="98714-115">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="98714-115">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="98714-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="98714-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="98714-117">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="98714-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="98714-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="98714-118">See also</span></span>

- [<span data-ttu-id="98714-119">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="98714-119">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
