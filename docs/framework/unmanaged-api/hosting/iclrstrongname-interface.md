---
description: 了解详细信息： ICLRStrongName 接口
title: ICLRStrongName 接口
ms.date: 03/30/2017
api_name:
- ICLRStrongName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName
helpviewer_keywords:
- ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 2fac66fd-6b3b-4dbd-8baf-86038bd85526
topic_type:
- apiref
ms.openlocfilehash: 5565e864d35e68e714602b291a724a0ad9999a28
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799663"
---
# <a name="iclrstrongname-interface"></a><span data-ttu-id="583a0-103">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="583a0-103">ICLRStrongName Interface</span></span>

<span data-ttu-id="583a0-104">提供用于对具有强名称的程序集进行签名的基本全局静态函数。</span><span class="sxs-lookup"><span data-stu-id="583a0-104">Provides basic global static functions for signing assemblies with strong names.</span></span> <span data-ttu-id="583a0-105">所有 `ICLRStrongName` 方法都返回标准 COM hresult。</span><span class="sxs-lookup"><span data-stu-id="583a0-105">All `ICLRStrongName` methods return standard COM HRESULTs.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="583a0-106">方法</span><span class="sxs-lookup"><span data-stu-id="583a0-106">Methods</span></span>  
  
|<span data-ttu-id="583a0-107">方法</span><span class="sxs-lookup"><span data-stu-id="583a0-107">Method</span></span>|<span data-ttu-id="583a0-108">说明</span><span class="sxs-lookup"><span data-stu-id="583a0-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="583a0-109">GetHashFromAssemblyFile 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-109">GetHashFromAssemblyFile Method</span></span>](iclrstrongname-gethashfromassemblyfile-method.md)|<span data-ttu-id="583a0-110">使用指定的哈希算法获取指定程序集文件的哈希。</span><span class="sxs-lookup"><span data-stu-id="583a0-110">Gets a hash of the specified assembly file, using the specified hash algorithm.</span></span>|  
|[<span data-ttu-id="583a0-111">GetHashFromAssemblyFileW 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-111">GetHashFromAssemblyFileW Method</span></span>](iclrstrongname-gethashfromassemblyfilew-method.md)|<span data-ttu-id="583a0-112">使用指定的哈希算法获取指定为 Unicode 字符串的程序集文件的哈希。</span><span class="sxs-lookup"><span data-stu-id="583a0-112">Gets a hash of the assembly file specified as a Unicode string, using the specified hash algorithm.</span></span>|  
|[<span data-ttu-id="583a0-113">GetHashFromBlob 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-113">GetHashFromBlob Method</span></span>](iclrstrongname-gethashfromblob-method.md)|<span data-ttu-id="583a0-114">使用指定的哈希算法获取指定内存地址处的程序集的哈希。</span><span class="sxs-lookup"><span data-stu-id="583a0-114">Gets a hash of the assembly at the specified memory address, using the specified hash algorithm.</span></span>|  
|[<span data-ttu-id="583a0-115">GetHashFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-115">GetHashFromFile Method</span></span>](iclrstrongname-gethashfromfile-method.md)|<span data-ttu-id="583a0-116">生成指定文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="583a0-116">Generates a hash over the contents of the specified file.</span></span>|  
|[<span data-ttu-id="583a0-117">GetHashFromFileW 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-117">GetHashFromFileW Method</span></span>](iclrstrongname-gethashfromfilew-method.md)|<span data-ttu-id="583a0-118">生成由 Unicode 字符串指定的文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="583a0-118">Generates a hash over the contents of the file specified by a Unicode string.</span></span>|  
|[<span data-ttu-id="583a0-119">GetHashFromHandle 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-119">GetHashFromHandle Method</span></span>](iclrstrongname-gethashfromhandle-method.md)|<span data-ttu-id="583a0-120">使用指定的哈希算法，生成具有指定文件句柄的文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="583a0-120">Generates a hash over the contents of the file with the specified file handle, using the specified hash algorithm.</span></span>|  
|[<span data-ttu-id="583a0-121">StrongNameCompareAssemblies 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-121">StrongNameCompareAssemblies Method</span></span>](iclrstrongname-strongnamecompareassemblies-method.md)|<span data-ttu-id="583a0-122">确定两个程序集是否仅是强名称签名不同。</span><span class="sxs-lookup"><span data-stu-id="583a0-122">Determines whether two assemblies differ only by their strong name signatures.</span></span>|  
|[<span data-ttu-id="583a0-123">StrongNameFreeBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-123">StrongNameFreeBuffer Method</span></span>](iclrstrongname-strongnamefreebuffer-method.md)|<span data-ttu-id="583a0-124">释放以前对强名称方法（如 [StrongNameGetPublicKey](iclrstrongname-strongnamegetpublickey-method.md)、 [StrongNameTokenFromPublicKey](iclrstrongname-strongnametokenfrompublickey-method.md)或 [StrongNameSignatureGeneration](iclrstrongname-strongnamesignaturegeneration-method.md)）的调用所分配的内存。</span><span class="sxs-lookup"><span data-stu-id="583a0-124">Frees memory that was allocated with a previous call to a strong name method such as [StrongNameGetPublicKey](iclrstrongname-strongnamegetpublickey-method.md), [StrongNameTokenFromPublicKey](iclrstrongname-strongnametokenfrompublickey-method.md), or [StrongNameSignatureGeneration](iclrstrongname-strongnamesignaturegeneration-method.md).</span></span>|  
|[<span data-ttu-id="583a0-125">StrongNameGetBlob 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-125">StrongNameGetBlob Method</span></span>](iclrstrongname-strongnamegetblob-method.md)|<span data-ttu-id="583a0-126">使用指定地址处可执行文件的二进制表示形式填充指定的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="583a0-126">Fills the specified buffer with the binary representation of the executable file at the specified address.</span></span>|  
|[<span data-ttu-id="583a0-127">StrongNameGetBlobFromImage 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-127">StrongNameGetBlobFromImage Method</span></span>](iclrstrongname-strongnamegetblobfromimage-method.md)|<span data-ttu-id="583a0-128">获取指定内存地址处程序集映像的二进制表示形式。</span><span class="sxs-lookup"><span data-stu-id="583a0-128">Gets a binary representation of the assembly image at the specified memory address.</span></span>|  
|[<span data-ttu-id="583a0-129">StrongNameGetPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-129">StrongNameGetPublicKey Method</span></span>](iclrstrongname-strongnamegetpublickey-method.md)|<span data-ttu-id="583a0-130">从私钥/公钥对中获取公钥。</span><span class="sxs-lookup"><span data-stu-id="583a0-130">Gets the public key from a private/public key pair.</span></span>|  
|[<span data-ttu-id="583a0-131">StrongNameHashSize 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-131">StrongNameHashSize Method</span></span>](iclrstrongname-strongnamehashsize-method.md)|<span data-ttu-id="583a0-132">使用指定的哈希算法获取哈希所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="583a0-132">Gets the buffer size required for a hash, using the specified hash algorithm.</span></span>|  
|[<span data-ttu-id="583a0-133">StrongNameKeyDelete 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-133">StrongNameKeyDelete Method</span></span>](iclrstrongname-strongnamekeydelete-method.md)|<span data-ttu-id="583a0-134">删除指定的密钥容器。</span><span class="sxs-lookup"><span data-stu-id="583a0-134">Deletes the specified key container.</span></span>|  
|[<span data-ttu-id="583a0-135">StrongNameKeyGen 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-135">StrongNameKeyGen Method</span></span>](iclrstrongname-strongnamekeygen-method.md)|<span data-ttu-id="583a0-136">创建新的公钥/私钥对，以便强名称使用。</span><span class="sxs-lookup"><span data-stu-id="583a0-136">Creates a new public/private key pair for strong name use.</span></span>|  
|[<span data-ttu-id="583a0-137">StrongNameKeyGenEx 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-137">StrongNameKeyGenEx Method</span></span>](iclrstrongname-strongnamekeygenex-method.md)|<span data-ttu-id="583a0-138">生成具有指定密钥大小的新公钥/私钥对，以便强名称使用。</span><span class="sxs-lookup"><span data-stu-id="583a0-138">Generates a new public/private key pair with the specified key size for strong name use.</span></span>|  
|[<span data-ttu-id="583a0-139">StrongNameKeyInstall 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-139">StrongNameKeyInstall Method</span></span>](iclrstrongname-strongnamekeyinstall-method.md)|<span data-ttu-id="583a0-140">将公钥/私钥对导入容器。</span><span class="sxs-lookup"><span data-stu-id="583a0-140">Imports a public/private key pair into a container.</span></span>|  
|[<span data-ttu-id="583a0-141">StrongNameSignatureGeneration 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-141">StrongNameSignatureGeneration Method</span></span>](iclrstrongname-strongnamesignaturegeneration-method.md)|<span data-ttu-id="583a0-142">为指定的程序集生成强名称签名。</span><span class="sxs-lookup"><span data-stu-id="583a0-142">Generates a strong name signature for the specified assembly.</span></span>|  
|[<span data-ttu-id="583a0-143">StrongNameSignatureGenerationEx 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-143">StrongNameSignatureGenerationEx Method</span></span>](iclrstrongname-strongnamesignaturegenerationex-method.md)|<span data-ttu-id="583a0-144">根据指定标志为指定的程序集生成强名称签名。</span><span class="sxs-lookup"><span data-stu-id="583a0-144">Generates a strong name signature for the specified assembly, based on the specified flags.</span></span>|  
|[<span data-ttu-id="583a0-145">StrongNameSignatureSize 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-145">StrongNameSignatureSize Method</span></span>](iclrstrongname-strongnamesignaturesize-method.md)|<span data-ttu-id="583a0-146">返回强名称签名的大小。</span><span class="sxs-lookup"><span data-stu-id="583a0-146">Returns the size of the strong name signature.</span></span>|  
|[<span data-ttu-id="583a0-147">StrongNameSignatureVerification 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-147">StrongNameSignatureVerification Method</span></span>](iclrstrongname-strongnamesignatureverification-method.md)|<span data-ttu-id="583a0-148">获取一个值，该值指示提供的路径中的程序集清单是否包含根据指定标志验证的强名称签名。</span><span class="sxs-lookup"><span data-stu-id="583a0-148">Gets a value indicating whether the assembly manifest at the supplied path contains a strong name signature, which is verified according to the specified flags.</span></span>|  
|[<span data-ttu-id="583a0-149">StrongNameSignatureVerificationEx 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-149">StrongNameSignatureVerificationEx Method</span></span>](iclrstrongname-strongnamesignatureverificationex-method.md)|<span data-ttu-id="583a0-150">获取一个值，该值指示提供的路径中的程序集清单是否包含强名称签名。</span><span class="sxs-lookup"><span data-stu-id="583a0-150">Gets a value indicating whether the assembly manifest at the supplied path contains a strong name signature.</span></span>|  
|[<span data-ttu-id="583a0-151">StrongNameSignatureVerificationFromImage 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-151">StrongNameSignatureVerificationFromImage Method</span></span>](iclrstrongname-strongnamesignatureverificationfromimage-method.md)|<span data-ttu-id="583a0-152">验证已映射到内存的程序集对关联的公钥是否有效。</span><span class="sxs-lookup"><span data-stu-id="583a0-152">Verifies that an assembly that has already been mapped to memory is valid for the associated public key.</span></span>|  
|[<span data-ttu-id="583a0-153">StrongNameTokenFromAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-153">StrongNameTokenFromAssembly Method</span></span>](iclrstrongname-strongnametokenfromassembly-method.md)|<span data-ttu-id="583a0-154">从指定的程序集文件创建强名称令牌。</span><span class="sxs-lookup"><span data-stu-id="583a0-154">Creates a strong name token from the specified assembly file.</span></span>|  
|[<span data-ttu-id="583a0-155">StrongNameTokenFromAssemblyEx 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-155">StrongNameTokenFromAssemblyEx Method</span></span>](iclrstrongname-strongnametokenfromassemblyex-method.md)|<span data-ttu-id="583a0-156">从指定的程序集文件创建强名称令牌并返回公钥。</span><span class="sxs-lookup"><span data-stu-id="583a0-156">Creates a strong name token from the specified assembly file, and returns the public key.</span></span>|  
|[<span data-ttu-id="583a0-157">StrongNameTokenFromPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="583a0-157">StrongNameTokenFromPublicKey Method</span></span>](iclrstrongname-strongnametokenfrompublickey-method.md)|<span data-ttu-id="583a0-158">获取表示公钥的令牌。</span><span class="sxs-lookup"><span data-stu-id="583a0-158">Gets a token representing a public key.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="583a0-159">备注</span><span class="sxs-lookup"><span data-stu-id="583a0-159">Remarks</span></span>  

 <span data-ttu-id="583a0-160">可以 `ICLRStrongName` 通过使用和作为参数调用 [ICLRRuntimeInfo：： GetInterface](iclrruntimeinfo-getinterface-method.md) 方法来获取的实例 `CLSID_CLRStrongName` `IID_ICLRStrongName` 。</span><span class="sxs-lookup"><span data-stu-id="583a0-160">You can get an instance of the `ICLRStrongName` by calling the [ICLRRuntimeInfo::GetInterface](iclrruntimeinfo-getinterface-method.md) method using `CLSID_CLRStrongName` and `IID_ICLRStrongName` as parameters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="583a0-161">要求</span><span class="sxs-lookup"><span data-stu-id="583a0-161">Requirements</span></span>  

 <span data-ttu-id="583a0-162">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="583a0-162">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="583a0-163">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="583a0-163">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="583a0-164">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="583a0-164">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="583a0-165">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="583a0-165">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="583a0-166">请参阅</span><span class="sxs-lookup"><span data-stu-id="583a0-166">See also</span></span>

- [<span data-ttu-id="583a0-167">承载接口</span><span class="sxs-lookup"><span data-stu-id="583a0-167">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="583a0-168">承载</span><span class="sxs-lookup"><span data-stu-id="583a0-168">Hosting</span></span>](index.md)
