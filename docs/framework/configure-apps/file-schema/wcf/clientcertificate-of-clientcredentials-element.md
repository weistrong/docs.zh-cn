---
description: 了解有关 <clientCertificate> 元素的详细 <clientCredentials> 信息
title: <clientCertificate> of <clientCredentials> 元素
ms.date: 03/30/2017
ms.assetid: 3b3fa000-3434-4142-a178-11903bdd2c5d
ms.openlocfilehash: 4305b94e62c76436a6bce91251049b3eebd2db2c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638829"
---
# <a name="clientcertificate-of-clientcredentials-element"></a><span data-ttu-id="c325f-103">\<clientCertificate> of \<clientCredentials> 元素</span><span class="sxs-lookup"><span data-stu-id="c325f-103">\<clientCertificate> of \<clientCredentials> Element</span></span>

<span data-ttu-id="c325f-104">定义用于针对服务进行客户端身份验证的 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="c325f-104">Defines an X.509 certificate used to authenticate a client to a service.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<clientCredentials>**](clientcredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<clientCertificate>**  
  
## <a name="syntax"></a><span data-ttu-id="c325f-105">语法</span><span class="sxs-lookup"><span data-stu-id="c325f-105">Syntax</span></span>  
  
```xml  
<clientCertificate findValue="String"
                   storeLocation="LocalMachine/CurrentUser"
                   storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                   X509FindType="FindByThumbPrint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c325f-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="c325f-106">Attributes and Elements</span></span>  

 <span data-ttu-id="c325f-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c325f-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c325f-108">特性</span><span class="sxs-lookup"><span data-stu-id="c325f-108">Attributes</span></span>  
  
|<span data-ttu-id="c325f-109">属性</span><span class="sxs-lookup"><span data-stu-id="c325f-109">Attribute</span></span>|<span data-ttu-id="c325f-110">说明</span><span class="sxs-lookup"><span data-stu-id="c325f-110">Description</span></span>|  
|---------------|-----------------|  
|`findValue`|<span data-ttu-id="c325f-111">一个字符串，包含要在 X.509 证书存储中搜索的值。</span><span class="sxs-lookup"><span data-stu-id="c325f-111">A string that contains the value to search for in the X.509 certificate store.</span></span> <span data-ttu-id="c325f-112">此属性中包含的类型必须满足 `X509FindType` 属性值的要求。</span><span class="sxs-lookup"><span data-stu-id="c325f-112">The type contained in the attribute must satisfy the requirements of the `X509FindType` attribute value.</span></span> <span data-ttu-id="c325f-113">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="c325f-113">The default is an empty string.</span></span>|  
|`storeLocation`|<span data-ttu-id="c325f-114">指定客户端用于向服务验证自身身份的 X.509 证书的位置。</span><span class="sxs-lookup"><span data-stu-id="c325f-114">Specifies the location of the X.509 certificate that the client uses to authenticate itself to the service.</span></span> <span data-ttu-id="c325f-115">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="c325f-115">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="c325f-116">-LocalMachine：分配给本地计算机的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="c325f-116">-   LocalMachine: the certificate store assigned to the local machine.</span></span><br /><span data-ttu-id="c325f-117">-CurrentUser：分配给当前用户的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="c325f-117">-   CurrentUser: the certificate store assigned to the current user.</span></span><br /><br /> <span data-ttu-id="c325f-118">默认值为 LocalMachine。</span><span class="sxs-lookup"><span data-stu-id="c325f-118">The default is LocalMachine.</span></span> <span data-ttu-id="c325f-119">此属性的类型为 <xref:System.Security.Cryptography.X509Certificates.StoreLocation>。</span><span class="sxs-lookup"><span data-stu-id="c325f-119">This attribute is of type <xref:System.Security.Cryptography.X509Certificates.StoreLocation>.</span></span>|  
|`storeName`|<span data-ttu-id="c325f-120">指定要搜索的 X.509 证书存储的名称。</span><span class="sxs-lookup"><span data-stu-id="c325f-120">Specifies the name of the X.509 certificate store to search.</span></span> <span data-ttu-id="c325f-121">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="c325f-121">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="c325f-122">-通讯簿：其他用户的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="c325f-122">-   AddressBook: Certificate store for other users.</span></span><br /><span data-ttu-id="c325f-123">-AuthRoot：第三方证书颁发机构的证书存储 (Ca) 。</span><span class="sxs-lookup"><span data-stu-id="c325f-123">-   AuthRoot: Certificate store for third-party certificate authorities (CAs).</span></span><br /><span data-ttu-id="c325f-124">-CertificateAuthority：用于中间证书颁发机构的证书存储 (Ca) 。</span><span class="sxs-lookup"><span data-stu-id="c325f-124">-   CertificateAuthority: Certificate store for intermediate certificate authorities (CAs).</span></span><br /><span data-ttu-id="c325f-125">-不允许：吊销的证书的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="c325f-125">-   Disallowed: Certificate store for revoked certificates.</span></span><br /><span data-ttu-id="c325f-126">-My：个人证书的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="c325f-126">-   My: Certificate store for personal certificates.</span></span><br /><span data-ttu-id="c325f-127">-Root：受信任的根证书颁发机构的证书存储 (Ca) 。</span><span class="sxs-lookup"><span data-stu-id="c325f-127">-   Root: Certificate store for trusted root certificate authorities (CAs).</span></span><br /><span data-ttu-id="c325f-128">-TrustedPeople：直接受信任的人和资源的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="c325f-128">-   TrustedPeople: Certificate store for directly trusted people and resources.</span></span><br /><span data-ttu-id="c325f-129">-TrustedPublisher：直接受信任的发布者的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="c325f-129">-   TrustedPublisher: Certificate store for directly trusted publishers.</span></span><br /><br /> <span data-ttu-id="c325f-130">默认值为 My。</span><span class="sxs-lookup"><span data-stu-id="c325f-130">The default is My.</span></span> <span data-ttu-id="c325f-131">此属性的类型为 <xref:System.Security.Cryptography.X509Certificates.StoreName>。</span><span class="sxs-lookup"><span data-stu-id="c325f-131">This attribute is of type <xref:System.Security.Cryptography.X509Certificates.StoreName>.</span></span>|  
|<span data-ttu-id="c325f-132">X509FindType</span><span class="sxs-lookup"><span data-stu-id="c325f-132">X509FindType</span></span>|<span data-ttu-id="c325f-133">定义要执行的 X.509 搜索的类型。</span><span class="sxs-lookup"><span data-stu-id="c325f-133">Defines the type of X.509 search to be executed.</span></span> <span data-ttu-id="c325f-134">`findValue` 属性中包含的类型必须满足此属性的要求。</span><span class="sxs-lookup"><span data-stu-id="c325f-134">The type contained in the `findValue` attribute must satisfy the requirements of this attribute.</span></span> <span data-ttu-id="c325f-135">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="c325f-135">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="c325f-136">-FindByThumbPrint</span><span class="sxs-lookup"><span data-stu-id="c325f-136">-   FindByThumbPrint</span></span><br /><span data-ttu-id="c325f-137">-Findbysubjectname) </span><span class="sxs-lookup"><span data-stu-id="c325f-137">-   FindBySubjectName</span></span><br /><span data-ttu-id="c325f-138">-FindBySubjectDistinguishedName</span><span class="sxs-lookup"><span data-stu-id="c325f-138">-   FindBySubjectDistinguishedName</span></span><br /><span data-ttu-id="c325f-139">- FindByIssuerName</span><span class="sxs-lookup"><span data-stu-id="c325f-139">-   FindByIssuerName</span></span><br /><span data-ttu-id="c325f-140">- FindByIssuerDistinguishedName</span><span class="sxs-lookup"><span data-stu-id="c325f-140">-   FindByIssuerDistinguishedName</span></span><br /><span data-ttu-id="c325f-141">-FindBySerialNumber</span><span class="sxs-lookup"><span data-stu-id="c325f-141">-   FindBySerialNumber</span></span><br /><span data-ttu-id="c325f-142">- FindByTimeValid</span><span class="sxs-lookup"><span data-stu-id="c325f-142">-   FindByTimeValid</span></span><br /><span data-ttu-id="c325f-143">- FindByTimeNotYetValid</span><span class="sxs-lookup"><span data-stu-id="c325f-143">-   FindByTimeNotYetValid</span></span><br /><span data-ttu-id="c325f-144">- FindByTemplateName</span><span class="sxs-lookup"><span data-stu-id="c325f-144">-   FindByTemplateName</span></span><br /><span data-ttu-id="c325f-145">- FindByApplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="c325f-145">-   FindByApplicationPolicy</span></span><br /><span data-ttu-id="c325f-146">- FindByCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c325f-146">-   FindByCertificatePolicy</span></span><br /><span data-ttu-id="c325f-147">- FindByExtension</span><span class="sxs-lookup"><span data-stu-id="c325f-147">-   FindByExtension</span></span><br /><span data-ttu-id="c325f-148">- FindByKeyUsage</span><span class="sxs-lookup"><span data-stu-id="c325f-148">-   FindByKeyUsage</span></span><br /><span data-ttu-id="c325f-149">- FindBySubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="c325f-149">-   FindBySubjectKeyIdentifier</span></span><br /><br /> <span data-ttu-id="c325f-150">默认值为 FindBySubjectDistinguishedName。</span><span class="sxs-lookup"><span data-stu-id="c325f-150">The default value is FindBySubjectDistinguishedName.</span></span> <span data-ttu-id="c325f-151">此属性的类型为 <xref:System.Security.Cryptography.X509Certificates.X509FindType>。</span><span class="sxs-lookup"><span data-stu-id="c325f-151">This attribute is of type <xref:System.Security.Cryptography.X509Certificates.X509FindType>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c325f-152">子元素</span><span class="sxs-lookup"><span data-stu-id="c325f-152">Child Elements</span></span>  

 <span data-ttu-id="c325f-153">无。</span><span class="sxs-lookup"><span data-stu-id="c325f-153">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c325f-154">父元素</span><span class="sxs-lookup"><span data-stu-id="c325f-154">Parent Elements</span></span>  
  
|<span data-ttu-id="c325f-155">元素</span><span class="sxs-lookup"><span data-stu-id="c325f-155">Element</span></span>|<span data-ttu-id="c325f-156">说明</span><span class="sxs-lookup"><span data-stu-id="c325f-156">Description</span></span>|  
|-------------|-----------------|  
|[\<clientCredentials>](clientcredentials.md)|<span data-ttu-id="c325f-157">指定用于向服务验证客户端身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="c325f-157">Specifies the credentials used to authenticate the client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c325f-158">备注</span><span class="sxs-lookup"><span data-stu-id="c325f-158">Remarks</span></span>  

 <span data-ttu-id="c325f-159">此配置元素指定用于对具有此元素的客户端进行身份验证的证书。</span><span class="sxs-lookup"><span data-stu-id="c325f-159">This configuration element specifies the certificate used to authenticate the client with this element.</span></span> <span data-ttu-id="c325f-160">有关详细信息，请参阅 [如何：指定客户端凭据值](../../../wcf/how-to-specify-client-credential-values.md)。</span><span class="sxs-lookup"><span data-stu-id="c325f-160">For more information, see [How to: Specify Client Credential Values](../../../wcf/how-to-specify-client-credential-values.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c325f-161">请参阅</span><span class="sxs-lookup"><span data-stu-id="c325f-161">See also</span></span>

- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.ClientCertificate%2A>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Description.ClientCredentials.ClientCertificate%2A>
- <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>
- <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential>
- [<span data-ttu-id="c325f-162">安全行为</span><span class="sxs-lookup"><span data-stu-id="c325f-162">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="c325f-163">如何：指定客户端凭据值</span><span class="sxs-lookup"><span data-stu-id="c325f-163">How to: Specify Client Credential Values</span></span>](../../../wcf/how-to-specify-client-credential-values.md)
- [<span data-ttu-id="c325f-164">保证客户端的安全</span><span class="sxs-lookup"><span data-stu-id="c325f-164">Securing Clients</span></span>](../../../wcf/securing-clients.md)
- [<span data-ttu-id="c325f-165">使用证书</span><span class="sxs-lookup"><span data-stu-id="c325f-165">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="c325f-166">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="c325f-166">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
