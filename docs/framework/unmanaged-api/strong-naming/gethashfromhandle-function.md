---
description: 了解详细信息： GetHashFromHandle 函数
title: GetHashFromHandle 函数
ms.date: 03/30/2017
api_name:
- GetHashFromHandle
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromHandle
helpviewer_keywords:
- GetHashFromHandle function [.NET Framework strong naming]
ms.assetid: 9e00337f-b307-4602-9bc3-965a8dbf02cd
topic_type:
- apiref
ms.openlocfilehash: 5951a5befd9e66b13a3b3033398614fca1f1a9d8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736484"
---
# <a name="gethashfromhandle-function"></a><span data-ttu-id="aed06-103">GetHashFromHandle 函数</span><span class="sxs-lookup"><span data-stu-id="aed06-103">GetHashFromHandle Function</span></span>

<span data-ttu-id="aed06-104">使用指定的哈希算法，生成具有指定文件句柄的文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="aed06-104">Generates a hash over the contents of the file with the specified file handle, using the specified hash algorithm.</span></span>  
  
 <span data-ttu-id="aed06-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="aed06-105">This function has been deprecated.</span></span> <span data-ttu-id="aed06-106">改为使用 [ICLRStrongName：： GetHashFromHandle](../hosting/iclrstrongname-gethashfromhandle-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="aed06-106">Use the [ICLRStrongName::GetHashFromHandle](../hosting/iclrstrongname-gethashfromhandle-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aed06-107">语法</span><span class="sxs-lookup"><span data-stu-id="aed06-107">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromHandle (  
    [in]  HANDLE   hFile,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="aed06-108">参数</span><span class="sxs-lookup"><span data-stu-id="aed06-108">Parameters</span></span>  

 `hFile`  
 <span data-ttu-id="aed06-109">中要进行哈希处理的文件的句柄。</span><span class="sxs-lookup"><span data-stu-id="aed06-109">[in] The handle of the file to be hashed.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="aed06-110">[in，out]指定哈希算法的常量。</span><span class="sxs-lookup"><span data-stu-id="aed06-110">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="aed06-111">对于默认算法，使用零。</span><span class="sxs-lookup"><span data-stu-id="aed06-111">Use zero for the default algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="aed06-112">弄返回的哈希缓冲区。</span><span class="sxs-lookup"><span data-stu-id="aed06-112">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="aed06-113">中请求的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="aed06-113">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="aed06-114">弄返回的的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="aed06-114">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aed06-115">要求</span><span class="sxs-lookup"><span data-stu-id="aed06-115">Requirements</span></span>  

 <span data-ttu-id="aed06-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="aed06-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aed06-117">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="aed06-117">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="aed06-118">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="aed06-118">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="aed06-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aed06-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aed06-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="aed06-120">See also</span></span>

- [<span data-ttu-id="aed06-121">GetHashFromHandle 方法</span><span class="sxs-lookup"><span data-stu-id="aed06-121">GetHashFromHandle Method</span></span>](../hosting/iclrstrongname-gethashfromhandle-method.md)
- [<span data-ttu-id="aed06-122">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="aed06-122">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
