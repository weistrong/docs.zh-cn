---
description: 了解详细信息： GetHashFromAssemblyFile 函数
title: GetHashFromAssemblyFile 函数
ms.date: 03/30/2017
api_name:
- GetHashFromAssemblyFile
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromAssemblyFile
helpviewer_keywords:
- GetHashFromAssemblyFile function [.NET Framework strong naming]
ms.assetid: 751ed69f-b7ab-4e07-80de-e17ca9319b0c
topic_type:
- apiref
ms.openlocfilehash: 79cc6289ebcf33f5a9ea8b4ef139c4b2a67e55e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736773"
---
# <a name="gethashfromassemblyfile-function"></a><span data-ttu-id="2645f-103">GetHashFromAssemblyFile 函数</span><span class="sxs-lookup"><span data-stu-id="2645f-103">GetHashFromAssemblyFile Function</span></span>

<span data-ttu-id="2645f-104">使用指定的哈希算法获取指定程序集文件的哈希。</span><span class="sxs-lookup"><span data-stu-id="2645f-104">Gets a hash of the specified assembly file, using the specified hash algorithm.</span></span>  
  
 <span data-ttu-id="2645f-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="2645f-105">This function has been deprecated.</span></span> <span data-ttu-id="2645f-106">改为使用 [ICLRStrongName：： GetHashFromAssemblyFile](../hosting/iclrstrongname-gethashfromassemblyfile-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="2645f-106">Use the [ICLRStrongName::GetHashFromAssemblyFile](../hosting/iclrstrongname-gethashfromassemblyfile-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2645f-107">语法</span><span class="sxs-lookup"><span data-stu-id="2645f-107">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromAssemblyFile (  
    [in]  LPCSTR   szFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2645f-108">参数</span><span class="sxs-lookup"><span data-stu-id="2645f-108">Parameters</span></span>  

 `szFilePath`  
 <span data-ttu-id="2645f-109">中要进行哈希处理的文件的路径。</span><span class="sxs-lookup"><span data-stu-id="2645f-109">[in] The path to the file to be hashed.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="2645f-110">[in，out]指定哈希算法的常量。</span><span class="sxs-lookup"><span data-stu-id="2645f-110">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="2645f-111">使用零作为默认哈希算法。</span><span class="sxs-lookup"><span data-stu-id="2645f-111">Use zero for the default hash algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="2645f-112">弄返回的哈希缓冲区。</span><span class="sxs-lookup"><span data-stu-id="2645f-112">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="2645f-113">中请求的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="2645f-113">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="2645f-114">弄返回的的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="2645f-114">[out] The returned size, in bytes, of `pbHash`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2645f-115">要求</span><span class="sxs-lookup"><span data-stu-id="2645f-115">Requirements</span></span>  

 <span data-ttu-id="2645f-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2645f-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2645f-117">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="2645f-117">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="2645f-118">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2645f-118">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="2645f-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2645f-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2645f-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="2645f-120">See also</span></span>

- [<span data-ttu-id="2645f-121">GetHashFromAssemblyFile 方法</span><span class="sxs-lookup"><span data-stu-id="2645f-121">GetHashFromAssemblyFile Method</span></span>](../hosting/iclrstrongname-gethashfromassemblyfile-method.md)
- [<span data-ttu-id="2645f-122">GetHashFromAssemblyFileW 方法</span><span class="sxs-lookup"><span data-stu-id="2645f-122">GetHashFromAssemblyFileW Method</span></span>](../hosting/iclrstrongname-gethashfromassemblyfilew-method.md)
- [<span data-ttu-id="2645f-123">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="2645f-123">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
