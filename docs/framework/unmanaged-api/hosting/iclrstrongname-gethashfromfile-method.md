---
description: 了解详细信息： ICLRStrongName：： GetHashFromFile 方法
title: ICLRStrongName::GetHashFromFile 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromFile
helpviewer_keywords:
- ICLRStrongName::GetHashFromFile method [.NET Framework hosting]
- GetHashFromFile method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 9e50480a-8ada-4044-b2a5-97bb14ed3525
topic_type:
- apiref
ms.openlocfilehash: e930f1c21e5b0be441fe44ad352b2ef2f43d0f67
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637048"
---
# <a name="iclrstrongnamegethashfromfile-method"></a><span data-ttu-id="f0746-103">ICLRStrongName::GetHashFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="f0746-103">ICLRStrongName::GetHashFromFile Method</span></span>

<span data-ttu-id="f0746-104">生成指定文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="f0746-104">Generates a hash over the contents of the specified file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0746-105">语法</span><span class="sxs-lookup"><span data-stu-id="f0746-105">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromFile (  
    [in]  LPCSTR   szFilePath,  
    [in, out] unsigned int   *piHashAlg,
    [out] BYTE     *pbHash,
    [in]  DWORD    cchHash,
    [out] DWORD    *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f0746-106">参数</span><span class="sxs-lookup"><span data-stu-id="f0746-106">Parameters</span></span>  

 `szFilePath`  
 <span data-ttu-id="f0746-107">中要进行哈希处理的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="f0746-107">[in] The name of the file to hash.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="f0746-108">[in，out]生成哈希时要使用的算法。</span><span class="sxs-lookup"><span data-stu-id="f0746-108">[in, out] The algorithm to use when generating the hash.</span></span> <span data-ttu-id="f0746-109">有效算法是由 Win32 CryptoAPI 定义的算法。</span><span class="sxs-lookup"><span data-stu-id="f0746-109">Valid algorithms are those defined by the Win32 CryptoAPI.</span></span> <span data-ttu-id="f0746-110">如果 `piHashAlg` 设置为0，则使用默认算法 CALG_SHA-1。</span><span class="sxs-lookup"><span data-stu-id="f0746-110">If `piHashAlg` is set to 0, the default algorithm CALG_SHA-1 is used.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="f0746-111">弄一个字节数组，其中包含生成的哈希。</span><span class="sxs-lookup"><span data-stu-id="f0746-111">[out] A byte array containing the generated hash.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="f0746-112">中指向的缓冲区的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="f0746-112">[in] The maximum size of the buffer that `pbHash` points to.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="f0746-113">弄返回的的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="f0746-113">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f0746-114">返回值</span><span class="sxs-lookup"><span data-stu-id="f0746-114">Return Value</span></span>  

 <span data-ttu-id="f0746-115">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="f0746-115">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f0746-116">备注</span><span class="sxs-lookup"><span data-stu-id="f0746-116">Remarks</span></span>  

 <span data-ttu-id="f0746-117">此方法与 [ICLRStrongName：： GetHashFromFileW](iclrstrongname-gethashfromfilew-method.md) 方法相同，不同之处在于文件名规范为 ANSI 而不是 Unicode。</span><span class="sxs-lookup"><span data-stu-id="f0746-117">This method is the same as the [ICLRStrongName::GetHashFromFileW](iclrstrongname-gethashfromfilew-method.md) method, except that the file name specification is ANSI instead of Unicode.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0746-118">要求</span><span class="sxs-lookup"><span data-stu-id="f0746-118">Requirements</span></span>  

 <span data-ttu-id="f0746-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f0746-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0746-120">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="f0746-120">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="f0746-121">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f0746-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f0746-122">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0746-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0746-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="f0746-123">See also</span></span>

- [<span data-ttu-id="f0746-124">GetHashFromFileW 方法</span><span class="sxs-lookup"><span data-stu-id="f0746-124">GetHashFromFileW Method</span></span>](iclrstrongname-gethashfromfilew-method.md)
- [<span data-ttu-id="f0746-125">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="f0746-125">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
