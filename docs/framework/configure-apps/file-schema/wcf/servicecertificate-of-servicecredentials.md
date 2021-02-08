---
description: 了解详细 <serviceCertificate> 信息： <serviceCredentials>
title: <serviceCertificate> 的 <serviceCredentials>
ms.date: 03/30/2017
ms.assetid: 597ae6d5-4938-4950-9f5e-b2280e816182
ms.openlocfilehash: ab52f27949168562ec0cab0433c95843a7c312d0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786728"
---
# <a name="servicecertificate-of-servicecredentials"></a><span data-ttu-id="b3e0d-103">\<serviceCertificate> 的 \<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="b3e0d-103">\<serviceCertificate> of \<serviceCredentials></span></span>

<span data-ttu-id="b3e0d-104">指定一个 X.509 证书，以供服务用来向使用 Message 安全模式的客户端证明自己的身份。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-104">Specify an X.509 certificate that will be used to authenticate the service to clients using Message security mode.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceCredentials>**](servicecredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<serviceCertificate>**  
  
## <a name="syntax"></a><span data-ttu-id="b3e0d-105">语法</span><span class="sxs-lookup"><span data-stu-id="b3e0d-105">Syntax</span></span>  
  
```xml  
<serviceCertificate findValue="String"
                    storeLocation="LocalMachine/CurrentUser"
                    storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                    x509FindType="FindByThumbprint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b3e0d-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="b3e0d-106">Attributes and Elements</span></span>  

 <span data-ttu-id="b3e0d-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b3e0d-108">特性</span><span class="sxs-lookup"><span data-stu-id="b3e0d-108">Attributes</span></span>  
  
|<span data-ttu-id="b3e0d-109">属性</span><span class="sxs-lookup"><span data-stu-id="b3e0d-109">Attribute</span></span>|<span data-ttu-id="b3e0d-110">说明</span><span class="sxs-lookup"><span data-stu-id="b3e0d-110">Description</span></span>|  
|---------------|-----------------|  
|`findValue`|<span data-ttu-id="b3e0d-111">一个字符串，包含要在 X.509 证书存储中搜索的值。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-111">A string that contains the value to search for in the X.509 certificate store.</span></span> <span data-ttu-id="b3e0d-112">此属性中包含的类型必须满足指定 X509FindType 的需求。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-112">The type contained in the attribute must satisfy the requirements of the specified X509FindType.</span></span> <span data-ttu-id="b3e0d-113">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-113">The default is an empty string.</span></span>|  
|`storeLocation`|<span data-ttu-id="b3e0d-114">指定客户端可用于验证服务器证书的 X.509 证书存储的位置。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-114">Specifies the location of the X.509 certificate store that the client uses to validate the server’s certificate against.</span></span> <span data-ttu-id="b3e0d-115">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="b3e0d-115">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="b3e0d-116">-LocalMachine：分配给本地计算机的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-116">-   LocalMachine: the certificate store assigned to the local machine.</span></span><br /><span data-ttu-id="b3e0d-117">-CurrentUser：分配给当前用户的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-117">-   CurrentUser: the certificate store assigned to the current user.</span></span><br /><br /> <span data-ttu-id="b3e0d-118">默认值为 LocalMachine。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-118">The default is LocalMachine.</span></span>|  
|`storeName`|<span data-ttu-id="b3e0d-119">指定要打开的 X.509 证书存储区的名称。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-119">Specifies the name of the X.509 certificate store to open.</span></span> <span data-ttu-id="b3e0d-120">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="b3e0d-120">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="b3e0d-121">-通讯簿：其他用户的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-121">-   AddressBook: Certificate store for other users.</span></span><br /><span data-ttu-id="b3e0d-122">-AuthRoot：第三方证书颁发机构的证书存储 (Ca) 。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-122">-   AuthRoot: Certificate store for third-party certification authorities (CAs).</span></span><br /><span data-ttu-id="b3e0d-123">-CertificatAuthority：用于中间证书颁发机构的证书存储 (Ca) 。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-123">-   CertificatAuthority: Certificate store for intermediate certification authorities (CAs).</span></span><br /><span data-ttu-id="b3e0d-124">-不允许：吊销的证书的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-124">-   Disallowed: Certificate store for revoked certificates.</span></span><br /><span data-ttu-id="b3e0d-125">-My：个人证书的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-125">-   My: Certificate store for personal certificates.</span></span><br /><span data-ttu-id="b3e0d-126">-Root：受信任的根证书颁发机构的证书存储 (Ca) 。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-126">-   Root: Certificate store for trusted root certification authorities (CAs).</span></span><br /><span data-ttu-id="b3e0d-127">-TrustedPeople：直接受信任的人和资源的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-127">-   TrustedPeople: Certificate store for directly trusted people and resources.</span></span><br /><span data-ttu-id="b3e0d-128">-TrustedPublisher：直接受信任的发布者的证书存储区。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-128">-   TrustedPublisher: Certificate store for directly trusted publishers.</span></span><br /><br /> <span data-ttu-id="b3e0d-129">默认值为 My。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-129">The default is My.</span></span>|  
|`x509FindType`|<span data-ttu-id="b3e0d-130">定义要执行的 X.509 搜索的类型。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-130">Defines the type of X.509 search to be executed.</span></span> <span data-ttu-id="b3e0d-131">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="b3e0d-131">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="b3e0d-132">-FindByThumbprint</span><span class="sxs-lookup"><span data-stu-id="b3e0d-132">-   FindByThumbprint</span></span><br /><span data-ttu-id="b3e0d-133">-Findbysubjectname) </span><span class="sxs-lookup"><span data-stu-id="b3e0d-133">-   FindBySubjectName</span></span><br /><span data-ttu-id="b3e0d-134">-FindBySubjectDistinguishedName</span><span class="sxs-lookup"><span data-stu-id="b3e0d-134">-   FindBySubjectDistinguishedName</span></span><br /><span data-ttu-id="b3e0d-135">- FindByIssuerName</span><span class="sxs-lookup"><span data-stu-id="b3e0d-135">-   FindByIssuerName</span></span><br /><span data-ttu-id="b3e0d-136">- FindByIssuerDistinguishedName</span><span class="sxs-lookup"><span data-stu-id="b3e0d-136">-   FindByIssuerDistinguishedName</span></span><br /><span data-ttu-id="b3e0d-137">-FindBySerialNumber</span><span class="sxs-lookup"><span data-stu-id="b3e0d-137">-   FindBySerialNumber</span></span><br /><span data-ttu-id="b3e0d-138">- FindByTimeValid</span><span class="sxs-lookup"><span data-stu-id="b3e0d-138">-   FindByTimeValid</span></span><br /><span data-ttu-id="b3e0d-139">- FindByTimeNotYetValid</span><span class="sxs-lookup"><span data-stu-id="b3e0d-139">-   FindByTimeNotYetValid</span></span><br /><span data-ttu-id="b3e0d-140">- FindByTemplateName</span><span class="sxs-lookup"><span data-stu-id="b3e0d-140">-   FindByTemplateName</span></span><br /><span data-ttu-id="b3e0d-141">- FindByApplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="b3e0d-141">-   FindByApplicationPolicy</span></span><br /><span data-ttu-id="b3e0d-142">- FindByCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b3e0d-142">-   FindByCertificatePolicy</span></span><br /><span data-ttu-id="b3e0d-143">- FindByExtension</span><span class="sxs-lookup"><span data-stu-id="b3e0d-143">-   FindByExtension</span></span><br /><span data-ttu-id="b3e0d-144">- FindByKeyUsage</span><span class="sxs-lookup"><span data-stu-id="b3e0d-144">-   FindByKeyUsage</span></span><br /><span data-ttu-id="b3e0d-145">- FindBySubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="b3e0d-145">-   FindBySubjectKeyIdentifier</span></span><br /><br /> <span data-ttu-id="b3e0d-146">`findValue` 属性中包含的类型必须满足指定 X509FindType 的要求。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-146">The type contained in the `findValue` attribute must satisfy the requirements of the specified X509FindType.</span></span><br /><br /> <span data-ttu-id="b3e0d-147">默认值为 FindBySubjectDistinguishedName。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-147">The default value is FindBySubjectDistinguishedName.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b3e0d-148">子元素</span><span class="sxs-lookup"><span data-stu-id="b3e0d-148">Child Elements</span></span>  

 <span data-ttu-id="b3e0d-149">无</span><span class="sxs-lookup"><span data-stu-id="b3e0d-149">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b3e0d-150">父元素</span><span class="sxs-lookup"><span data-stu-id="b3e0d-150">Parent Elements</span></span>  
  
|<span data-ttu-id="b3e0d-151">元素</span><span class="sxs-lookup"><span data-stu-id="b3e0d-151">Element</span></span>|<span data-ttu-id="b3e0d-152">说明</span><span class="sxs-lookup"><span data-stu-id="b3e0d-152">Description</span></span>|  
|-------------|-----------------|  
|[\<serviceCredentials>](servicecredentials.md)|<span data-ttu-id="b3e0d-153">指定要用于对服务进行身份验证的凭据以及与客户端凭据验证相关的设置。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-153">Specifies the credential to be used in authenticating the service, and the client credential validation related settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b3e0d-154">备注</span><span class="sxs-lookup"><span data-stu-id="b3e0d-154">Remarks</span></span>  

 <span data-ttu-id="b3e0d-155">使用此元素可指定一个 X.509 证书，以供服务用来向使用 Message 安全模式的客户端证明自己的身份。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-155">Use this element to specify an X.509 certificate that will be used to authenticate the service to clients using Message security mode.</span></span> <span data-ttu-id="b3e0d-156">如果您使用的是将会定期续订的证书，则证书的指纹将会变更。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-156">If you are using a certificate that will be periodically renewed, then its thumbprint will change.</span></span> <span data-ttu-id="b3e0d-157">在此情况下，请使用主题名称作为 `x509FindType`，因为可以使用同一主题名称来重新颁发该证书。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-157">In that case, use the subject name as the `x509FindType` because the certificate can be reissued with the same subject name.</span></span>  
  
 <span data-ttu-id="b3e0d-158">有关使用元素的详细信息，请参阅 [如何：指定客户端凭据值](../../../wcf/how-to-specify-client-credential-values.md)。</span><span class="sxs-lookup"><span data-stu-id="b3e0d-158">For more information about using the element, see [How to: Specify Client Credential Values](../../../wcf/how-to-specify-client-credential-values.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3e0d-159">请参阅</span><span class="sxs-lookup"><span data-stu-id="b3e0d-159">See also</span></span>

- <xref:System.ServiceModel.Configuration.X509RecipientCertificateServiceElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.ServiceCertificate%2A>
- <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential>
- <xref:System.ServiceModel.Description.ServiceCredentials.ServiceCertificate%2A>
- [<span data-ttu-id="b3e0d-160">如何：指定客户端凭据值</span><span class="sxs-lookup"><span data-stu-id="b3e0d-160">How to: Specify Client Credential Values</span></span>](../../../wcf/how-to-specify-client-credential-values.md)
- [<span data-ttu-id="b3e0d-161">安全行为</span><span class="sxs-lookup"><span data-stu-id="b3e0d-161">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)
