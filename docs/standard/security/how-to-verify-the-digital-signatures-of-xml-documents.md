---
description: 了解详细信息：如何：验证 XML 文档的数字签名
title: 如何：验证 XML 文档的数字签名
ms.date: 07/14/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- System.Security.Cryptography.SignedXml class
- signatures, cryptographic
- System.Security.Cryptography.RSA class
- verifying signatures
- checking signatures
- XML digital signatures
- digital signatures, verifying
ms.assetid: a4d5ceb1-b9f5-47e8-9e4a-a2b39110002f
ms.openlocfilehash: 37ef72c6bedf73ced7c2dde4335034f603190946
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99685031"
---
# <a name="how-to-verify-the-digital-signatures-of-xml-documents"></a><span data-ttu-id="8cd70-103">如何：验证 XML 文档的数字签名</span><span class="sxs-lookup"><span data-stu-id="8cd70-103">How to: Verify the Digital Signatures of XML Documents</span></span>

<span data-ttu-id="8cd70-104">可以使用 <xref:System.Security.Cryptography.Xml> 命名空间中的类来验证签有数字签名的 XML 数据。</span><span class="sxs-lookup"><span data-stu-id="8cd70-104">You can use the classes in the <xref:System.Security.Cryptography.Xml> namespace to verify XML data signed with a digital signature.</span></span> <span data-ttu-id="8cd70-105">使用 XML 数字签名 (XMLDSIG)，你可以验证签名后的数据没有被更改。</span><span class="sxs-lookup"><span data-stu-id="8cd70-105">XML digital signatures (XMLDSIG) allow you to verify that data was not altered after it was signed.</span></span> <span data-ttu-id="8cd70-106">有关 XMLDSIG 标准的详细信息，请参阅中 (W3C) 规范的万维网联合会 <https://www.w3.org/TR/xmldsig-core/> 。</span><span class="sxs-lookup"><span data-stu-id="8cd70-106">For more information about the XMLDSIG standard, see the World Wide Web Consortium (W3C) specification at <https://www.w3.org/TR/xmldsig-core/>.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8cd70-107">本文中的代码适用于 Windows。</span><span class="sxs-lookup"><span data-stu-id="8cd70-107">The code in this article applies to Windows.</span></span>

<span data-ttu-id="8cd70-108">此过程中的代码示例演示如何验证包含在 <> 元素中的 XML 数字签名 `Signature` 。</span><span class="sxs-lookup"><span data-stu-id="8cd70-108">The code example in this procedure demonstrates how to verify an XML digital signature contained in a <`Signature`> element.</span></span>  <span data-ttu-id="8cd70-109">该示例检索密钥容器中 RSA 公钥，然后使用该密钥来验证签名。</span><span class="sxs-lookup"><span data-stu-id="8cd70-109">The example retrieves an RSA public key from a key container and then uses the key to verify the signature.</span></span>  
  
<span data-ttu-id="8cd70-110">有关如何使用此方法创建可以验证的数字签名的信息，请参阅 [如何：使用数字签名为 XML 文档签名](how-to-sign-xml-documents-with-digital-signatures.md)。</span><span class="sxs-lookup"><span data-stu-id="8cd70-110">For information about how create a digital signature that can be verified using this technique, see [How to: Sign XML Documents with Digital Signatures](how-to-sign-xml-documents-with-digital-signatures.md).</span></span>  
  
### <a name="to-verify-the-digital-signature-of-an-xml-document"></a><span data-ttu-id="8cd70-111">验证 XML 文档的数字签名</span><span class="sxs-lookup"><span data-stu-id="8cd70-111">To verify the digital signature of an XML document</span></span>  
  
