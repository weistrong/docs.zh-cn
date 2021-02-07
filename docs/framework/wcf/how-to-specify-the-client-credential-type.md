---
description: 了解详细信息：如何：指定客户端凭据类型
title: 如何：指定客户端凭据类型
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- security credentials, adding to SOAP messages
- WCF, security
ms.assetid: 10f51bee-5f92-4c1a-9126-fa5418535d8f
ms.openlocfilehash: f6536778e8814a1b5a4c03e22c0fe4108f89b6eb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99752530"
---
# <a name="how-to-specify-the-client-credential-type"></a><span data-ttu-id="835a5-103">如何：指定客户端凭据类型</span><span class="sxs-lookup"><span data-stu-id="835a5-103">How to: Specify the Client Credential Type</span></span>

<span data-ttu-id="835a5-104">设置安全模式（传输或消息）后，您可以设置客户端凭据类型。</span><span class="sxs-lookup"><span data-stu-id="835a5-104">After setting a security mode (either transport or message), you have the option of setting the client credential type.</span></span> <span data-ttu-id="835a5-105">此属性指定客户端必须向服务提供以进行身份验证的凭据类型。</span><span class="sxs-lookup"><span data-stu-id="835a5-105">This property specifies what type of credential the client must provide to the service for authentication.</span></span> <span data-ttu-id="835a5-106">有关在设置客户端凭据类型) 之前设置安全模式 (必需步骤的详细信息，请参阅 [如何：设置安全模式](how-to-set-the-security-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="835a5-106">For more information about setting the security mode (a necessary step before setting the client credential type), see [How to: Set the Security Mode](how-to-set-the-security-mode.md).</span></span>  
  
### <a name="to-set-the-client-credential-type-in-code"></a><span data-ttu-id="835a5-107">在代码中设置客户端凭据类型</span><span class="sxs-lookup"><span data-stu-id="835a5-107">To set the client credential type in code</span></span>  
  
1. <span data-ttu-id="835a5-108">创建服务将使用的绑定的实例。</span><span class="sxs-lookup"><span data-stu-id="835a5-108">Create an instance of the binding that the service will use.</span></span> <span data-ttu-id="835a5-109">本示例使用 <xref:System.ServiceModel.WSHttpBinding> 绑定。</span><span class="sxs-lookup"><span data-stu-id="835a5-109">This example uses the <xref:System.ServiceModel.WSHttpBinding> binding.</span></span>  
  
2. <span data-ttu-id="835a5-110">将 <xref:System.ServiceModel.WSHttpSecurity.Mode%2A> 属性设置为适当的值。</span><span class="sxs-lookup"><span data-stu-id="835a5-110">Set the <xref:System.ServiceModel.WSHttpSecurity.Mode%2A> property to an appropriate value.</span></span> <span data-ttu-id="835a5-111">本示例使用 Message 模式。</span><span class="sxs-lookup"><span data-stu-id="835a5-111">This example uses the Message mode.</span></span>  
  
3. <span data-ttu-id="835a5-112">将 <xref:System.ServiceModel.MessageSecurityOverHttp.ClientCredentialType%2A> 属性设置为适当的值。</span><span class="sxs-lookup"><span data-stu-id="835a5-112">Set the <xref:System.ServiceModel.MessageSecurityOverHttp.ClientCredentialType%2A> property to an appropriate value.</span></span> <span data-ttu-id="835a5-113">本示例将其设置为使用 Windows 身份验证 (<xref:System.ServiceModel.MessageCredentialType.Windows>)。</span><span class="sxs-lookup"><span data-stu-id="835a5-113">This example sets it to use Windows authentication (<xref:System.ServiceModel.MessageCredentialType.Windows>).</span></span>  
  
     [!code-csharp[c_ProgrammingSecurity#14](../../../samples/snippets/csharp/VS_Snippets_CFX/c_programmingsecurity/cs/source.cs#14)]
     [!code-vb[c_ProgrammingSecurity#14](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_programmingsecurity/vb/source.vb#14)]  
  
### <a name="to-set-the-client-credential-type-in-configuration"></a><span data-ttu-id="835a5-114">在配置中设置客户端凭据类型</span><span class="sxs-lookup"><span data-stu-id="835a5-114">To set the client credential type in configuration</span></span>  
  
1. <span data-ttu-id="835a5-115">将一个 [\<system.serviceModel>](../configure-apps/file-schema/wcf/system-servicemodel.md) 元素添加到配置文件中。</span><span class="sxs-lookup"><span data-stu-id="835a5-115">Add a [\<system.serviceModel>](../configure-apps/file-schema/wcf/system-servicemodel.md) element to the configuration file.</span></span>  
  
2. <span data-ttu-id="835a5-116">添加元素作为子元素 [\<bindings>](../configure-apps/file-schema/wcf/bindings.md) 。</span><span class="sxs-lookup"><span data-stu-id="835a5-116">As a child element, add a [\<bindings>](../configure-apps/file-schema/wcf/bindings.md) element.</span></span>  
  
3. <span data-ttu-id="835a5-117">添加一个相应的绑定。</span><span class="sxs-lookup"><span data-stu-id="835a5-117">Add an appropriate binding.</span></span> <span data-ttu-id="835a5-118">此示例使用 [\<wsHttpBinding>](../configure-apps/file-schema/wcf/wshttpbinding.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="835a5-118">This example uses the [\<wsHttpBinding>](../configure-apps/file-schema/wcf/wshttpbinding.md) element.</span></span>  
  
4. <span data-ttu-id="835a5-119">添加 [\<binding>](../configure-apps/file-schema/wcf/bindings.md) 元素，并将 `name` 属性设置为合适的值。</span><span class="sxs-lookup"><span data-stu-id="835a5-119">Add a [\<binding>](../configure-apps/file-schema/wcf/bindings.md) element and set the `name` attribute to an appropriate value.</span></span> <span data-ttu-id="835a5-120">本示例使用名称“SecureBinding”。</span><span class="sxs-lookup"><span data-stu-id="835a5-120">This example uses the name "SecureBinding".</span></span>  
  
5. <span data-ttu-id="835a5-121">添加一个 `<security>` 绑定。</span><span class="sxs-lookup"><span data-stu-id="835a5-121">Add a `<security>` binding.</span></span> <span data-ttu-id="835a5-122">将 `mode` 属性设置为适当的值。</span><span class="sxs-lookup"><span data-stu-id="835a5-122">Set the `mode` attribute to an appropriate value.</span></span> <span data-ttu-id="835a5-123">本示例将其设置为 `"Message"`。</span><span class="sxs-lookup"><span data-stu-id="835a5-123">This example sets it to `"Message"`.</span></span>  
  
6. <span data-ttu-id="835a5-124">添加一个 `<message>` 或 `<transport>` 元素，具体由安全模式确定。</span><span class="sxs-lookup"><span data-stu-id="835a5-124">Add either a `<message>` or `<transport>` element, as determined by the security mode.</span></span> <span data-ttu-id="835a5-125">将 `clientCredentialType` 属性设置为适当的值。</span><span class="sxs-lookup"><span data-stu-id="835a5-125">Set the `clientCredentialType` attribute to an appropriate value.</span></span> <span data-ttu-id="835a5-126">本示例使用 `"Windows"`。</span><span class="sxs-lookup"><span data-stu-id="835a5-126">This example uses `"Windows"`.</span></span>  
  
    ```xml  
    <system.serviceModel>  
      <bindings>  
        <wsHttpBinding>  
          <binding name="SecureBinding">  
            <security mode="Message">  
                 <message clientCredentialType="Windows" />  
             </security>  
          </binding>  
        </wsHttpBinding>  
      </bindings>  
    </system.serviceModel>  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="835a5-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="835a5-127">See also</span></span>

- [<span data-ttu-id="835a5-128">保证服务的安全</span><span class="sxs-lookup"><span data-stu-id="835a5-128">Securing Services</span></span>](securing-services.md)
- [<span data-ttu-id="835a5-129">如何：设置安全模式</span><span class="sxs-lookup"><span data-stu-id="835a5-129">How to: Set the Security Mode</span></span>](how-to-set-the-security-mode.md)
