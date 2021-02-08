---
description: 了解详细信息： StrongNameTokenFromAssembly 函数
title: StrongNameTokenFromAssembly 函数
ms.date: 03/30/2017
api_name:
- StrongNameTokenFromAssembly
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameTokenFromAssembly
helpviewer_keywords:
- StrongNameTokenFromAssembly function [.NET Framework strong naming]
ms.assetid: 0a4b47ee-02f6-4a98-864e-a6f11ca3f2d9
topic_type:
- apiref
ms.openlocfilehash: 3646d441da4885624c15d5e53670a8dd8db45160
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794476"
---
# <a name="strongnametokenfromassembly-function"></a><span data-ttu-id="6c9d3-103">StrongNameTokenFromAssembly 函数</span><span class="sxs-lookup"><span data-stu-id="6c9d3-103">StrongNameTokenFromAssembly Function</span></span>

<span data-ttu-id="6c9d3-104">从指定的程序集文件创建强名称令牌。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-104">Creates a strong name token from the specified assembly file.</span></span>  
  
 <span data-ttu-id="6c9d3-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-105">This function has been deprecated.</span></span> <span data-ttu-id="6c9d3-106">改为使用 [ICLRStrongName：： StrongNameTokenFromAssembly](../hosting/iclrstrongname-strongnametokenfromassembly-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-106">Use the [ICLRStrongName::StrongNameTokenFromAssembly](../hosting/iclrstrongname-strongnametokenfromassembly-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c9d3-107">语法</span><span class="sxs-lookup"><span data-stu-id="6c9d3-107">Syntax</span></span>  
  
```cpp  
BOOLEAN StrongNameTokenFromAssembly (  
    [in]  LPCWSTR   wszFilePath,  
    [out] BYTE      **ppbStrongNameToken,  
    [out] ULONG     *pcbStrongNameToken  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6c9d3-108">参数</span><span class="sxs-lookup"><span data-stu-id="6c9d3-108">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="6c9d3-109">中适用于程序集的可移植可执行文件 (PE) 文件的路径。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-109">[in] The path to the portable executable (PE) file for the assembly.</span></span>  
  
 `ppbStrongNameToken`  
 <span data-ttu-id="6c9d3-110">弄返回的强名称标记。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-110">[out] The returned strong name token.</span></span>  
  
 `pcbStrongNameToken`  
 <span data-ttu-id="6c9d3-111">弄强名称令牌的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-111">[out] The size, in bytes, of the strong name token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6c9d3-112">返回值</span><span class="sxs-lookup"><span data-stu-id="6c9d3-112">Return Value</span></span>  

 <span data-ttu-id="6c9d3-113">`true` 成功完成时;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-113">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6c9d3-114">备注</span><span class="sxs-lookup"><span data-stu-id="6c9d3-114">Remarks</span></span>  

 <span data-ttu-id="6c9d3-115">强名称标记是公钥的缩写形式。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-115">A strong name token is the shortened form of a public key.</span></span> <span data-ttu-id="6c9d3-116">标记是从用于对程序集进行签名的公钥创建的64位哈希。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-116">The token is a 64-bit hash that is created from the public key used to sign the assembly.</span></span> <span data-ttu-id="6c9d3-117">该令牌是程序集的强名称的一部分，并且可以从程序集元数据中读取。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-117">The token is a part of the strong name for the assembly, and can be read from the assembly metadata.</span></span>  
  
 <span data-ttu-id="6c9d3-118">创建令牌后，应调用 [StrongNameFreeBuffer](strongnamefreebuffer-function.md) 函数以释放已分配的内存。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-118">After the token is created, you should call the [StrongNameFreeBuffer](strongnamefreebuffer-function.md) function to release the allocated memory.</span></span>  
  
 <span data-ttu-id="6c9d3-119">如果 `StrongNameTokenFromAssembly` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-119">If the `StrongNameTokenFromAssembly` function does not complete successfully, call the [StrongNameErrorInfo](strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6c9d3-120">要求</span><span class="sxs-lookup"><span data-stu-id="6c9d3-120">Requirements</span></span>  

 <span data-ttu-id="6c9d3-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6c9d3-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c9d3-122">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="6c9d3-122">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="6c9d3-123">**库：** 作为中的资源包含 mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="6c9d3-123">**Library:** Included as a resource in mscoree.dll</span></span>  
  
 <span data-ttu-id="6c9d3-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c9d3-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c9d3-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="6c9d3-125">See also</span></span>

- [<span data-ttu-id="6c9d3-126">StrongNameTokenFromAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="6c9d3-126">StrongNameTokenFromAssembly Method</span></span>](../hosting/iclrstrongname-strongnametokenfromassembly-method.md)
- [<span data-ttu-id="6c9d3-127">StrongNameTokenFromAssemblyEx 方法</span><span class="sxs-lookup"><span data-stu-id="6c9d3-127">StrongNameTokenFromAssemblyEx Method</span></span>](../hosting/iclrstrongname-strongnametokenfromassemblyex-method.md)
- [<span data-ttu-id="6c9d3-128">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="6c9d3-128">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
