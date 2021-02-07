---
description: 了解详细信息：如何：创建使用自定义证书验证程序的服务
title: 如何：创建使用自定义证书验证程序的服务
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF, authentication
ms.assetid: bb0190ff-0738-4e54-8d22-c97d343708bf
ms.openlocfilehash: 8ed5d23143b7b69768cc556d9fd5663e46fd7da7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99668976"
---
# <a name="how-to-create-a-service-that-employs-a-custom-certificate-validator"></a><span data-ttu-id="bc864-103">如何：创建使用自定义证书验证程序的服务</span><span class="sxs-lookup"><span data-stu-id="bc864-103">How to: Create a Service that Employs a Custom Certificate Validator</span></span>

<span data-ttu-id="bc864-104">本主题介绍如何实现自定义证书验证程序，以及如何配置客户端或服务凭据以使用自定义证书验证程序替换默认证书验证逻辑。</span><span class="sxs-lookup"><span data-stu-id="bc864-104">This topic shows how to implement a custom certificate validator and how to configure client or service credentials to replace the default certificate validation logic with the custom certificate validator.</span></span>  
  
 <span data-ttu-id="bc864-105">如果使用 x.509 证书对客户端或服务进行身份验证，Windows Communication Foundation (WCF) 默认情况下使用 Windows 证书存储和加密 API 来验证证书，并确保其受信任。</span><span class="sxs-lookup"><span data-stu-id="bc864-105">If the X.509 certificate is used to authenticate a client or service, Windows Communication Foundation (WCF) by default uses the Windows certificate store and Crypto API to validate the certificate and to ensure that it is trusted.</span></span> <span data-ttu-id="bc864-106">有时，内置证书验证功能并不足够且必须更改。</span><span class="sxs-lookup"><span data-stu-id="bc864-106">Sometimes the built-in certificate validation functionality is not enough and must be changed.</span></span> <span data-ttu-id="bc864-107">WCF 提供了一种简单的方法来通过允许用户添加自定义证书验证程序来更改验证逻辑。</span><span class="sxs-lookup"><span data-stu-id="bc864-107">WCF provides an easy way to change the validation logic by allowing users to add a custom certificate validator.</span></span> <span data-ttu-id="bc864-108">如果指定了自定义证书验证程序，则 WCF 不使用内置证书验证逻辑，而是依赖于自定义验证程序。</span><span class="sxs-lookup"><span data-stu-id="bc864-108">If a custom certificate validator is specified, WCF does not use the built-in certificate validation logic but relies on the custom validator instead.</span></span>  
  
## <a name="procedures"></a><span data-ttu-id="bc864-109">过程</span><span class="sxs-lookup"><span data-stu-id="bc864-109">Procedures</span></span>  
  
#### <a name="to-create-a-custom-certificate-validator"></a><span data-ttu-id="bc864-110">创建自定义证书验证程序</span><span class="sxs-lookup"><span data-stu-id="bc864-110">To create a custom certificate validator</span></span>  
  
1. <span data-ttu-id="bc864-111">定义一个从 <xref:System.IdentityModel.Selectors.X509CertificateValidator> 派生的新类。</span><span class="sxs-lookup"><span data-stu-id="bc864-111">Define a new class derived from <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span></span>  
  
