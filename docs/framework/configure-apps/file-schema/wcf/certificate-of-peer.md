---
description: 了解详细 <certificate> 信息： <peer>
title: <certificate> 的 <peer>
ms.date: 03/30/2017
ms.assetid: 48b69142-c957-4305-a042-c9d0c9a55c0e
ms.openlocfilehash: e48a96a3f1fa486b19289584ae0c059eb5b7048d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639050"
---
# <a name="certificate-of-peer"></a><span data-ttu-id="a6cd8-103">\<certificate> 的 \<peer></span><span class="sxs-lookup"><span data-stu-id="a6cd8-103">\<certificate> of \<peer></span></span>

<span data-ttu-id="a6cd8-104">指定对等方使用的证书。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-104">Specifies a certificate used by a peer.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceCredentials>**](servicecredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<peer>**](peer-of-servicecredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<certificate>**  
  
## <a name="syntax"></a><span data-ttu-id="a6cd8-105">语法</span><span class="sxs-lookup"><span data-stu-id="a6cd8-105">Syntax</span></span>  
  
```xml  
<certificate findValue = "String"
             storeLocation = "CurrentUser/LocalMachine"
             storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
             X509FindType="FindByThumbPrint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a6cd8-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="a6cd8-106">Attributes and Elements</span></span>  

 <span data-ttu-id="a6cd8-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a6cd8-108">特性</span><span class="sxs-lookup"><span data-stu-id="a6cd8-108">Attributes</span></span>  
  
|<span data-ttu-id="a6cd8-109">属性</span><span class="sxs-lookup"><span data-stu-id="a6cd8-109">Attribute</span></span>|<span data-ttu-id="a6cd8-110">说明</span><span class="sxs-lookup"><span data-stu-id="a6cd8-110">Description</span></span>|  
|---------------|-----------------|  
|`findValue`|<span data-ttu-id="a6cd8-111">一个字符串，包含要在 X.509 证书存储中搜索的值。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-111">A string that contains the value to search for in the X.509 certificate store.</span></span> <span data-ttu-id="a6cd8-112">此属性中包含的类型必须满足指定 `x509FindType` 的要求。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-112">The type contained in the attribute must satisfy the requirements of the specified `x509FindType`.</span></span> <span data-ttu-id="a6cd8-113">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-113">The default is an empty string.</span></span>|  
|`storeLocation`|<span data-ttu-id="a6cd8-114">指定客户端可用于验证对等方的证书的 X.509 证书存储的位置。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-114">Specifies the location of the X.509 certificate store that the client uses to validate the peer's certificate against.</span></span> <span data-ttu-id="a6cd8-115">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="a6cd8-115">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="a6cd8-116">-LocalMachine：分配给本地计算机的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-116">-   LocalMachine: the certificate store assigned to the local machine.</span></span><br /><span data-ttu-id="a6cd8-117">-CurrentUser：分配给当前用户的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-117">-   CurrentUser: the certificate store assigned to the current user.</span></span><br /><br /> <span data-ttu-id="a6cd8-118">默认值为 LocalMachine。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-118">The default is LocalMachine.</span></span>|  
|`storeName`|<span data-ttu-id="a6cd8-119">指定要打开的 X.509 证书存储区的名称。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-119">Specifies the name of the X.509 certificate store to open.</span></span> <span data-ttu-id="a6cd8-120">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="a6cd8-120">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="a6cd8-121">-通讯簿：其他用户的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-121">-   AddressBook: Certificate store for other users.</span></span><br /><span data-ttu-id="a6cd8-122">-AuthRoot：第三方证书颁发机构的证书存储 (Ca) 。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-122">-   AuthRoot: Certificate store for third-party certificate authorities (CAs).</span></span><br /><span data-ttu-id="a6cd8-123">-CertificateAuthority：用于中间证书颁发机构的证书存储 (Ca) 。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-123">-   CertificateAuthority: Certificate store for intermediate certificate authorities (CAs).</span></span><br /><span data-ttu-id="a6cd8-124">-不允许：吊销的证书的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-124">-   Disallowed: Certificate store for revoked certificates.</span></span><br /><span data-ttu-id="a6cd8-125">-My：个人证书的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-125">-   My: Certificate store for personal certificates.</span></span><br /><span data-ttu-id="a6cd8-126">-Root：受信任的根证书颁发机构的证书存储 (Ca) 。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-126">-   Root: Certificate store for trusted root certificate authorities (CAs).</span></span><br /><span data-ttu-id="a6cd8-127">-TrustedPeople：直接受信任的人和资源的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-127">-   TrustedPeople: Certificate store for directly-trusted people and resources.</span></span><br /><span data-ttu-id="a6cd8-128">-TrustedPublisher：直接受信任的发布者的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-128">-   TrustedPublisher: Certificate store for directly-trusted publishers.</span></span><br /><br /> <span data-ttu-id="a6cd8-129">默认值为 My。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-129">The default is My.</span></span>|  
|`X509FindType`|<span data-ttu-id="a6cd8-130">定义要执行的 X.509 搜索的类型。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-130">Defines the type of X.509 search to be executed.</span></span> <span data-ttu-id="a6cd8-131">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="a6cd8-131">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="a6cd8-132">-FindByThumbPrint</span><span class="sxs-lookup"><span data-stu-id="a6cd8-132">-   FindByThumbPrint</span></span><br /><span data-ttu-id="a6cd8-133">-Findbysubjectname) </span><span class="sxs-lookup"><span data-stu-id="a6cd8-133">-   FindBySubjectName</span></span><br /><span data-ttu-id="a6cd8-134">-FindBySubjectDistinguishedName</span><span class="sxs-lookup"><span data-stu-id="a6cd8-134">-   FindBySubjectDistinguishedName</span></span><br /><span data-ttu-id="a6cd8-135">- FindByIssuerName</span><span class="sxs-lookup"><span data-stu-id="a6cd8-135">-   FindByIssuerName</span></span><br /><span data-ttu-id="a6cd8-136">- FindByIssuerDistinguishedName</span><span class="sxs-lookup"><span data-stu-id="a6cd8-136">-   FindByIssuerDistinguishedName</span></span><br /><span data-ttu-id="a6cd8-137">-FindBySerialNumber</span><span class="sxs-lookup"><span data-stu-id="a6cd8-137">-   FindBySerialNumber</span></span><br /><span data-ttu-id="a6cd8-138">- FindByTimeValid</span><span class="sxs-lookup"><span data-stu-id="a6cd8-138">-   FindByTimeValid</span></span><br /><span data-ttu-id="a6cd8-139">- FindByTimeNotYetValid</span><span class="sxs-lookup"><span data-stu-id="a6cd8-139">-   FindByTimeNotYetValid</span></span><br /><span data-ttu-id="a6cd8-140">- FindByTemplateName</span><span class="sxs-lookup"><span data-stu-id="a6cd8-140">-   FindByTemplateName</span></span><br /><span data-ttu-id="a6cd8-141">- FindByApplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a6cd8-141">-   FindByApplicationPolicy</span></span><br /><span data-ttu-id="a6cd8-142">- FindByCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a6cd8-142">-   FindByCertificatePolicy</span></span><br /><span data-ttu-id="a6cd8-143">- FindByExtension</span><span class="sxs-lookup"><span data-stu-id="a6cd8-143">-   FindByExtension</span></span><br /><span data-ttu-id="a6cd8-144">- FindByKeyUsage</span><span class="sxs-lookup"><span data-stu-id="a6cd8-144">-   FindByKeyUsage</span></span><br /><span data-ttu-id="a6cd8-145">- FindBySubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="a6cd8-145">-   FindBySubjectKeyIdentifier</span></span><br /><br /> <span data-ttu-id="a6cd8-146">`findValue` 属性中包含的类型必须满足指定 `X509FindType` 的要求。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-146">The type contained in the `findValue` attribute must satisfy the requirements of the specified `X509FindType`.</span></span><br /><br /> <span data-ttu-id="a6cd8-147">默认值为 FindBySubjectDistinguishedName。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-147">The default value is FindBySubjectDistinguishedName.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a6cd8-148">子元素</span><span class="sxs-lookup"><span data-stu-id="a6cd8-148">Child Elements</span></span>  

 <span data-ttu-id="a6cd8-149">无。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-149">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a6cd8-150">父元素</span><span class="sxs-lookup"><span data-stu-id="a6cd8-150">Parent Elements</span></span>  
  
|<span data-ttu-id="a6cd8-151">元素</span><span class="sxs-lookup"><span data-stu-id="a6cd8-151">Element</span></span>|<span data-ttu-id="a6cd8-152">说明</span><span class="sxs-lookup"><span data-stu-id="a6cd8-152">Description</span></span>|  
|-------------|-----------------|  
|[\<peer>](peer-of-servicecredentials.md)|<span data-ttu-id="a6cd8-153">指定对等节点的当前凭据。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-153">Specifies the current credentials for a peer node.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a6cd8-154">备注</span><span class="sxs-lookup"><span data-stu-id="a6cd8-154">Remarks</span></span>  

 <span data-ttu-id="a6cd8-155">此配置元素包含对对等网格中的邻居进行身份验证时使用的 `X509Certificate2` 实例。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-155">This configuration element contains an `X509Certificate2` instance used when authenticating neighbors in the peer mesh.</span></span>  
  
 <span data-ttu-id="a6cd8-156">有关对等编程的详细信息，请参阅对等 [网络](../../../wcf/feature-details/peer-to-peer-networking.md)。</span><span class="sxs-lookup"><span data-stu-id="a6cd8-156">For more information about peer-to-peer programming, see [Peer-to-Peer Networking](../../../wcf/feature-details/peer-to-peer-networking.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6cd8-157">请参阅</span><span class="sxs-lookup"><span data-stu-id="a6cd8-157">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement.Certificate%2A>
- <xref:System.ServiceModel.Configuration.X509PeerCertificateElement>
- <xref:System.ServiceModel.Security.PeerCredential.Certificate%2A>
- <xref:System.ServiceModel.Security.PeerCredential>
- [<span data-ttu-id="a6cd8-158">使用证书</span><span class="sxs-lookup"><span data-stu-id="a6cd8-158">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="a6cd8-159">对等网络</span><span class="sxs-lookup"><span data-stu-id="a6cd8-159">Peer-to-Peer Networking</span></span>](../../../wcf/feature-details/peer-to-peer-networking.md)
- <span data-ttu-id="a6cd8-160">[对等通道消息身份验证](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="a6cd8-160">[Peer Channel Message Authentication](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span></span>
- <span data-ttu-id="a6cd8-161">[对等通道自定义身份验证](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="a6cd8-161">[Peer Channel Custom Authentication](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span></span>
- [<span data-ttu-id="a6cd8-162">保护对等通道应用程序</span><span class="sxs-lookup"><span data-stu-id="a6cd8-162">Securing Peer Channel Applications</span></span>](../../../wcf/feature-details/securing-peer-channel-applications.md)
- [<span data-ttu-id="a6cd8-163">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="a6cd8-163">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
