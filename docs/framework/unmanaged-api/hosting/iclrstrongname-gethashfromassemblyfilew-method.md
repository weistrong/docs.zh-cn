---
description: 了解详细信息： ICLRStrongName：： GetHashFromAssemblyFileW 方法
title: ICLRStrongName::GetHashFromAssemblyFileW 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromAssemblyFileW
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromAssemblyFileW
helpviewer_keywords:
- ICLRStrongName::GetHashFromAssemblyFileW method [.NET Framework hosting]
- GetHashFromAssemblyFileW method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 5d0b44a2-5a14-44a2-9a0e-e8682fd4e106
topic_type:
- apiref
ms.openlocfilehash: 27123ed8217d49765fe3fd7c19efc92f4e770722
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637074"
---
# <a name="iclrstrongnamegethashfromassemblyfilew-method"></a><span data-ttu-id="3be48-103">ICLRStrongName::GetHashFromAssemblyFileW 方法</span><span class="sxs-lookup"><span data-stu-id="3be48-103">ICLRStrongName::GetHashFromAssemblyFileW Method</span></span>

<span data-ttu-id="3be48-104">生成由 Unicode 字符串指定的文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="3be48-104">Generates a hash over the contents of the file specified by a Unicode string.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3be48-105">语法</span><span class="sxs-lookup"><span data-stu-id="3be48-105">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromAssemblyFileW (  
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3be48-106">参数</span><span class="sxs-lookup"><span data-stu-id="3be48-106">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="3be48-107">中要进行哈希处理的文件的路径。</span><span class="sxs-lookup"><span data-stu-id="3be48-107">[in] The path to the file to be hashed.</span></span> <span data-ttu-id="3be48-108">此参数必须是 Unicode 字符串。</span><span class="sxs-lookup"><span data-stu-id="3be48-108">This parameter must be a Unicode string.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="3be48-109">[in，out]指定哈希算法的常量。</span><span class="sxs-lookup"><span data-stu-id="3be48-109">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="3be48-110">使用零作为默认哈希算法。</span><span class="sxs-lookup"><span data-stu-id="3be48-110">Use zero for the default hash algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="3be48-111">弄返回的哈希缓冲区。</span><span class="sxs-lookup"><span data-stu-id="3be48-111">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="3be48-112">中请求的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="3be48-112">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="3be48-113">弄返回的的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="3be48-113">[out] The returned size, in bytes, of `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3be48-114">返回值</span><span class="sxs-lookup"><span data-stu-id="3be48-114">Return Value</span></span>  

 <span data-ttu-id="3be48-115">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="3be48-115">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3be48-116">要求</span><span class="sxs-lookup"><span data-stu-id="3be48-116">Requirements</span></span>  

 <span data-ttu-id="3be48-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3be48-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3be48-118">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="3be48-118">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="3be48-119">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3be48-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3be48-120">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3be48-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3be48-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="3be48-121">See also</span></span>

- [<span data-ttu-id="3be48-122">GetHashFromAssemblyFile 方法</span><span class="sxs-lookup"><span data-stu-id="3be48-122">GetHashFromAssemblyFile Method</span></span>](iclrstrongname-gethashfromassemblyfile-method.md)
- [<span data-ttu-id="3be48-123">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="3be48-123">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
