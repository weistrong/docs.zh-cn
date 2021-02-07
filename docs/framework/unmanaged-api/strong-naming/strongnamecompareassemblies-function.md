---
description: 了解详细信息： StrongNameCompareAssemblies 函数
title: StrongNameCompareAssemblies 函数
ms.date: 03/30/2017
api_name:
- StrongNameCompareAssemblies
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameCompareAssemblies
helpviewer_keywords:
- StrongNameCompareAssemblies function [.NET Framework strong naming]
ms.assetid: 763f2375-efc6-4219-8806-a3b0567ef72b
topic_type:
- apiref
ms.openlocfilehash: e59bb96a89dc1e1cf8b809c3e0d538aaffe83b8e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736485"
---
# <a name="strongnamecompareassemblies-function"></a><span data-ttu-id="4ab96-103">StrongNameCompareAssemblies 函数</span><span class="sxs-lookup"><span data-stu-id="4ab96-103">StrongNameCompareAssemblies Function</span></span>

<span data-ttu-id="4ab96-104">确定两个程序集是否仅是强名称签名不同。</span><span class="sxs-lookup"><span data-stu-id="4ab96-104">Determines whether two assemblies differ only by their strong name signatures.</span></span>  
  
 <span data-ttu-id="4ab96-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="4ab96-105">This function has been deprecated.</span></span> <span data-ttu-id="4ab96-106">改为使用 [ICLRStrongName：： StrongNameCompareAssemblies](../hosting/iclrstrongname-strongnamecompareassemblies-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4ab96-106">Use the [ICLRStrongName::StrongNameCompareAssemblies](../hosting/iclrstrongname-strongnamecompareassemblies-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ab96-107">语法</span><span class="sxs-lookup"><span data-stu-id="4ab96-107">Syntax</span></span>  
  
```cpp  
BOOLEAN StrongNameCompareAssemblies (  
    [in]  LPCWSTR   wszAssembly1,  
    [in]  LPCWSTR   wszAssembly2,  
    [out] DWORD     *pdwResult  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4ab96-108">参数</span><span class="sxs-lookup"><span data-stu-id="4ab96-108">Parameters</span></span>  

 `wszAssembly1`  
 <span data-ttu-id="4ab96-109">中第一个程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="4ab96-109">[in] The path to the first assembly.</span></span>  
  
 `wszAssembly2`  
 <span data-ttu-id="4ab96-110">中第二个程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="4ab96-110">[in] The path to the second assembly.</span></span>  
  
 `pdwResult`  
 <span data-ttu-id="4ab96-111">弄以下值之一：</span><span class="sxs-lookup"><span data-stu-id="4ab96-111">[out] One of the following values:</span></span>  
  
- <span data-ttu-id="4ab96-112">`SN_CMP_DIFFERENT` (0) -指定程序集包含不同的数据。</span><span class="sxs-lookup"><span data-stu-id="4ab96-112">`SN_CMP_DIFFERENT` (0) - Specifies that the assemblies contain different data.</span></span>  
  
- <span data-ttu-id="4ab96-113">`SN_CMP_IDENTICAL` (1) -指定程序集完全相同，包括它们的签名和校验和。</span><span class="sxs-lookup"><span data-stu-id="4ab96-113">`SN_CMP_IDENTICAL` (1) - Specifies that the assemblies are exactly the same, including their signatures and checksum.</span></span>  
  
- <span data-ttu-id="4ab96-114">`SN_CMP_SIGONLY` (2) -指定程序集不同于签名和校验和。</span><span class="sxs-lookup"><span data-stu-id="4ab96-114">`SN_CMP_SIGONLY` (2) - Specifies that the assemblies differ only by signature and checksum.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4ab96-115">返回值</span><span class="sxs-lookup"><span data-stu-id="4ab96-115">Return Value</span></span>  

 <span data-ttu-id="4ab96-116">`true` 成功完成时;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="4ab96-116">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4ab96-117">要求</span><span class="sxs-lookup"><span data-stu-id="4ab96-117">Requirements</span></span>  

 <span data-ttu-id="4ab96-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4ab96-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4ab96-119">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="4ab96-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="4ab96-120">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4ab96-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="4ab96-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4ab96-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4ab96-122">备注</span><span class="sxs-lookup"><span data-stu-id="4ab96-122">Remarks</span></span>  

 <span data-ttu-id="4ab96-123">程序集的强名称签名由程序集的文本名称、版本、区域性和公钥标记组成。</span><span class="sxs-lookup"><span data-stu-id="4ab96-123">The strong name signature of an assembly consists of the assembly's text name, version, culture, and public key token.</span></span>  
  
 <span data-ttu-id="4ab96-124">如果 `StrongNameCompareAssemblies` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。</span><span class="sxs-lookup"><span data-stu-id="4ab96-124">If the `StrongNameCompareAssemblies` function does not complete successfully, call the [StrongNameErrorInfo](strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ab96-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="4ab96-125">See also</span></span>

- [<span data-ttu-id="4ab96-126">StrongNameCompareAssemblies 方法</span><span class="sxs-lookup"><span data-stu-id="4ab96-126">StrongNameCompareAssemblies Method</span></span>](../hosting/iclrstrongname-strongnamecompareassemblies-method.md)
- [<span data-ttu-id="4ab96-127">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="4ab96-127">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
