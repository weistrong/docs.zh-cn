---
description: 了解详细信息：如何：设置签名确认
title: 如何：设置签名确认
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- signature confirmation
- WCF, security
ms.assetid: 2424c137-c7c2-4aa9-8d5d-a066e12fefda
ms.openlocfilehash: 158ec2a5f74038f5c1ca1af847f57457a8881974
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643184"
---
# <a name="how-to-set-up-a-signature-confirmation"></a><span data-ttu-id="5d5f8-103">如何：设置签名确认</span><span class="sxs-lookup"><span data-stu-id="5d5f8-103">How to: Set Up a Signature Confirmation</span></span>

<span data-ttu-id="5d5f8-104">*签名确认* 是一种机制，用于消息发起方确保收到的答复是为了响应发送方的原始消息。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-104">*Signature confirmation* is a mechanism for a message initiator to ensure that a received reply was generated in response to the sender's original message.</span></span> <span data-ttu-id="5d5f8-105">WS-Security 1.1 规范中对签名确认进行了定义。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-105">Signature confirmation is defined in the WS-Security 1.1 specification.</span></span> <span data-ttu-id="5d5f8-106">如果终结点支持 WS-Security 1.0，则不能使用签名确认。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-106">If an endpoint supports WS-Security 1.0, you cannot use signature confirmation.</span></span>

<span data-ttu-id="5d5f8-107">下面的过程指定如何使用 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement> 来启用签名确认。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-107">The following procedures specify how to enable signature confirmation using an <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>.</span></span> <span data-ttu-id="5d5f8-108">可以对 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> 使用相同的过程。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-108">You can use the same procedure with a <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>.</span></span> <span data-ttu-id="5d5f8-109">此过程基于 [如何：使用 SecurityBindingElement 创建自定义绑定](how-to-create-a-custom-binding-using-the-securitybindingelement.md)中的基本步骤。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-109">The procedure builds upon the basic steps found in [How to: Create a Custom Binding Using the SecurityBindingElement](how-to-create-a-custom-binding-using-the-securitybindingelement.md).</span></span>

### <a name="to-enable-signature-confirmation-in-code"></a><span data-ttu-id="5d5f8-110">在代码中启用签名确认</span><span class="sxs-lookup"><span data-stu-id="5d5f8-110">To enable signature confirmation in code</span></span>

1. <span data-ttu-id="5d5f8-111">创建的 <xref:System.ServiceModel.Channels.BindingElementCollection> 类的实例。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-111">Create an instance of the <xref:System.ServiceModel.Channels.BindingElementCollection> class.</span></span>

2. <span data-ttu-id="5d5f8-112">创建类的实例  <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> 。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-112">Create an instance of the  <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> class.</span></span>

3. <span data-ttu-id="5d5f8-113">将 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement.RequireSignatureConfirmation%2A> 设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-113">Set the <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement.RequireSignatureConfirmation%2A> to `true`.</span></span>

4. <span data-ttu-id="5d5f8-114">将安全元素添加到绑定集合中。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-114">Add the security element to the binding collection.</span></span>

5. <span data-ttu-id="5d5f8-115">按照 [如何：使用 SecurityBindingElement 创建自定义绑定](how-to-create-a-custom-binding-using-the-securitybindingelement.md)中的说明创建自定义绑定。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-115">Create a custom binding, as specified in [How to: Create a Custom Binding Using the SecurityBindingElement](how-to-create-a-custom-binding-using-the-securitybindingelement.md).</span></span>

### <a name="to-enable-signature-confirmation-in-configuration"></a><span data-ttu-id="5d5f8-116">在配置中启用签名确认</span><span class="sxs-lookup"><span data-stu-id="5d5f8-116">To enable signature confirmation in configuration</span></span>

1. <span data-ttu-id="5d5f8-117">将 `<customBinding>` 元素添加到配置文件的 `<bindings>` 节。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-117">Add a `<customBinding>` element to the `<bindings>` section of the configuration file.</span></span>

2. <span data-ttu-id="5d5f8-118">添加一个 `<binding>` 元素，并将 name 属性设置为适当的值。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-118">Add a `<binding>` element and set the name attribute to an appropriate value.</span></span>

