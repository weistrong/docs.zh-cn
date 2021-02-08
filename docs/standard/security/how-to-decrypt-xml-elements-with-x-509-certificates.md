---
description: 了解详细信息：如何：用 x.509 证书对 XML 元素进行解密
title: 如何：使用 X.509 证书解密 XML 元素
ms.date: 07/14/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- System.Security.Cryptography.EncryptedXml class
- XML encryption
- System.Security.Cryptography.X509Certificate2 class
- decryption
- X.509 certificates
- certificates, X.509 certificates
ms.assetid: bd015722-d88d-408d-8ca8-e4e475c441ed
ms.openlocfilehash: 40006ca1d3e76dbbc0899c0c22090b27c2cfb0de
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792370"
---
# <a name="how-to-decrypt-xml-elements-with-x509-certificates"></a><span data-ttu-id="dd75a-103">如何：使用 X.509 证书解密 XML 元素</span><span class="sxs-lookup"><span data-stu-id="dd75a-103">How to: Decrypt XML Elements with X.509 Certificates</span></span>

<span data-ttu-id="dd75a-104">可以使用 <xref:System.Security.Cryptography.Xml> 命名空间中的类对 XML 文档内的元素进行加密和解密。</span><span class="sxs-lookup"><span data-stu-id="dd75a-104">You can use the classes in the <xref:System.Security.Cryptography.Xml> namespace to encrypt and decrypt an element within an XML document.</span></span>  <span data-ttu-id="dd75a-105">XML 加密是交换或存储加密的 XML 数据的一种标准方式，使用后就无需担心数据被轻易读取。</span><span class="sxs-lookup"><span data-stu-id="dd75a-105">XML Encryption is a standard way to exchange or store encrypted XML data, without worrying about the data being easily read.</span></span>  <span data-ttu-id="dd75a-106">有关 XML 加密标准的详细信息，请参阅位于万维网联合会 (W3C) 规范 for XML Encryption <https://www.w3.org/TR/xmldsig-core/> 。</span><span class="sxs-lookup"><span data-stu-id="dd75a-106">For more information about the XML Encryption standard, see the World Wide Web Consortium (W3C) specification for XML Encryption located at <https://www.w3.org/TR/xmldsig-core/>.</span></span>  
  
 <span data-ttu-id="dd75a-107">此示例对使用中所述的方法进行加密的 XML 元素进行解密： how [to：使用 X.509 证书对 XML 元素进行加密](how-to-encrypt-xml-elements-with-x-509-certificates.md)。</span><span class="sxs-lookup"><span data-stu-id="dd75a-107">This example decrypts an XML element that was encrypted using the methods described in: [How to: Encrypt XML Elements with X.509 Certificates](how-to-encrypt-xml-elements-with-x-509-certificates.md).</span></span>  <span data-ttu-id="dd75a-108">它将查找 <`EncryptedData`> 元素，对元素进行解密，然后将元素替换为原始纯文本 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="dd75a-108">It finds an <`EncryptedData`> element, decrypts the element, and then replaces the element with the original plaintext XML element.</span></span>  
  
<span data-ttu-id="dd75a-109">此过程中的代码示例将使用当前用户帐户的本地证书存储中的 X.509 证书来解密 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="dd75a-109">The code example in this procedure decrypts an XML element using an X.509 certificate from the local certificate store of the current user account.</span></span>  <span data-ttu-id="dd75a-110">该示例使用 <xref:System.Security.Cryptography.Xml.EncryptedXml.DecryptDocument%2A> 方法自动检索 x.509 证书，并对存储在 `EncryptedKey` <> 元素的 <> 元素中的会话密钥进行解密 `EncryptedData` 。</span><span class="sxs-lookup"><span data-stu-id="dd75a-110">The example uses the <xref:System.Security.Cryptography.Xml.EncryptedXml.DecryptDocument%2A> method to automatically retrieve the X.509 certificate and decrypt a session key stored in the <`EncryptedKey`> element of the <`EncryptedData`> element.</span></span>  <span data-ttu-id="dd75a-111">然后，<xref:System.Security.Cryptography.Xml.EncryptedXml.DecryptDocument%2A> 方法将自动使用会话密钥对 XML 元素进行解密。</span><span class="sxs-lookup"><span data-stu-id="dd75a-111">The <xref:System.Security.Cryptography.Xml.EncryptedXml.DecryptDocument%2A> method then automatically uses the session key to decrypt the XML element.</span></span>  
  
