---
description: 了解详细信息： GetHashFromFile 函数
title: GetHashFromFile 函数
ms.date: 03/30/2017
api_name:
- GetHashFromFile
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromFile
helpviewer_keywords:
- GetHashFromFile function [.NET Framework strong naming]
ms.assetid: b3c526a4-8fb4-4ad6-b6af-42ce9c06492e
topic_type:
- apiref
ms.openlocfilehash: f91bfe8a3988b6aae563b5a852997d6fd3c309d6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736591"
---
# <a name="gethashfromfile-function"></a><span data-ttu-id="654e8-103">GetHashFromFile 函数</span><span class="sxs-lookup"><span data-stu-id="654e8-103">GetHashFromFile Function</span></span>

<span data-ttu-id="654e8-104">生成指定文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="654e8-104">Generates a hash over the contents of the specified file.</span></span>  
  
 <span data-ttu-id="654e8-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="654e8-105">This function has been deprecated.</span></span> <span data-ttu-id="654e8-106">改为使用 [ICLRStrongName：： GetHashFromFile](../hosting/iclrstrongname-gethashfromfile-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="654e8-106">Use the [ICLRStrongName::GetHashFromFile](../hosting/iclrstrongname-gethashfromfile-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="654e8-107">语法</span><span class="sxs-lookup"><span data-stu-id="654e8-107">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromFile (  
    [in]  LPCSTR   szFilePath,  
    [in, out] unsigned int   *piHashAlg,
    [out] BYTE     *pbHash,
    [in]  DWORD    cchHash,
    [out] DWORD    *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="654e8-108">参数</span><span class="sxs-lookup"><span data-stu-id="654e8-108">Parameters</span></span>  

 `szFilePath`  
 <span data-ttu-id="654e8-109">中要进行哈希处理的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="654e8-109">[in] The name of the file to hash.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="654e8-110">[in，out]生成哈希时要使用的算法。</span><span class="sxs-lookup"><span data-stu-id="654e8-110">[in, out] The algorithm to use when generating the hash.</span></span> <span data-ttu-id="654e8-111">有效算法是由 Win32 CryptoAPI 定义的算法。</span><span class="sxs-lookup"><span data-stu-id="654e8-111">Valid algorithms are those defined by the Win32 CryptoAPI.</span></span> <span data-ttu-id="654e8-112">如果 `piHashAlg` 设置为0，则使用默认算法 CALG_SHA-1。</span><span class="sxs-lookup"><span data-stu-id="654e8-112">If `piHashAlg` is set to 0, the default algorithm CALG_SHA-1 is used.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="654e8-113">弄一个字节数组，其中包含生成的哈希。</span><span class="sxs-lookup"><span data-stu-id="654e8-113">[out] A byte array containing the generated hash.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="654e8-114">中指向的缓冲区的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="654e8-114">[in] The maximum size of the buffer that `pbHash` points to.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="654e8-115">弄返回的的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="654e8-115">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="654e8-116">备注</span><span class="sxs-lookup"><span data-stu-id="654e8-116">Remarks</span></span>  

 <span data-ttu-id="654e8-117">此函数与 [GetHashFromFileW](gethashfromfilew-function.md)相同，不同之处在于文件名规范为 ANSI 而不是 Unicode。</span><span class="sxs-lookup"><span data-stu-id="654e8-117">This function is the same as [GetHashFromFileW](gethashfromfilew-function.md), except that the file name specification is ANSI instead of Unicode.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="654e8-118">要求</span><span class="sxs-lookup"><span data-stu-id="654e8-118">Requirements</span></span>  

 <span data-ttu-id="654e8-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="654e8-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="654e8-120">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="654e8-120">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="654e8-121">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="654e8-121">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="654e8-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="654e8-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="654e8-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="654e8-123">See also</span></span>

- [<span data-ttu-id="654e8-124">GetHashFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="654e8-124">GetHashFromFile Method</span></span>](../hosting/iclrstrongname-gethashfromfile-method.md)
- [<span data-ttu-id="654e8-125">GetHashFromFileW 方法</span><span class="sxs-lookup"><span data-stu-id="654e8-125">GetHashFromFileW Method</span></span>](../hosting/iclrstrongname-gethashfromfilew-method.md)
- [<span data-ttu-id="654e8-126">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="654e8-126">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
