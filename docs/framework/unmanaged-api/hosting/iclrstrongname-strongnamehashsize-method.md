---
description: 了解详细信息： ICLRStrongName：： StrongNameHashSize 方法
title: ICLRStrongName::StrongNameHashSize 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameHashSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameHashSize
helpviewer_keywords:
- ICLRStrongName::StrongNameHashSize method [.NET Framework hosting]
- StrongNameHashSize method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 4a05ee56-08e4-4f3a-86a9-9b52083d5c0f
topic_type:
- apiref
ms.openlocfilehash: 74781f0eaec720a84a242e6a9637036408652601
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799585"
---
# <a name="iclrstrongnamestrongnamehashsize-method"></a><span data-ttu-id="01718-103">ICLRStrongName::StrongNameHashSize 方法</span><span class="sxs-lookup"><span data-stu-id="01718-103">ICLRStrongName::StrongNameHashSize Method</span></span>

<span data-ttu-id="01718-104">使用指定的哈希算法获取哈希所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="01718-104">Gets the buffer size required for a hash, using the specified hash algorithm.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="01718-105">语法</span><span class="sxs-lookup"><span data-stu-id="01718-105">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameHashSize (  
    [in]  ULONG   ulHashAlg,  
    [out] DWORD   *pcbSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="01718-106">参数</span><span class="sxs-lookup"><span data-stu-id="01718-106">Parameters</span></span>  

 `ulHashAlg`  
 <span data-ttu-id="01718-107">中用于计算缓冲区大小的哈希算法。</span><span class="sxs-lookup"><span data-stu-id="01718-107">[in] The hash algorithm used to compute the buffer size.</span></span>  
  
 `pcbSize`  
 <span data-ttu-id="01718-108">弄返回的缓冲区大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="01718-108">[out] The returned buffer size, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="01718-109">返回值</span><span class="sxs-lookup"><span data-stu-id="01718-109">Return Value</span></span>  

 <span data-ttu-id="01718-110">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="01718-110">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="01718-111">要求</span><span class="sxs-lookup"><span data-stu-id="01718-111">Requirements</span></span>  

 <span data-ttu-id="01718-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="01718-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="01718-113">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="01718-113">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="01718-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="01718-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="01718-115">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="01718-115">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01718-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="01718-116">See also</span></span>

- [<span data-ttu-id="01718-117">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="01718-117">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
