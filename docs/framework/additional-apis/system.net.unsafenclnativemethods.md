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
# <a name="unsafenclnativemethods-class"></a>UnsafeNclNativeMethods 类

包含导入不安全的本机网络方法的类。 此类不能被继承。

```csharp
internal static class UnsafeNclNativeMethods
```

> [!WARNING]
> 此类是内部的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此类。

## <a name="nativepki-class"></a>NativePKI 类

包含从 crypt32.dll 导入的方法。 使用超文本传输协议 (HTTPS) 安全时，这些方法将处理证书。 此类不能被继承。

```csharp
internal static class NativePKI
```

## <a name="nativepkifindclientcertificates-method"></a>NativePKI. FindClientCertificates 方法

发现要发送到服务器的可用客户端证书。

```csharp
internal static X509CertificateCollection FindClientCertificates
```

### <a name="return-value"></a>返回值

<xref:System.Security.Cryptography.X509Certificates.X509CertificateCollection?displayProperty=nameWithType>

可用客户端证书的集合。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Net>

**程序集：** System.dll 中的系统 () 
