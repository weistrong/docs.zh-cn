---
description: 了解详细信息： ICLRStrongName：： StrongNameKeyInstall 方法
title: ICLRStrongName::StrongNameKeyInstall 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameKeyInstall
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameKeyInstall
helpviewer_keywords:
- ICLRStrongName::StrongNameKeyInstall method [.NET Framework hosting]
- StrongNameKeyInstall method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 5c15cf3b-164c-49d1-8e57-e42949d55acf
topic_type:
- apiref
ms.openlocfilehash: 8f9e7bfebff555a6430a3970c8ee1c481e341f58
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799507"
---
# <a name="iclrstrongnamestrongnamekeyinstall-method"></a><span data-ttu-id="c359f-103">ICLRStrongName::StrongNameKeyInstall 方法</span><span class="sxs-lookup"><span data-stu-id="c359f-103">ICLRStrongName::StrongNameKeyInstall Method</span></span>

<span data-ttu-id="c359f-104">将公钥/私钥对导入容器。</span><span class="sxs-lookup"><span data-stu-id="c359f-104">Imports a public/private key pair into a container.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c359f-105">语法</span><span class="sxs-lookup"><span data-stu-id="c359f-105">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameKeyInstall (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c359f-106">参数</span><span class="sxs-lookup"><span data-stu-id="c359f-106">Parameters</span></span>  

 `wszKeyContainer`  
 <span data-ttu-id="c359f-107">中密钥容器的名称。</span><span class="sxs-lookup"><span data-stu-id="c359f-107">[in] The name of the key container.</span></span> <span data-ttu-id="c359f-108">`wszKeyContainer` 必须为非空字符串。</span><span class="sxs-lookup"><span data-stu-id="c359f-108">`wszKeyContainer` must be a non-empty string.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="c359f-109">中二进制密钥对。</span><span class="sxs-lookup"><span data-stu-id="c359f-109">[in] The binary key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="c359f-110">中的大小（以字节为单位） `pbKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="c359f-110">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c359f-111">返回值</span><span class="sxs-lookup"><span data-stu-id="c359f-111">Return Value</span></span>  

 <span data-ttu-id="c359f-112">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="c359f-112">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c359f-113">备注</span><span class="sxs-lookup"><span data-stu-id="c359f-113">Remarks</span></span>  

 <span data-ttu-id="c359f-114">使用 [ICLRStrongName：： StrongNameKeyDelete](iclrstrongname-strongnamekeydelete-method.md) 方法删除密钥容器。</span><span class="sxs-lookup"><span data-stu-id="c359f-114">Use the [ICLRStrongName::StrongNameKeyDelete](iclrstrongname-strongnamekeydelete-method.md) method to delete the key container.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c359f-115">要求</span><span class="sxs-lookup"><span data-stu-id="c359f-115">Requirements</span></span>  

 <span data-ttu-id="c359f-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c359f-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c359f-117">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="c359f-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="c359f-118">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c359f-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c359f-119">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c359f-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c359f-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="c359f-120">See also</span></span>

- [<span data-ttu-id="c359f-121">StrongNameKeyDelete 方法</span><span class="sxs-lookup"><span data-stu-id="c359f-121">StrongNameKeyDelete Method</span></span>](iclrstrongname-strongnamekeydelete-method.md)
- [<span data-ttu-id="c359f-122">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="c359f-122">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
