---
description: 了解详细信息： UnsafeNclNativeMethods 类
title: 'UnsafeNclNativeMethods 类 (System.Net) '
ms.date: 06/12/2020
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.UnsafeNclNativeMethods
- System.Net.UnsafeNclNativeMethods.NativePKI
- System.Net.UnsafeNclNativeMethods.NativePKI.FindClientCertificates
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: fa1084efddae0ba5cbfc9a949dcd94d2c64f3272
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699488"
---
# <a name="unsafenclnativemethods-class"></a><span data-ttu-id="83836-103">UnsafeNclNativeMethods 类</span><span class="sxs-lookup"><span data-stu-id="83836-103">UnsafeNclNativeMethods class</span></span>

<span data-ttu-id="83836-104">包含导入不安全的本机网络方法的类。</span><span class="sxs-lookup"><span data-stu-id="83836-104">Contains classes that import unsafe native networking methods.</span></span> <span data-ttu-id="83836-105">此类不能被继承。</span><span class="sxs-lookup"><span data-stu-id="83836-105">This class cannot be inherited.</span></span>

```csharp
internal static class UnsafeNclNativeMethods
```

> [!WARNING]
> <span data-ttu-id="83836-106">此类是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="83836-106">This class is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="83836-107">在任何情况下，Microsoft 不支持在生产应用程序中使用此类。</span><span class="sxs-lookup"><span data-stu-id="83836-107">Microsoft does not support the use of this class in a production application under any circumstance.</span></span>

## <a name="nativepki-class"></a><span data-ttu-id="83836-108">NativePKI 类</span><span class="sxs-lookup"><span data-stu-id="83836-108">NativePKI class</span></span>

<span data-ttu-id="83836-109">包含从 crypt32.dll 导入的方法。</span><span class="sxs-lookup"><span data-stu-id="83836-109">Contains methods imported from crypt32.dll.</span></span> <span data-ttu-id="83836-110">使用超文本传输协议 (HTTPS) 安全时，这些方法将处理证书。</span><span class="sxs-lookup"><span data-stu-id="83836-110">These methods handle certificates when using Hypertext Transfer Protocol Secure (HTTPS).</span></span> <span data-ttu-id="83836-111">此类不能被继承。</span><span class="sxs-lookup"><span data-stu-id="83836-111">This class cannot be inherited.</span></span>

```csharp
internal static class NativePKI
```

## <a name="nativepkifindclientcertificates-method"></a><span data-ttu-id="83836-112">NativePKI. FindClientCertificates 方法</span><span class="sxs-lookup"><span data-stu-id="83836-112">NativePKI.FindClientCertificates method</span></span>

<span data-ttu-id="83836-113">发现要发送到服务器的可用客户端证书。</span><span class="sxs-lookup"><span data-stu-id="83836-113">Discovers available client certificates to send to the server.</span></span>

```csharp
internal static X509CertificateCollection FindClientCertificates
```

### <a name="return-value"></a><span data-ttu-id="83836-114">返回值</span><span class="sxs-lookup"><span data-stu-id="83836-114">Return value</span></span>

<xref:System.Security.Cryptography.X509Certificates.X509CertificateCollection?displayProperty=nameWithType>

<span data-ttu-id="83836-115">可用客户端证书的集合。</span><span class="sxs-lookup"><span data-stu-id="83836-115">A collection of available client certificates.</span></span>

## <a name="requirements"></a><span data-ttu-id="83836-116">要求</span><span class="sxs-lookup"><span data-stu-id="83836-116">Requirements</span></span>

<span data-ttu-id="83836-117">**命名空间：** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="83836-117">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="83836-118">**程序集：** System.dll 中的系统 () </span><span class="sxs-lookup"><span data-stu-id="83836-118">**Assembly:** System (in System.dll)</span></span>
