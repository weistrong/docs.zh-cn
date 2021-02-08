---
description: 详细了解：强命名（非托管 API 参考）
title: 强命名（非托管 API 参考）
ms.date: 03/30/2017
helpviewer_keywords:
- strong naming [.NET Framework], using the unmanaged API
- native API reference [.NET Framework], strong naming
- unmanaged API reference [.NET Framework], strong naming
ms.assetid: 428c68b6-a7b4-44be-b280-75905f46612c
ms.openlocfilehash: 058cc51d8e9eb2ef4a2d0670811aefcd32dafb6e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646356"
---
# <a name="strong-naming-unmanaged-api-reference"></a><span data-ttu-id="12d2b-103">强命名（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="12d2b-103">Strong Naming (Unmanaged API Reference)</span></span>

<span data-ttu-id="12d2b-104">强命名 API 允许客户端管理程序集的强名称签名。</span><span class="sxs-lookup"><span data-stu-id="12d2b-104">The strong naming API enables a client to administer strong name signing for assemblies.</span></span>  
  
 <span data-ttu-id="12d2b-105">使用强名称对程序集进行签名将向包含程序集清单的文件添加公钥加密。</span><span class="sxs-lookup"><span data-stu-id="12d2b-105">Signing an assembly with a strong name adds a public key encryption to the file containing the assembly manifest.</span></span> <span data-ttu-id="12d2b-106">强名称签名帮助验证名称的唯一性，避免名称欺骗，并在解析引用时向调用方提供唯一标识。</span><span class="sxs-lookup"><span data-stu-id="12d2b-106">Strong name signing helps verify name uniqueness, prevents name spoofing, and provides callers with a unique identity when a reference is resolved.</span></span> <span data-ttu-id="12d2b-107">但是，任何信任级别都不会与强名称关联。</span><span class="sxs-lookup"><span data-stu-id="12d2b-107">However, no level of trust is associated with a strong name.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="12d2b-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="12d2b-108">In This Section</span></span>  
  
