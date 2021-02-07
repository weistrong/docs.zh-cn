---
description: 了解详细信息： GetHashFromAssemblyFileW 函数
title: GetHashFromAssemblyFileW 函数
ms.date: 03/30/2017
api_name:
- GetHashFromAssemblyFileW
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromAssemblyFileW
helpviewer_keywords:
- GetHashFromAssemblyFileW function [.NET Framework strong naming]
ms.assetid: d1b2b172-5353-42af-a877-cf653c68ece0
topic_type:
- apiref
ms.openlocfilehash: 7f44106f12a2d21ea67acb874b577c5b303632b2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736669"
---
# <a name="gethashfromassemblyfilew-function"></a><span data-ttu-id="435ec-103">GetHashFromAssemblyFileW 函数</span><span class="sxs-lookup"><span data-stu-id="435ec-103">GetHashFromAssemblyFileW Function</span></span>

<span data-ttu-id="435ec-104">使用指定的哈希算法获取指定程序集文件的哈希。</span><span class="sxs-lookup"><span data-stu-id="435ec-104">Gets a hash of the specified assembly file, using the specified hash algorithm.</span></span> <span data-ttu-id="435ec-105">必须将程序集文件的路径指定为 Unicode 字符串。</span><span class="sxs-lookup"><span data-stu-id="435ec-105">The path to the assembly file must be specified as a Unicode string.</span></span>  
  
 <span data-ttu-id="435ec-106">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="435ec-106">This function has been deprecated.</span></span> <span data-ttu-id="435ec-107">改为使用 [ICLRStrongName：： GetHashFromAssemblyFileW](../hosting/iclrstrongname-gethashfromassemblyfilew-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="435ec-107">Use the [ICLRStrongName::GetHashFromAssemblyFileW](../hosting/iclrstrongname-gethashfromassemblyfilew-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="435ec-108">语法</span><span class="sxs-lookup"><span data-stu-id="435ec-108">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromAssemblyFileW (  
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="435ec-109">参数</span><span class="sxs-lookup"><span data-stu-id="435ec-109">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="435ec-110">中要进行哈希处理的文件的路径。</span><span class="sxs-lookup"><span data-stu-id="435ec-110">[in] The path to the file to be hashed.</span></span> <span data-ttu-id="435ec-111">此参数必须是 Unicode 字符串。</span><span class="sxs-lookup"><span data-stu-id="435ec-111">This parameter must be a Unicode string.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="435ec-112">[in，out]指定哈希算法的常量。</span><span class="sxs-lookup"><span data-stu-id="435ec-112">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="435ec-113">使用零作为默认哈希算法。</span><span class="sxs-lookup"><span data-stu-id="435ec-113">Use zero for the default hash algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="435ec-114">弄返回的哈希缓冲区。</span><span class="sxs-lookup"><span data-stu-id="435ec-114">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="435ec-115">中请求的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="435ec-115">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="435ec-116">弄返回的的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="435ec-116">[out] The returned size, in bytes, of `pbHash`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="435ec-117">要求</span><span class="sxs-lookup"><span data-stu-id="435ec-117">Requirements</span></span>  

 <span data-ttu-id="435ec-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="435ec-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="435ec-119">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="435ec-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="435ec-120">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="435ec-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="435ec-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="435ec-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="435ec-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="435ec-122">See also</span></span>

- [<span data-ttu-id="435ec-123">GetHashFromAssemblyFileW 方法</span><span class="sxs-lookup"><span data-stu-id="435ec-123">GetHashFromAssemblyFileW Method</span></span>](../hosting/iclrstrongname-gethashfromassemblyfilew-method.md)
- [<span data-ttu-id="435ec-124">GetHashFromAssemblyFile 方法</span><span class="sxs-lookup"><span data-stu-id="435ec-124">GetHashFromAssemblyFile Method</span></span>](../hosting/iclrstrongname-gethashfromassemblyfile-method.md)
- [<span data-ttu-id="435ec-125">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="435ec-125">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