1. <span data-ttu-id="8cd70-112">若要验证文档，必须使用用于签名的同一非对称密钥。</span><span class="sxs-lookup"><span data-stu-id="8cd70-112">To verify the document, you must use the same asymmetric key that was used for signing.</span></span>  <span data-ttu-id="8cd70-113">创建 <xref:System.Security.Cryptography.CspParameters> 对象，并指定用于签名的密钥容器的名称。</span><span class="sxs-lookup"><span data-stu-id="8cd70-113">Create a <xref:System.Security.Cryptography.CspParameters> object and specify the name of the key container that was used for signing.</span></span>  
  
     [!code-csharp[HowToVerifyXMLDocumentRSA#2](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/cs/sample.cs#2)]
     [!code-vb[HowToVerifyXMLDocumentRSA#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/vb/sample.vb#2)]  
  
2. <span data-ttu-id="8cd70-114">检索使用 <xref:System.Security.Cryptography.RSACryptoServiceProvider> 类的公钥。</span><span class="sxs-lookup"><span data-stu-id="8cd70-114">Retrieve the public key using the <xref:System.Security.Cryptography.RSACryptoServiceProvider> class.</span></span>  <span data-ttu-id="8cd70-115">当将 <xref:System.Security.Cryptography.CspParameters> 对象传递到 <xref:System.Security.Cryptography.RSACryptoServiceProvider> 类的构造函数中时，会按名称从密钥容器自动加载密钥。</span><span class="sxs-lookup"><span data-stu-id="8cd70-115">The key is automatically loaded from the key container by name when you pass the <xref:System.Security.Cryptography.CspParameters> object to the constructor of the <xref:System.Security.Cryptography.RSACryptoServiceProvider> class.</span></span>  
  
     [!code-csharp[HowToVerifyXMLDocumentRSA#3](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/cs/sample.cs#3)]
     [!code-vb[HowToVerifyXMLDocumentRSA#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/vb/sample.vb#3)]  
  
3. <span data-ttu-id="8cd70-116">通过从磁盘加载 XML 文件来创建 <xref:System.Xml.XmlDocument> 对象。</span><span class="sxs-lookup"><span data-stu-id="8cd70-116">Create an <xref:System.Xml.XmlDocument> object by loading an XML file from disk.</span></span>  <span data-ttu-id="8cd70-117"><xref:System.Xml.XmlDocument> 对象包含要验证的已签名 XML 文档。</span><span class="sxs-lookup"><span data-stu-id="8cd70-117">The <xref:System.Xml.XmlDocument> object contains the signed XML document to verify.</span></span>  
  
     [!code-csharp[HowToVerifyXMLDocumentRSA#4](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/cs/sample.cs#4)]
     [!code-vb[HowToVerifyXMLDocumentRSA#4](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/vb/sample.vb#4)]  
  
4. <span data-ttu-id="8cd70-118">创建一个新的 <xref:System.Security.Cryptography.Xml.SignedXml> 对象，并向其传递 <xref:System.Xml.XmlDocument> 对象。</span><span class="sxs-lookup"><span data-stu-id="8cd70-118">Create a new <xref:System.Security.Cryptography.Xml.SignedXml> object and pass the <xref:System.Xml.XmlDocument> object to it.</span></span>  
  
     [!code-csharp[HowToVerifyXMLDocumentRSA#5](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/cs/sample.cs#5)]
     [!code-vb[HowToVerifyXMLDocumentRSA#5](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/vb/sample.vb#5)]  
  
5. <span data-ttu-id="8cd70-119">查找 <`signature`> 元素并创建一个新的 <xref:System.Xml.XmlNodeList> 对象。</span><span class="sxs-lookup"><span data-stu-id="8cd70-119">Find the <`signature`> element and create a new <xref:System.Xml.XmlNodeList> object.</span></span>  
  
     [!code-csharp[HowToVerifyXMLDocumentRSA#6](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/cs/sample.cs#6)]
     [!code-vb[HowToVerifyXMLDocumentRSA#6](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/vb/sample.vb#6)]  
  
6. <span data-ttu-id="8cd70-120">将第一个 <> 元素的 XML 加载 `signature` 到 <xref:System.Security.Cryptography.Xml.SignedXml> 对象。</span><span class="sxs-lookup"><span data-stu-id="8cd70-120">Load the XML of the first <`signature`> element into the <xref:System.Security.Cryptography.Xml.SignedXml> object.</span></span>  
  
     [!code-csharp[HowToVerifyXMLDocumentRSA#7](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/cs/sample.cs#7)]
     [!code-vb[HowToVerifyXMLDocumentRSA#7](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/vb/sample.vb#7)]  
  
7. <span data-ttu-id="8cd70-121">使用 <xref:System.Security.Cryptography.Xml.SignedXml.CheckSignature%2A> 方法和 RSA 公钥检查签名。</span><span class="sxs-lookup"><span data-stu-id="8cd70-121">Check the signature using the <xref:System.Security.Cryptography.Xml.SignedXml.CheckSignature%2A> method and the RSA public key.</span></span>  <span data-ttu-id="8cd70-122">此方法返回一个指示成功或失败的布尔值。</span><span class="sxs-lookup"><span data-stu-id="8cd70-122">This method returns a Boolean value that indicates success or failure.</span></span>  
  
     [!code-csharp[HowToVerifyXMLDocumentRSA#8](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/cs/sample.cs#8)]
     [!code-vb[HowToVerifyXMLDocumentRSA#8](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/vb/sample.vb#8)]  
  
## <a name="example"></a><span data-ttu-id="8cd70-123">示例</span><span class="sxs-lookup"><span data-stu-id="8cd70-123">Example</span></span>

<span data-ttu-id="8cd70-124">此示例假定名为 `"test.xml"` 的文件与已编译程序存在于同一目录中。</span><span class="sxs-lookup"><span data-stu-id="8cd70-124">This example assumes that a file named `"test.xml"` exists in the same directory as the compiled program.</span></span>  <span data-ttu-id="8cd70-125">`"test.xml"`必须使用[如何：使用数字签名为 XML 文档签名](how-to-sign-xml-documents-with-digital-signatures.md)中所述的技术对文件进行签名。</span><span class="sxs-lookup"><span data-stu-id="8cd70-125">The `"test.xml"` file must be signed using the techniques described in [How to: Sign XML Documents with Digital Signatures](how-to-sign-xml-documents-with-digital-signatures.md).</span></span>  
  
[!code-csharp[HowToVerifyXMLDocumentRSA#1](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/cs/sample.cs#1)]
[!code-vb[HowToVerifyXMLDocumentRSA#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToVerifyXMLDocumentRSA/vb/sample.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="8cd70-126">编译代码</span><span class="sxs-lookup"><span data-stu-id="8cd70-126">Compiling the Code</span></span>  
  
- <span data-ttu-id="8cd70-127">在面向 .NET Framework 的项目中，包含对的引用 `System.Security.dll` 。</span><span class="sxs-lookup"><span data-stu-id="8cd70-127">In a project that targets .NET Framework, include a reference to `System.Security.dll`.</span></span>

- <span data-ttu-id="8cd70-128">在面向 .NET Core 或 .NET 5 的项目中，安装 NuGet 包 [System.Security.Cryptography.Xml](https://www.nuget.org/packages/System.Security.Cryptography.Xml)。</span><span class="sxs-lookup"><span data-stu-id="8cd70-128">In a project that targets .NET Core or .NET 5, install NuGet package [System.Security.Cryptography.Xml](https://www.nuget.org/packages/System.Security.Cryptography.Xml).</span></span>
  
- <span data-ttu-id="8cd70-129">包括以下命名空间：<xref:System.Xml>、<xref:System.Security.Cryptography> 和 <xref:System.Security.Cryptography.Xml>。</span><span class="sxs-lookup"><span data-stu-id="8cd70-129">Include the following namespaces: <xref:System.Xml>, <xref:System.Security.Cryptography>, and <xref:System.Security.Cryptography.Xml>.</span></span>  
  
## <a name="net-security"></a><span data-ttu-id="8cd70-130">.NET 安全性</span><span class="sxs-lookup"><span data-stu-id="8cd70-130">.NET Security</span></span>

<span data-ttu-id="8cd70-131">切勿用纯文本存储或传输非对称密钥对的私钥。</span><span class="sxs-lookup"><span data-stu-id="8cd70-131">Never store or transfer the private key of an asymmetric key pair in plaintext.</span></span>  <span data-ttu-id="8cd70-132">有关对称和非对称加密密钥的详细信息，请参阅 [生成加密和解密密钥](generating-keys-for-encryption-and-decryption.md)。</span><span class="sxs-lookup"><span data-stu-id="8cd70-132">For more information about symmetric and asymmetric cryptographic keys, see [Generating Keys for Encryption and Decryption](generating-keys-for-encryption-and-decryption.md).</span></span>  
  
<span data-ttu-id="8cd70-133">切勿将私钥直接嵌入到源代码中。</span><span class="sxs-lookup"><span data-stu-id="8cd70-133">Never embed a private key directly into your source code.</span></span>  <span data-ttu-id="8cd70-134">[Ildasm.exe 使用 (IL 拆装器) ](../../framework/tools/ildasm-exe-il-disassembler.md)或通过在文本编辑器（例如记事本）中打开程序集，可以轻松地从程序集中读取嵌入的密钥。</span><span class="sxs-lookup"><span data-stu-id="8cd70-134">Embedded keys can be easily read from an assembly using the [Ildasm.exe (IL Disassembler)](../../framework/tools/ildasm-exe-il-disassembler.md) or by opening the assembly in a text editor such as Notepad.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8cd70-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="8cd70-135">See also</span></span>

- [<span data-ttu-id="8cd70-136">加密模型</span><span class="sxs-lookup"><span data-stu-id="8cd70-136">Cryptography Model</span></span>](cryptography-model.md)
- [<span data-ttu-id="8cd70-137">加密服务</span><span class="sxs-lookup"><span data-stu-id="8cd70-137">Cryptographic Services</span></span>](cryptographic-services.md)
- [<span data-ttu-id="8cd70-138">跨平台加密</span><span class="sxs-lookup"><span data-stu-id="8cd70-138">Cross-Platform Cryptography</span></span>](cross-platform-cryptography.md)
- <xref:System.Security.Cryptography.Xml>
- [<span data-ttu-id="8cd70-139">如何：使用数字签名为 XML 文档签名</span><span class="sxs-lookup"><span data-stu-id="8cd70-139">How to: Sign XML Documents with Digital Signatures</span></span>](how-to-sign-xml-documents-with-digital-signatures.md)
- [<span data-ttu-id="8cd70-140">ASP.NET Core 数据保护</span><span class="sxs-lookup"><span data-stu-id="8cd70-140">ASP.NET Core Data Protection</span></span>](/aspnet/core/security/data-protection/introduction)