<span data-ttu-id="dd75a-112">此示例适用于以下情况：多个应用程序需要共享加密数据，或应用程序需要保存它各次运行之间的加密数据。</span><span class="sxs-lookup"><span data-stu-id="dd75a-112">This example is appropriate for situations where multiple applications need to share encrypted data or where an application needs to save encrypted data between the times that it runs.</span></span>  
  
### <a name="to-decrypt-an-xml-element-with-an-x509-certificate"></a><span data-ttu-id="dd75a-113">用 X.509 证书解密 XML 元素</span><span class="sxs-lookup"><span data-stu-id="dd75a-113">To decrypt an XML element with an X.509 certificate</span></span>  
  
1. <span data-ttu-id="dd75a-114">通过从磁盘加载 XML 文件来创建 <xref:System.Xml.XmlDocument> 对象。</span><span class="sxs-lookup"><span data-stu-id="dd75a-114">Create an <xref:System.Xml.XmlDocument> object by loading an XML file from disk.</span></span>  <span data-ttu-id="dd75a-115"><xref:System.Xml.XmlDocument> 对象包含要解密的 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="dd75a-115">The <xref:System.Xml.XmlDocument> object contains the XML element to decrypt.</span></span>  
  
     [!code-csharp[HowToDecryptXMLElementX509#2](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToDecryptXMLElementX509/cs/sample.cs#2)]
     [!code-vb[HowToDecryptXMLElementX509#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToDecryptXMLElementX509/vb/sample.vb#2)]  
  
2. <span data-ttu-id="dd75a-116">通过将 <xref:System.Xml.XmlDocument> 对象传递给构造函数，创建一个新的 <xref:System.Security.Cryptography.Xml.EncryptedXml> 对象。</span><span class="sxs-lookup"><span data-stu-id="dd75a-116">Create a new <xref:System.Security.Cryptography.Xml.EncryptedXml> object by passing the <xref:System.Xml.XmlDocument> object to the constructor.</span></span>  
  
     [!code-csharp[HowToDecryptXMLElementX509#3](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToDecryptXMLElementX509/cs/sample.cs#3)]
     [!code-vb[HowToDecryptXMLElementX509#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToDecryptXMLElementX509/vb/sample.vb#3)]  
  
3. <span data-ttu-id="dd75a-117">使用 <xref:System.Security.Cryptography.Xml.EncryptedXml.DecryptDocument%2A> 方法解密 XML 文档。</span><span class="sxs-lookup"><span data-stu-id="dd75a-117">Decrypt the XML document using the <xref:System.Security.Cryptography.Xml.EncryptedXml.DecryptDocument%2A> method.</span></span>  
  
     [!code-csharp[HowToDecryptXMLElementX509#4](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToDecryptXMLElementX509/cs/sample.cs#4)]
     [!code-vb[HowToDecryptXMLElementX509#4](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToDecryptXMLElementX509/vb/sample.vb#4)]  
  
4. <span data-ttu-id="dd75a-118">保存 <xref:System.Xml.XmlDocument> 对象。</span><span class="sxs-lookup"><span data-stu-id="dd75a-118">Save the <xref:System.Xml.XmlDocument> object.</span></span>  
  
     [!code-csharp[HowToDecryptXMLElementX509#5](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToDecryptXMLElementX509/cs/sample.cs#5)]
     [!code-vb[HowToDecryptXMLElementX509#5](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToDecryptXMLElementX509/vb/sample.vb#5)]  
  
## <a name="example"></a><span data-ttu-id="dd75a-119">示例</span><span class="sxs-lookup"><span data-stu-id="dd75a-119">Example</span></span>

<span data-ttu-id="dd75a-120">此示例假定名为 `"test.xml"` 的文件与已编译程序存在于同一目录中。</span><span class="sxs-lookup"><span data-stu-id="dd75a-120">This example assumes that a file named `"test.xml"` exists in the same directory as the compiled program.</span></span>  <span data-ttu-id="dd75a-121">它还假定 `"test.xml"` 包含 `"creditcard"` 元素。</span><span class="sxs-lookup"><span data-stu-id="dd75a-121">It also assumes that `"test.xml"` contains a `"creditcard"` element.</span></span>  <span data-ttu-id="dd75a-122">可以将以下 XML 放在名为 `test.xml` 的文件，并将其用于以下示例。</span><span class="sxs-lookup"><span data-stu-id="dd75a-122">You can place the following XML into a file called `test.xml` and use it with this example.</span></span>  
  
```xml  
<root>  
    <creditcard>  
        <number>19834209</number>  
        <expiry>02/02/2002</expiry>  
    </creditcard>  
</root>  
```  
  
[!code-csharp[HowToDecryptXMLElementX509#1](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToDecryptXMLElementX509/cs/sample.cs#1)]
[!code-vb[HowToDecryptXMLElementX509#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToDecryptXMLElementX509/vb/sample.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="dd75a-123">编译代码</span><span class="sxs-lookup"><span data-stu-id="dd75a-123">Compiling the Code</span></span>  
  
- <span data-ttu-id="dd75a-124">在面向 .NET Framework 的项目中，包含对的引用 `System.Security.dll` 。</span><span class="sxs-lookup"><span data-stu-id="dd75a-124">In a project that targets .NET Framework, include a reference to `System.Security.dll`.</span></span>

- <span data-ttu-id="dd75a-125">在面向 .NET Core 或 .NET 5 的项目中，安装 NuGet 包 [System.Security.Cryptography.Xml](https://www.nuget.org/packages/System.Security.Cryptography.Xml)。</span><span class="sxs-lookup"><span data-stu-id="dd75a-125">In a project that targets .NET Core or .NET 5, install NuGet package [System.Security.Cryptography.Xml](https://www.nuget.org/packages/System.Security.Cryptography.Xml).</span></span>

- <span data-ttu-id="dd75a-126">包括以下命名空间：<xref:System.Xml>、<xref:System.Security.Cryptography> 和 <xref:System.Security.Cryptography.Xml>。</span><span class="sxs-lookup"><span data-stu-id="dd75a-126">Include the following namespaces: <xref:System.Xml>, <xref:System.Security.Cryptography>, and <xref:System.Security.Cryptography.Xml>.</span></span>  
  
## <a name="net-security"></a><span data-ttu-id="dd75a-127">.NET 安全性</span><span class="sxs-lookup"><span data-stu-id="dd75a-127">.NET Security</span></span>

<span data-ttu-id="dd75a-128">此示例中使用的 X.509 证书仅用于测试目的。</span><span class="sxs-lookup"><span data-stu-id="dd75a-128">The X.509 certificate used in this example is for test purposes only.</span></span>  <span data-ttu-id="dd75a-129">应用程序应使用由受信任的证书颁发机构生成的 x.509 证书。</span><span class="sxs-lookup"><span data-stu-id="dd75a-129">Applications should use an X.509 certificate generated by a trusted certificate authority.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd75a-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="dd75a-130">See also</span></span>

- [<span data-ttu-id="dd75a-131">加密模型</span><span class="sxs-lookup"><span data-stu-id="dd75a-131">Cryptography Model</span></span>](cryptography-model.md)
- [<span data-ttu-id="dd75a-132">加密服务</span><span class="sxs-lookup"><span data-stu-id="dd75a-132">Cryptographic Services</span></span>](cryptographic-services.md)
- [<span data-ttu-id="dd75a-133">跨平台加密</span><span class="sxs-lookup"><span data-stu-id="dd75a-133">Cross-Platform Cryptography</span></span>](cross-platform-cryptography.md)
- <xref:System.Security.Cryptography.Xml>
- [<span data-ttu-id="dd75a-134">如何：使用 X.509 证书加密 XML 元素</span><span class="sxs-lookup"><span data-stu-id="dd75a-134">How to: Encrypt XML Elements with X.509 Certificates</span></span>](how-to-encrypt-xml-elements-with-x-509-certificates.md)
- [<span data-ttu-id="dd75a-135">ASP.NET Core 数据保护</span><span class="sxs-lookup"><span data-stu-id="dd75a-135">ASP.NET Core Data Protection</span></span>](/aspnet/core/security/data-protection/introduction)