> [!NOTE]
> <span data-ttu-id="12d2b-109">从 .NET Framework 4 开始，所有这些函数都已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-109">All of these functions have been deprecated starting with the .NET Framework 4.</span></span> <span data-ttu-id="12d2b-110">有关建议的替代方案，请参阅 [ICLRStrongName](../hosting/iclrstrongname-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="12d2b-110">For suggested alternatives, see the [ICLRStrongName](../hosting/iclrstrongname-interface.md) interface.</span></span>  
  
 [<span data-ttu-id="12d2b-111">GetHashFromAssemblyFile 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-111">GetHashFromAssemblyFile Function</span></span>](gethashfromassemblyfile-function.md)  
 <span data-ttu-id="12d2b-112">使用指定的哈希算法获取指定程序集文件的哈希。</span><span class="sxs-lookup"><span data-stu-id="12d2b-112">Gets a hash of the specified assembly file, using the specified hash algorithm.</span></span> <span data-ttu-id="12d2b-113">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-113">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-114">GetHashFromAssemblyFileW 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-114">GetHashFromAssemblyFileW Function</span></span>](gethashfromassemblyfilew-function.md)  
 <span data-ttu-id="12d2b-115">使用指定的哈希算法获取指定为 Unicode 字符串的程序集文件的哈希。</span><span class="sxs-lookup"><span data-stu-id="12d2b-115">Gets a hash of the assembly file specified as a Unicode string, using the specified hash algorithm.</span></span> <span data-ttu-id="12d2b-116">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-116">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-117">GetHashFromBlob 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-117">GetHashFromBlob Function</span></span>](gethashfromblob-function.md)  
 <span data-ttu-id="12d2b-118">使用指定的哈希算法获取指定内存地址处的程序集的哈希。</span><span class="sxs-lookup"><span data-stu-id="12d2b-118">Gets a hash of the assembly at the specified memory address, using the specified hash algorithm.</span></span> <span data-ttu-id="12d2b-119">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-119">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-120">GetHashFromFile 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-120">GetHashFromFile Function</span></span>](gethashfromfile-function.md)  
 <span data-ttu-id="12d2b-121">生成指定文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="12d2b-121">Generates a hash over the contents of the specified file.</span></span>  <span data-ttu-id="12d2b-122">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-122">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-123">GetHashFromFileW 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-123">GetHashFromFileW Function</span></span>](gethashfromfilew-function.md)  
 <span data-ttu-id="12d2b-124">生成由 Unicode 字符串指定的文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="12d2b-124">Generates a hash over the contents of the file specified by a Unicode string.</span></span> <span data-ttu-id="12d2b-125">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-125">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-126">GetHashFromHandle 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-126">GetHashFromHandle Function</span></span>](gethashfromhandle-function.md)  
 <span data-ttu-id="12d2b-127">使用指定的哈希算法，生成具有指定文件句柄的文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="12d2b-127">Generates a hash over the contents of the file with the specified file handle, using the specified hash algorithm.</span></span>  <span data-ttu-id="12d2b-128">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-128">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-129">StrongNameCompareAssemblies 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-129">StrongNameCompareAssemblies Function</span></span>](strongnamecompareassemblies-function.md)  
 <span data-ttu-id="12d2b-130">确定两个程序集是否仅是强名称签名不同。</span><span class="sxs-lookup"><span data-stu-id="12d2b-130">Determines whether two assemblies differ only by their strong name signatures.</span></span> <span data-ttu-id="12d2b-131">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-131">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-132">StrongNameErrorInfo 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-132">StrongNameErrorInfo Function</span></span>](strongnameerrorinfo-function.md)  
 <span data-ttu-id="12d2b-133">获取由其中一个强名称函数引发的最后一个错误代码。</span><span class="sxs-lookup"><span data-stu-id="12d2b-133">Gets the last error code that was raised by one of the strong name functions.</span></span>  
  
 [<span data-ttu-id="12d2b-134">StrongNameFreeBuffer 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-134">StrongNameFreeBuffer Function</span></span>](strongnamefreebuffer-function.md)  
 <span data-ttu-id="12d2b-135">释放先前调用 [StrongNameGetPublicKey](strongnamegetpublickey-function.md)、[StrongNameTokenFromPublicKey](strongnametokenfrompublickey-function.md) 或 [StrongNameSignatureGeneration](strongnamesignaturegeneration-function.md) 强名称函数分配的内存。</span><span class="sxs-lookup"><span data-stu-id="12d2b-135">Frees memory that was allocated with a previous call to a strong name function such as [StrongNameGetPublicKey](strongnamegetpublickey-function.md), [StrongNameTokenFromPublicKey](strongnametokenfrompublickey-function.md), or [StrongNameSignatureGeneration](strongnamesignaturegeneration-function.md).</span></span>   <span data-ttu-id="12d2b-136">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-136">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-137">StrongNameGetBlob 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-137">StrongNameGetBlob Function</span></span>](strongnamegetblob-function.md)  
 <span data-ttu-id="12d2b-138">使用指定地址处可执行文件的二进制表示形式填充指定的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="12d2b-138">Fills the specified buffer with the binary representation of the executable file at the specified address.</span></span> <span data-ttu-id="12d2b-139">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-139">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-140">StrongNameGetBlobFromImage 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-140">StrongNameGetBlobFromImage Function</span></span>](strongnamegetblobfromimage-function.md)  
 <span data-ttu-id="12d2b-141">获取指定内存地址处程序集映像的二进制表示形式。</span><span class="sxs-lookup"><span data-stu-id="12d2b-141">Gets a binary representation of the assembly image at the specified memory address.</span></span> <span data-ttu-id="12d2b-142">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-142">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-143">StrongNameGetPublicKey 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-143">StrongNameGetPublicKey Function</span></span>](strongnamegetpublickey-function.md)  
 <span data-ttu-id="12d2b-144">从私钥/公钥对中获取公钥。</span><span class="sxs-lookup"><span data-stu-id="12d2b-144">Gets the public key from a private/public key pair.</span></span> <span data-ttu-id="12d2b-145">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-145">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-146">StrongNameHashSize 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-146">StrongNameHashSize Function</span></span>](strongnamehashsize-function.md)  
 <span data-ttu-id="12d2b-147">使用指定的哈希算法获取哈希所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="12d2b-147">Gets the buffer size required for a hash, using the specified hash algorithm.</span></span>  <span data-ttu-id="12d2b-148">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-148">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-149">StrongNameKeyDelete 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-149">StrongNameKeyDelete Function</span></span>](strongnamekeydelete-function.md)  
 <span data-ttu-id="12d2b-150">删除指定的密钥容器。</span><span class="sxs-lookup"><span data-stu-id="12d2b-150">Deletes the specified key container.</span></span> <span data-ttu-id="12d2b-151">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-151">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-152">StrongNameKeyGen 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-152">StrongNameKeyGen Function</span></span>](strongnamekeygen-function.md)  
 <span data-ttu-id="12d2b-153">创建新的公钥/私钥对，以便强名称使用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-153">Creates a new public/private key pair for strong name use.</span></span>  <span data-ttu-id="12d2b-154">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-154">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-155">StrongNameKeyGenEx 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-155">StrongNameKeyGenEx Function</span></span>](strongnamekeygenex-function.md)  
 <span data-ttu-id="12d2b-156">生成具有指定密钥大小的新公钥/私钥对，以便强名称使用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-156">Generates a new public/private key pair with the specified key size for strong name use.</span></span> <span data-ttu-id="12d2b-157">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-157">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-158">StrongNameKeyInstall 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-158">StrongNameKeyInstall Function</span></span>](strongnamekeyinstall-function.md)  
 <span data-ttu-id="12d2b-159">将公钥/私钥对导入容器。</span><span class="sxs-lookup"><span data-stu-id="12d2b-159">Imports a public/private key pair into a container.</span></span>  <span data-ttu-id="12d2b-160">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-160">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-161">StrongNameSignatureGeneration 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-161">StrongNameSignatureGeneration Function</span></span>](strongnamesignaturegeneration-function.md)  
 <span data-ttu-id="12d2b-162">为指定的程序集生成强名称签名。</span><span class="sxs-lookup"><span data-stu-id="12d2b-162">Generates a strong name signature for the specified assembly.</span></span>   <span data-ttu-id="12d2b-163">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-163">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-164">StrongNameSignatureGenerationEx 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-164">StrongNameSignatureGenerationEx Function</span></span>](strongnamesignaturegenerationex-function.md)  
 <span data-ttu-id="12d2b-165">根据指定标志为指定的程序集生成强名称签名。</span><span class="sxs-lookup"><span data-stu-id="12d2b-165">Generates a strong name signature for the specified assembly, based on the specified flags.</span></span>    <span data-ttu-id="12d2b-166">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-166">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-167">StrongNameSignatureSize 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-167">StrongNameSignatureSize Function</span></span>](strongnamesignaturesize-function.md)  
 <span data-ttu-id="12d2b-168">返回强名称签名的大小。</span><span class="sxs-lookup"><span data-stu-id="12d2b-168">Returns the size of the strong name signature.</span></span> <span data-ttu-id="12d2b-169">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-169">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-170">StrongNameSignatureVerification 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-170">StrongNameSignatureVerification Function</span></span>](strongnamesignatureverification-function.md)  
 <span data-ttu-id="12d2b-171">获取一个值，该值指示提供的路径中的程序集清单是否包含根据指定标志验证的强名称签名。</span><span class="sxs-lookup"><span data-stu-id="12d2b-171">Gets a value indicating whether the assembly manifest at the supplied path contains a strong name signature, which is verified according to the specified flags.</span></span> <span data-ttu-id="12d2b-172">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-172">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-173">StrongNameSignatureVerificationEx 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-173">StrongNameSignatureVerificationEx Function</span></span>](strongnamesignatureverificationex-function.md)  
 <span data-ttu-id="12d2b-174">获取一个值，该值指示提供的路径中的程序集清单是否包含强名称签名。</span><span class="sxs-lookup"><span data-stu-id="12d2b-174">Gets a value indicating whether the assembly manifest at the supplied path contains a strong name signature.</span></span>  <span data-ttu-id="12d2b-175">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-175">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-176">StrongNameSignatureVerificationFromImage 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-176">StrongNameSignatureVerificationFromImage Function</span></span>](strongnamesignatureverificationfromimage-function.md)  
 <span data-ttu-id="12d2b-177">验证已映射到内存的程序集对关联的公钥是否有效。</span><span class="sxs-lookup"><span data-stu-id="12d2b-177">Verifies that an assembly that has already been mapped to memory is valid for the associated public key.</span></span> <span data-ttu-id="12d2b-178">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-178">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-179">StrongNameTokenFromAssembly 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-179">StrongNameTokenFromAssembly Function</span></span>](strongnametokenfromassembly-function.md)  
 <span data-ttu-id="12d2b-180">从指定的程序集文件创建强名称令牌。</span><span class="sxs-lookup"><span data-stu-id="12d2b-180">Creates a strong name token from the specified assembly file.</span></span>  <span data-ttu-id="12d2b-181">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-181">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-182">StrongNameTokenFromAssemblyEx 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-182">StrongNameTokenFromAssemblyEx Function</span></span>](strongnametokenfromassemblyex-function.md)  
 <span data-ttu-id="12d2b-183">从指定的程序集文件创建强名称令牌并返回公钥。</span><span class="sxs-lookup"><span data-stu-id="12d2b-183">Creates a strong name token from the specified assembly file, and returns the public key.</span></span> <span data-ttu-id="12d2b-184">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-184">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-185">StrongNameTokenFromPublicKey 函数</span><span class="sxs-lookup"><span data-stu-id="12d2b-185">StrongNameTokenFromPublicKey Function</span></span>](strongnametokenfrompublickey-function.md)  
 <span data-ttu-id="12d2b-186">获取表示公钥的令牌。</span><span class="sxs-lookup"><span data-stu-id="12d2b-186">Gets a token representing a public key.</span></span> <span data-ttu-id="12d2b-187">从 .NET Framework 4 开始已弃用。</span><span class="sxs-lookup"><span data-stu-id="12d2b-187">Deprecated starting with the .NET Framework 4.</span></span>  
  
 [<span data-ttu-id="12d2b-188">PublicKeyBlob 结构</span><span class="sxs-lookup"><span data-stu-id="12d2b-188">PublicKeyBlob Structure</span></span>](publickeyblob-structure.md)  
 <span data-ttu-id="12d2b-189">表示二进制格式的公钥/私钥对中的公钥。</span><span class="sxs-lookup"><span data-stu-id="12d2b-189">Represents the public key of a public/private key pair in binary format.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12d2b-190">另请参阅</span><span class="sxs-lookup"><span data-stu-id="12d2b-190">See also</span></span>

- [<span data-ttu-id="12d2b-191">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="12d2b-191">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
- [<span data-ttu-id="12d2b-192">非托管 API 参考</span><span class="sxs-lookup"><span data-stu-id="12d2b-192">Unmanaged API Reference</span></span>](../index.md)