2. <span data-ttu-id="bc864-112">实现抽象 <xref:System.IdentityModel.Selectors.X509CertificateValidator.Validate%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="bc864-112">Implement the abstract <xref:System.IdentityModel.Selectors.X509CertificateValidator.Validate%2A> method.</span></span> <span data-ttu-id="bc864-113">将必须验证的证书作为自变量传递给该方法。</span><span class="sxs-lookup"><span data-stu-id="bc864-113">The certificate that must be validated is passed as an argument to the method.</span></span> <span data-ttu-id="bc864-114">如果根据验证逻辑，传递的证书无效，则此方法引发 <xref:System.IdentityModel.Tokens.SecurityTokenValidationException>。</span><span class="sxs-lookup"><span data-stu-id="bc864-114">If the passed certificate is not valid according to the validation logic, this method throws a <xref:System.IdentityModel.Tokens.SecurityTokenValidationException>.</span></span> <span data-ttu-id="bc864-115">如果证书有效，则此方法返回到调用方。</span><span class="sxs-lookup"><span data-stu-id="bc864-115">If the certificate is valid, the method returns to the caller.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="bc864-116">若要将身份验证错误返回到客户端，应在 <xref:System.ServiceModel.FaultException> 方法中引发 <xref:System.IdentityModel.Selectors.UserNamePasswordValidator.Validate%2A>。</span><span class="sxs-lookup"><span data-stu-id="bc864-116">To return authentication errors back to the client, throw a <xref:System.ServiceModel.FaultException> in the <xref:System.IdentityModel.Selectors.UserNamePasswordValidator.Validate%2A> method.</span></span>  
  
 [!code-csharp[c_CustomCertificateValidator#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customcertificatevalidator/cs/source.cs#2)]
 [!code-vb[c_CustomCertificateValidator#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customcertificatevalidator/vb/source.vb#2)]  
  
#### <a name="to-specify-a-custom-certificate-validator-in-service-configuration"></a><span data-ttu-id="bc864-117">指定服务配置中的自定义证书验证程序</span><span class="sxs-lookup"><span data-stu-id="bc864-117">To specify a custom certificate validator in service configuration</span></span>  
  
1. <span data-ttu-id="bc864-118">将 [\<behaviors>](../../configure-apps/file-schema/wcf/behaviors.md) 元素和添加 [\<serviceBehaviors>](../../configure-apps/file-schema/wcf/servicebehaviors.md) 到 [\<system.serviceModel>](../../configure-apps/file-schema/wcf/system-servicemodel.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="bc864-118">Add a [\<behaviors>](../../configure-apps/file-schema/wcf/behaviors.md) element and a [\<serviceBehaviors>](../../configure-apps/file-schema/wcf/servicebehaviors.md) to the [\<system.serviceModel>](../../configure-apps/file-schema/wcf/system-servicemodel.md) element.</span></span>  
  
2. <span data-ttu-id="bc864-119">添加 [\<behavior>](../../configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md) ，并将 `name` 属性设置为合适的值。</span><span class="sxs-lookup"><span data-stu-id="bc864-119">Add a [\<behavior>](../../configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md) and set the `name` attribute to an appropriate value.</span></span>  
  
3. <span data-ttu-id="bc864-120">将添加 [\<serviceCredentials>](../../configure-apps/file-schema/wcf/servicecredentials.md) 到 `<behavior>` 元素。</span><span class="sxs-lookup"><span data-stu-id="bc864-120">Add a [\<serviceCredentials>](../../configure-apps/file-schema/wcf/servicecredentials.md) to the `<behavior>` element.</span></span>  
  
4. <span data-ttu-id="bc864-121">向 `<clientCertificate>` 元素中添加一个 `<serviceCredentials>` 元素。</span><span class="sxs-lookup"><span data-stu-id="bc864-121">Add a `<clientCertificate>` element to the `<serviceCredentials>` element.</span></span>  
  
5. <span data-ttu-id="bc864-122">将添加 [\<authentication>](../../configure-apps/file-schema/wcf/authentication-of-clientcertificate-element.md) 到 `<clientCertificate>` 元素。</span><span class="sxs-lookup"><span data-stu-id="bc864-122">Add an [\<authentication>](../../configure-apps/file-schema/wcf/authentication-of-clientcertificate-element.md) to the `<clientCertificate>` element.</span></span>  
  
6. <span data-ttu-id="bc864-123">将 `customCertificateValidatorType` 属性设置为验证程序类型。</span><span class="sxs-lookup"><span data-stu-id="bc864-123">Set the `customCertificateValidatorType` attribute to the validator type.</span></span> <span data-ttu-id="bc864-124">下面的示例将该属性设置为类型的命名空间和名称。</span><span class="sxs-lookup"><span data-stu-id="bc864-124">The following example sets the attribute to the namespace and name of the type.</span></span>  
  
7. <span data-ttu-id="bc864-125">将 `certificateValidationMode` 属性设置为 `Custom`。</span><span class="sxs-lookup"><span data-stu-id="bc864-125">Set the `certificateValidationMode` attribute to `Custom`.</span></span>  
  
    ```xml  
    <configuration>  
     <system.serviceModel>  
      <behaviors>  
       <serviceBehaviors>  
        <behavior name="ServiceBehavior">  
         <serviceCredentials>  
          <clientCertificate>  
          <authentication certificateValidationMode="Custom" customCertificateValidatorType="Samples.MyValidator, service" />  
          </clientCertificate>  
         </serviceCredentials>  
        </behavior>  
       </serviceBehaviors>  
      </behaviors>  
    </system.serviceModel>  
    </configuration>  
    ```  
  
#### <a name="to-specify-a-custom-certificate-validator-using-configuration-on-the-client"></a><span data-ttu-id="bc864-126">使用客户端上的配置指定自定义证书验证程序</span><span class="sxs-lookup"><span data-stu-id="bc864-126">To specify a custom certificate validator using configuration on the client</span></span>  
  
1. <span data-ttu-id="bc864-127">将 [\<behaviors>](../../configure-apps/file-schema/wcf/behaviors.md) 元素和添加 [\<serviceBehaviors>](../../configure-apps/file-schema/wcf/servicebehaviors.md) 到 [\<system.serviceModel>](../../configure-apps/file-schema/wcf/system-servicemodel.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="bc864-127">Add a [\<behaviors>](../../configure-apps/file-schema/wcf/behaviors.md) element and a [\<serviceBehaviors>](../../configure-apps/file-schema/wcf/servicebehaviors.md) to the [\<system.serviceModel>](../../configure-apps/file-schema/wcf/system-servicemodel.md) element.</span></span>  
  
2. <span data-ttu-id="bc864-128">添加 [\<endpointBehaviors>](../../configure-apps/file-schema/wcf/endpointbehaviors.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="bc864-128">Add an [\<endpointBehaviors>](../../configure-apps/file-schema/wcf/endpointbehaviors.md) element.</span></span>  
  
3. <span data-ttu-id="bc864-129">添加一个 `<behavior>` 元素，并将 `name` 属性设置为适当的值。</span><span class="sxs-lookup"><span data-stu-id="bc864-129">Add a `<behavior>` element and set the `name` attribute to an appropriate value.</span></span>  
  
4. <span data-ttu-id="bc864-130">添加 [\<clientCredentials>](../../configure-apps/file-schema/wcf/clientcredentials.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="bc864-130">Add a [\<clientCredentials>](../../configure-apps/file-schema/wcf/clientcredentials.md) element.</span></span>  
  
5. <span data-ttu-id="bc864-131">添加 [\<serviceCertificate>](../../configure-apps/file-schema/wcf/servicecertificate-of-clientcredentials-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="bc864-131">Add a [\<serviceCertificate>](../../configure-apps/file-schema/wcf/servicecertificate-of-clientcredentials-element.md).</span></span>  
  
6. <span data-ttu-id="bc864-132">添加， [\<authentication>](../../configure-apps/file-schema/wcf/authentication-of-servicecertificate-element.md) 如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="bc864-132">Add an [\<authentication>](../../configure-apps/file-schema/wcf/authentication-of-servicecertificate-element.md) as shown on the following example.</span></span>  
  
7. <span data-ttu-id="bc864-133">将 `customCertificateValidatorType` 属性设置为验证程序类型。</span><span class="sxs-lookup"><span data-stu-id="bc864-133">Set the `customCertificateValidatorType` attribute to the validator type.</span></span>  
  
8. <span data-ttu-id="bc864-134">将 `certificateValidationMode` 属性设置为 `Custom`。</span><span class="sxs-lookup"><span data-stu-id="bc864-134">Set the `certificateValidationMode` attribute to `Custom`.</span></span> <span data-ttu-id="bc864-135">下面的示例将该属性设置为类型的命名空间和名称。</span><span class="sxs-lookup"><span data-stu-id="bc864-135">The following example sets the attribute to the namespace and name of the type.</span></span>  
  
    ```xml  
    <configuration>  
     <system.serviceModel>  
      <behaviors>  
       <endpointBehaviors>  
        <behavior name="clientBehavior">  
         <clientCredentials>  
          <serviceCertificate>  
           <authentication certificateValidationMode="Custom"
                  customCertificateValidatorType=  
             "Samples.CustomX509CertificateValidator, client"/>  
          </serviceCertificate>  
         </clientCredentials>  
        </behavior>  
       </endpointBehaviors>  
      </behaviors>  
     </system.serviceModel>  
    </configuration>  
    ```  
  
#### <a name="to-specify-a-custom-certificate-validator-using-code-on-the-service"></a><span data-ttu-id="bc864-136">使用服务上的代码指定自定义证书验证程序</span><span class="sxs-lookup"><span data-stu-id="bc864-136">To specify a custom certificate validator using code on the service</span></span>  
  
1. <span data-ttu-id="bc864-137">指定 <xref:System.ServiceModel.Description.ServiceCredentials.ClientCertificate%2A> 属性的自定义证书验证程序。</span><span class="sxs-lookup"><span data-stu-id="bc864-137">Specify the custom certificate validator on the <xref:System.ServiceModel.Description.ServiceCredentials.ClientCertificate%2A> property.</span></span> <span data-ttu-id="bc864-138">您可以使用 <xref:System.ServiceModel.ServiceHostBase.Credentials%2A> 属性访问服务凭据。</span><span class="sxs-lookup"><span data-stu-id="bc864-138">You can access the service credentials using the <xref:System.ServiceModel.ServiceHostBase.Credentials%2A> property.</span></span>  
  
2. <span data-ttu-id="bc864-139">将 <xref:System.ServiceModel.Security.X509ClientCertificateAuthentication.CertificateValidationMode%2A> 属性设置为 <xref:System.ServiceModel.Security.X509CertificateValidationMode.Custom>。</span><span class="sxs-lookup"><span data-stu-id="bc864-139">Set the <xref:System.ServiceModel.Security.X509ClientCertificateAuthentication.CertificateValidationMode%2A> property to <xref:System.ServiceModel.Security.X509CertificateValidationMode.Custom>.</span></span>  
  
 [!code-csharp[c_CustomCertificateValidator#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customcertificatevalidator/cs/source.cs#1)]
 [!code-vb[c_CustomCertificateValidator#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customcertificatevalidator/vb/source.vb#1)]  
  
#### <a name="to-specify-a-custom-certificate-validator-using-code-on-the-client"></a><span data-ttu-id="bc864-140">使用客户端上的代码指定自定义证书验证程序</span><span class="sxs-lookup"><span data-stu-id="bc864-140">To specify a custom certificate validator using code on the client</span></span>  
  
1. <span data-ttu-id="bc864-141">使用 <xref:System.ServiceModel.Security.X509ServiceCertificateAuthentication.CustomCertificateValidator%2A> 属性指定自定义证书验证程序。</span><span class="sxs-lookup"><span data-stu-id="bc864-141">Specify the custom certificate validator using the <xref:System.ServiceModel.Security.X509ServiceCertificateAuthentication.CustomCertificateValidator%2A> property.</span></span> <span data-ttu-id="bc864-142">您可以使用 <xref:System.ServiceModel.ServiceHostBase.Credentials%2A> 属性访问客户端凭据。</span><span class="sxs-lookup"><span data-stu-id="bc864-142">You can access the client credentials using the <xref:System.ServiceModel.ServiceHostBase.Credentials%2A> property.</span></span> <span data-ttu-id="bc864-143"> (由 [ ( 的元数据实用工具工具 ](../servicemodel-metadata-utility-tool-svcutil-exe.md) 生成的客户端类) 始终从类派生 <xref:System.ServiceModel.ClientBase%601> 。 ) </span><span class="sxs-lookup"><span data-stu-id="bc864-143">(The client class generated by [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md) always derives from the <xref:System.ServiceModel.ClientBase%601> class.)</span></span>  
  
2. <span data-ttu-id="bc864-144">将 <xref:System.ServiceModel.Security.X509ServiceCertificateAuthentication.CertificateValidationMode%2A> 属性设置为 <xref:System.ServiceModel.Security.X509CertificateValidationMode.Custom>。</span><span class="sxs-lookup"><span data-stu-id="bc864-144">Set the <xref:System.ServiceModel.Security.X509ServiceCertificateAuthentication.CertificateValidationMode%2A> property to <xref:System.ServiceModel.Security.X509CertificateValidationMode.Custom>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bc864-145">示例</span><span class="sxs-lookup"><span data-stu-id="bc864-145">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="bc864-146">说明</span><span class="sxs-lookup"><span data-stu-id="bc864-146">Description</span></span>  

 <span data-ttu-id="bc864-147">下面的示例演示自定义证书验证程序的实现及其在服务上的用法。</span><span class="sxs-lookup"><span data-stu-id="bc864-147">The following sample shows an implementation of a custom certificate validator and its usage on the service.</span></span>  
  
### <a name="code"></a><span data-ttu-id="bc864-148">代码</span><span class="sxs-lookup"><span data-stu-id="bc864-148">Code</span></span>  

 [!code-csharp[c_CustomCertificateValidator#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customcertificatevalidator/cs/source.cs#3)]
 [!code-vb[c_CustomCertificateValidator#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customcertificatevalidator/vb/source.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="bc864-149">请参阅</span><span class="sxs-lookup"><span data-stu-id="bc864-149">See also</span></span>

- <xref:System.IdentityModel.Selectors.X509CertificateValidator>
