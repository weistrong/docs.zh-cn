---
description: 了解详细信息： GetHashFromFileW 函数
title: GetHashFromFileW 函数
ms.date: 03/30/2017
api_name:
- GetHashFromFileW
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromFileW
helpviewer_keywords:
- GetHashFromFileW function [.NET Framework strong naming]
ms.assetid: 97c2d7a6-5376-45a1-ba65-146a249147cc
topic_type:
- apiref
ms.openlocfilehash: daebd06de02dfe936f1bdeb8697de4fe6524dce3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736507"
---
# <a name="gethashfromfilew-function"></a><span data-ttu-id="cc09d-103">GetHashFromFileW 函数</span><span class="sxs-lookup"><span data-stu-id="cc09d-103">GetHashFromFileW Function</span></span>

<span data-ttu-id="cc09d-104">生成由 Unicode 字符串指定的文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="cc09d-104">Generates a hash over the contents of the file specified by a Unicode string.</span></span>  
  
 <span data-ttu-id="cc09d-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="cc09d-105">This function has been deprecated.</span></span> <span data-ttu-id="cc09d-106">改为使用 [ICLRStrongName：： GetHashFromFileW](../hosting/iclrstrongname-gethashfromfilew-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="cc09d-106">Use the [ICLRStrongName::GetHashFromFileW](../hosting/iclrstrongname-gethashfromfilew-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc09d-107">语法</span><span class="sxs-lookup"><span data-stu-id="cc09d-107">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromFileW (
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="cc09d-108">参数</span><span class="sxs-lookup"><span data-stu-id="cc09d-108">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="cc09d-109">中要进行哈希处理的文件的 Unicode 名称。</span><span class="sxs-lookup"><span data-stu-id="cc09d-109">[in] The Unicode name of the file to hash.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="cc09d-110">[in，out]生成哈希时要使用的算法。</span><span class="sxs-lookup"><span data-stu-id="cc09d-110">[in, out] The algorithm to use when generating the hash.</span></span> <span data-ttu-id="cc09d-111">有效算法是由 Win32 CryptoAPI 定义的算法。</span><span class="sxs-lookup"><span data-stu-id="cc09d-111">Valid algorithms are those defined by the Win32 CryptoAPI.</span></span> <span data-ttu-id="cc09d-112">如果 `piHashAlg` 设置为0，则使用默认算法 CALG_SHA-1。</span><span class="sxs-lookup"><span data-stu-id="cc09d-112">If `piHashAlg` is set to 0, the default algorithm CALG_SHA-1 is used.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="cc09d-113">弄一个字节数组，其中包含生成的哈希。</span><span class="sxs-lookup"><span data-stu-id="cc09d-113">[out] A byte array containing the generated hash.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="cc09d-114">中所指向的缓冲区的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="cc09d-114">[in] The maximum size of the buffer pointed to by `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="cc09d-115">弄的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="cc09d-115">[out] The size, in bytes, of `pbHash`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cc09d-116">备注</span><span class="sxs-lookup"><span data-stu-id="cc09d-116">Remarks</span></span>  

 <span data-ttu-id="cc09d-117">此函数与 [GetHashFromFile](gethashfromfile-function.md)相同，不同之处在于文件名规范是 Unicode 而不是 ANSI。</span><span class="sxs-lookup"><span data-stu-id="cc09d-117">This function is the same as [GetHashFromFile](gethashfromfile-function.md), except that the file name specification is Unicode instead of ANSI.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc09d-118">要求</span><span class="sxs-lookup"><span data-stu-id="cc09d-118">Requirements</span></span>  

 <span data-ttu-id="cc09d-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cc09d-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc09d-120">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="cc09d-120">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="cc09d-121">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cc09d-121">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="cc09d-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cc09d-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc09d-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="cc09d-123">See also</span></span>

- [<span data-ttu-id="cc09d-124">GetHashFromFileW 方法</span><span class="sxs-lookup"><span data-stu-id="cc09d-124">GetHashFromFileW Method</span></span>](../hosting/iclrstrongname-gethashfromfilew-method.md)
- [<span data-ttu-id="cc09d-125">GetHashFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="cc09d-125">GetHashFromFile Method</span></span>](../hosting/iclrstrongname-gethashfromfile-method.md)
- [<span data-ttu-id="cc09d-126">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="cc09d-126">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