3. <span data-ttu-id="5d5f8-119">添加一个适当的编码元素。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-119">Add an appropriate encoding element.</span></span> <span data-ttu-id="5d5f8-120">下面的示例添加了一个 `<TextMessageEncoding>` 元素。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-120">The following example adds a `<TextMessageEncoding>` element.</span></span>

4. <span data-ttu-id="5d5f8-121">添加一个 `<security>` 子元素并将 `requireSignatureConfirmation` 属性设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-121">Add a `<security>` child element and set the `requireSignatureConfirmation` attribute to `true`.</span></span>

5. <span data-ttu-id="5d5f8-122">可选。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-122">Optional.</span></span> <span data-ttu-id="5d5f8-123">若要在启动过程中启用签名确认，请添加一个 [\<secureConversationBootstrap>](../../configure-apps/file-schema/wcf/secureconversationbootstrap.md) 子元素，并将 `requireSignatureConfirmation` 属性设置为 `true` 。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-123">To enable signature confirmation during the bootstrap, add a [\<secureConversationBootstrap>](../../configure-apps/file-schema/wcf/secureconversationbootstrap.md) child element and set the `requireSignatureConfirmation` attribute to `true`.</span></span>

6. <span data-ttu-id="5d5f8-124">添加一个适当的传输元素。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-124">Add an appropriate transport element.</span></span> <span data-ttu-id="5d5f8-125">下面的示例添加一个 [\<httpTransport>](../../configure-apps/file-schema/wcf/httptransport.md) ：</span><span class="sxs-lookup"><span data-stu-id="5d5f8-125">The following example adds an [\<httpTransport>](../../configure-apps/file-schema/wcf/httptransport.md):</span></span>

    ```xml
    <bindings>
      <customBinding>
        <binding name="SignatureConfirmationBinding">
          <security requireSignatureConfirmation="true">
            <secureConversationBootstrap requireSignatureConfirmation="true" />
              </security>
           <textMessageEncoding />
             <httpTransport />
        </binding>
      </customBinding>
    </bindings>
    ```

## <a name="example"></a><span data-ttu-id="5d5f8-126">示例</span><span class="sxs-lookup"><span data-stu-id="5d5f8-126">Example</span></span>

<span data-ttu-id="5d5f8-127">下面的代码创建 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> 的实例并将 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement.RequireSignatureConfirmation%2A> 属性设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-127">The following code creates an instance of the <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> and sets the <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement.RequireSignatureConfirmation%2A> property to `true`.</span></span> <span data-ttu-id="5d5f8-128">请注意，此示例不使用上一示例中所示的 `<secureConversationBootstrap>` 元素。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-128">Note that this example does not use the `<secureConversationBootstrap>` element shown in the preceding example.</span></span> <span data-ttu-id="5d5f8-129">此示例演示了使用 Windows（Kerberos 协议）令牌时的签名确认。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-129">This example demonstrates signature confirmation when using a Windows (Kerberos protocol) token.</span></span> <span data-ttu-id="5d5f8-130">在本例中，在来自服务的所有响应中均返回客户端的签名，并且该签名由客户端进行确认。</span><span class="sxs-lookup"><span data-stu-id="5d5f8-130">In this case, the signature of the client is returned in all responses from the service and is confirmed by the client.</span></span>

[!code-csharp[c_SignatureConfirmation#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_signatureconfirmation/cs/source.cs#1)]
[!code-vb[c_SignatureConfirmation#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_signatureconfirmation/vb/source.vb#1)]

## <a name="see-also"></a><span data-ttu-id="5d5f8-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="5d5f8-131">See also</span></span>

- <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
- <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
- <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateMutualCertificateBindingElement%2A>
- [<span data-ttu-id="5d5f8-132">如何：使用 SecurityBindingElement 创建自定义绑定</span><span class="sxs-lookup"><span data-stu-id="5d5f8-132">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [<span data-ttu-id="5d5f8-133">如何：为指定的身份验证模式创建 SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="5d5f8-133">How to: Create a SecurityBindingElement for a Specified Authentication Mode</span></span>](how-to-create-a-securitybindingelement-for-a-specified-authentication-mode.md)
