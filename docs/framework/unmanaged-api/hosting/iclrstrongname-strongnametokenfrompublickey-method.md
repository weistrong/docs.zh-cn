---
description: 了解详细信息： ICLRStrongName：： StrongNameTokenFromPublicKey 方法
title: ICLRStrongName::StrongNameTokenFromPublicKey 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameTokenFromPublicKey
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameTokenFromPublicKey
helpviewer_keywords:
- ICLRStrongName::StrongNameTokenFromPublicKey method [.NET Framework hosting]
- StrongNameTokenFromPublicKey method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 7962ce88-7e86-4a6f-8298-621b01ffc3c2
topic_type:
- apiref
ms.openlocfilehash: de245b151e5ca016a00793a8901c0fd990a3f804
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789738"
---
# <a name="iclrstrongnamestrongnametokenfrompublickey-method"></a><span data-ttu-id="2d8b4-103">ICLRStrongName::StrongNameTokenFromPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="2d8b4-103">ICLRStrongName::StrongNameTokenFromPublicKey Method</span></span>

<span data-ttu-id="2d8b4-104">获取表示公钥的标记。</span><span class="sxs-lookup"><span data-stu-id="2d8b4-104">Gets a token that represents a public key.</span></span> <span data-ttu-id="2d8b4-105">强名称标记是公钥的缩写形式。</span><span class="sxs-lookup"><span data-stu-id="2d8b4-105">A strong name token is the shortened form of a public key.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d8b4-106">语法</span><span class="sxs-lookup"><span data-stu-id="2d8b4-106">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameTokenFromPublicKey (
    [in]  BYTE    *pbPublicKeyBlob,  
    [in]  ULONG   cbPublicKeyBlob,  
    [out] BYTE    **ppbStrongNameToken,  
    [out] ULONG   *pcbStrongNameToken  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2d8b4-107">参数</span><span class="sxs-lookup"><span data-stu-id="2d8b4-107">Parameters</span></span>  

 `pbPublicKeyBlob`  
 <span data-ttu-id="2d8b4-108">中 [PublicKeyBlob](../strong-naming/publickeyblob-structure.md) 类型的结构，它包含用于生成强名称签名的密钥对的公共部分。</span><span class="sxs-lookup"><span data-stu-id="2d8b4-108">[in] A structure of type [PublicKeyBlob](../strong-naming/publickeyblob-structure.md) that contains the public portion of the key pair used to generate the strong name signature.</span></span>  
  
 `cbPublicKeyBlob`  
 <span data-ttu-id="2d8b4-109">中的大小（以字节为单位） `pbPublicKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="2d8b4-109">[in] The size, in bytes, of `pbPublicKeyBlob`.</span></span>  
  
 `ppbStrongNameToken`  
 <span data-ttu-id="2d8b4-110">弄与传入的密钥对应的强名称标记 `pbPublicKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="2d8b4-110">[out] The strong name token corresponding to the key passed in `pbPublicKeyBlob`.</span></span> <span data-ttu-id="2d8b4-111">公共语言运行时分配要在其中返回标记的内存。</span><span class="sxs-lookup"><span data-stu-id="2d8b4-111">The common language runtime allocates the memory in which to return the token.</span></span> <span data-ttu-id="2d8b4-112">调用方必须通过使用 [ICLRStrongName：： StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) 方法释放此内存。</span><span class="sxs-lookup"><span data-stu-id="2d8b4-112">The caller must free this memory by using the [ICLRStrongName::StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) method.</span></span>  
  
 `pcbStrongNameToken`  
 <span data-ttu-id="2d8b4-113">弄返回的强名称标记的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="2d8b4-113">[out] The size, in bytes, of the returned strong name token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2d8b4-114">返回值</span><span class="sxs-lookup"><span data-stu-id="2d8b4-114">Return Value</span></span>  

 <span data-ttu-id="2d8b4-115">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="2d8b4-115">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2d8b4-116">备注</span><span class="sxs-lookup"><span data-stu-id="2d8b4-116">Remarks</span></span>  

 <span data-ttu-id="2d8b4-117">强名称标记是用于在元数据中存储密钥信息时节省空间的公钥的缩写形式。</span><span class="sxs-lookup"><span data-stu-id="2d8b4-117">A strong name token is the shortened form of a public key that is used to save space when storing key information in metadata.</span></span> <span data-ttu-id="2d8b4-118">具体而言，强名称令牌在程序集引用中用于引用依赖程序集。</span><span class="sxs-lookup"><span data-stu-id="2d8b4-118">Specifically, strong name tokens are used in assembly references to refer to the dependent assembly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d8b4-119">要求</span><span class="sxs-lookup"><span data-stu-id="2d8b4-119">Requirements</span></span>  

 <span data-ttu-id="2d8b4-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2d8b4-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d8b4-121">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="2d8b4-121">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="2d8b4-122">**库：** 作为中的资源包含 mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="2d8b4-122">**Library:** Included as a resource in mscoree.dll</span></span>  
  
 <span data-ttu-id="2d8b4-123">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d8b4-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d8b4-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="2d8b4-124">See also</span></span>

- [<span data-ttu-id="2d8b4-125">StrongNameGetPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="2d8b4-125">StrongNameGetPublicKey Method</span></span>](iclrstrongname-strongnamegetpublickey-method.md)
- [<span data-ttu-id="2d8b4-126">PublicKeyBlob 结构</span><span class="sxs-lookup"><span data-stu-id="2d8b4-126">PublicKeyBlob Structure</span></span>](../strong-naming/publickeyblob-structure.md)
- [<span data-ttu-id="2d8b4-127">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="2d8b4-127">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
