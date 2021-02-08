---
description: 了解详细信息： ICLRStrongName：： GetHashFromHandle 方法
title: ICLRStrongName::GetHashFromHandle 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromHandle
- ICLRStrongName.StrongNameCompareAssemblies
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromHandle
helpviewer_keywords:
- GetHashFromHandle method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::GetHashFromHandle method [.NET Framework hosting]
ms.assetid: 3bedbb7d-3cdd-4175-b370-10ae734062db
topic_type:
- apiref
ms.openlocfilehash: 30248b5cb5d102adaa06293c92cc4f21e905cba5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799676"
---
# <a name="iclrstrongnamegethashfromhandle-method"></a><span data-ttu-id="e4c36-103">ICLRStrongName::GetHashFromHandle 方法</span><span class="sxs-lookup"><span data-stu-id="e4c36-103">ICLRStrongName::GetHashFromHandle Method</span></span>

<span data-ttu-id="e4c36-104">使用指定的哈希算法，通过具有指定的文件句柄的文件的内容生成哈希。</span><span class="sxs-lookup"><span data-stu-id="e4c36-104">Generates a hash over the contents of the file that has the specified file handle, using the specified hash algorithm.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4c36-105">语法</span><span class="sxs-lookup"><span data-stu-id="e4c36-105">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromHandle (  
    [in]  HANDLE   hFile,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e4c36-106">参数</span><span class="sxs-lookup"><span data-stu-id="e4c36-106">Parameters</span></span>  

 `hFile`  
 <span data-ttu-id="e4c36-107">中要进行哈希处理的文件的句柄。</span><span class="sxs-lookup"><span data-stu-id="e4c36-107">[in] The handle of the file to be hashed.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="e4c36-108">[in，out]指定哈希算法的常量。</span><span class="sxs-lookup"><span data-stu-id="e4c36-108">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="e4c36-109">对于默认算法，使用零。</span><span class="sxs-lookup"><span data-stu-id="e4c36-109">Use zero for the default algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="e4c36-110">弄返回的哈希缓冲区。</span><span class="sxs-lookup"><span data-stu-id="e4c36-110">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="e4c36-111">中请求的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="e4c36-111">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="e4c36-112">弄返回的的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="e4c36-112">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e4c36-113">返回值</span><span class="sxs-lookup"><span data-stu-id="e4c36-113">Return Value</span></span>  

 <span data-ttu-id="e4c36-114">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="e4c36-114">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4c36-115">要求</span><span class="sxs-lookup"><span data-stu-id="e4c36-115">Requirements</span></span>  

 <span data-ttu-id="e4c36-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e4c36-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4c36-117">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="e4c36-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="e4c36-118">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e4c36-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e4c36-119">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4c36-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4c36-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e4c36-120">See also</span></span>

- [<span data-ttu-id="e4c36-121">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="e4c36-121">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
