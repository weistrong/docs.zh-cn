---
description: 了解详细信息： ICLRStrongName：： GetHashFromFileW 方法
title: ICLRStrongName::GetHashFromFileW 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromFileW
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromFileW
helpviewer_keywords:
- GetHashFromFileW method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::GetHashFromFileW method [.NET Framework hosting]
ms.assetid: c6ff45fc-905d-4c6e-b00c-97c6c7c55d99
topic_type:
- apiref
ms.openlocfilehash: 6145a044f490ef3827de6db8d84d16222306642d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636970"
---
# <a name="iclrstrongnamegethashfromfilew-method"></a><span data-ttu-id="50460-103">ICLRStrongName::GetHashFromFileW 方法</span><span class="sxs-lookup"><span data-stu-id="50460-103">ICLRStrongName::GetHashFromFileW Method</span></span>

<span data-ttu-id="50460-104">生成由 Unicode 字符串指定的文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="50460-104">Generates a hash over the contents of the file specified by a Unicode string.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50460-105">语法</span><span class="sxs-lookup"><span data-stu-id="50460-105">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromFileW (
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="50460-106">参数</span><span class="sxs-lookup"><span data-stu-id="50460-106">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="50460-107">中要进行哈希处理的文件的 Unicode 名称。</span><span class="sxs-lookup"><span data-stu-id="50460-107">[in] The Unicode name of the file to hash.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="50460-108">[in，out]生成哈希时要使用的算法。</span><span class="sxs-lookup"><span data-stu-id="50460-108">[in, out] The algorithm to use when generating the hash.</span></span> <span data-ttu-id="50460-109">有效算法是由 Win32 CryptoAPI 定义的算法。</span><span class="sxs-lookup"><span data-stu-id="50460-109">Valid algorithms are those defined by the Win32 CryptoAPI.</span></span> <span data-ttu-id="50460-110">如果 `piHashAlg` 设置为0，则使用默认算法 CALG_SHA-1。</span><span class="sxs-lookup"><span data-stu-id="50460-110">If `piHashAlg` is set to 0, the default algorithm CALG_SHA-1 is used.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="50460-111">弄一个字节数组，其中包含生成的哈希。</span><span class="sxs-lookup"><span data-stu-id="50460-111">[out] A byte array containing the generated hash.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="50460-112">中所指向的缓冲区的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="50460-112">[in] The maximum size of the buffer pointed to by `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="50460-113">弄的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="50460-113">[out] The size, in bytes, of `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="50460-114">返回值</span><span class="sxs-lookup"><span data-stu-id="50460-114">Return Value</span></span>  

 <span data-ttu-id="50460-115">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="50460-115">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="50460-116">备注</span><span class="sxs-lookup"><span data-stu-id="50460-116">Remarks</span></span>  

 <span data-ttu-id="50460-117">此方法与 [ICLRStrongName：： GetHashFromFile](iclrstrongname-gethashfromfile-method.md) 方法相同，不同之处在于文件名规范是 Unicode 而不是 ANSI。</span><span class="sxs-lookup"><span data-stu-id="50460-117">This method is the same as the [ICLRStrongName::GetHashFromFile](iclrstrongname-gethashfromfile-method.md) method, except that the file name specification is Unicode instead of ANSI.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="50460-118">要求</span><span class="sxs-lookup"><span data-stu-id="50460-118">Requirements</span></span>  

 <span data-ttu-id="50460-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="50460-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="50460-120">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="50460-120">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="50460-121">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="50460-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="50460-122">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="50460-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50460-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="50460-123">See also</span></span>

- [<span data-ttu-id="50460-124">GetHashFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="50460-124">GetHashFromFile Method</span></span>](iclrstrongname-gethashfromfile-method.md)
- [<span data-ttu-id="50460-125">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="50460-125">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
