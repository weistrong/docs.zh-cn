---
description: 了解详细信息：如何：为安全会话创建安全上下文令牌
title: 如何：为安全会话创建安全上下文令牌
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 640676b6-c75a-4ff7-aea4-b1a1524d71b2
ms.openlocfilehash: 29e8b694779f2a960f449469438c3aed0d0a815d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99734667"
---
# <a name="how-to-create-a-security-context-token-for-a-secure-session"></a><span data-ttu-id="57541-103">如何：为安全会话创建安全上下文令牌</span><span class="sxs-lookup"><span data-stu-id="57541-103">How to: Create a Security Context Token for a Secure Session</span></span>

<span data-ttu-id="57541-104">通过在安全会话中使用有状态安全上下文令牌 (SCT)，可以使该会话避免因为重新使用服务而受到影响。</span><span class="sxs-lookup"><span data-stu-id="57541-104">By using a stateful security context token (SCT) in a secure session, the session can withstand the service being recycled.</span></span> <span data-ttu-id="57541-105">例如，如果在安全会话中使用了无状态 SCT 并且 Internet 信息服务 (IIS) 被重置，则与该服务相关联的会话数据将丢失。</span><span class="sxs-lookup"><span data-stu-id="57541-105">For instance, when a stateless SCT is used in a secure session and Internet Information Services (IIS) is reset, then the session data that is associated with the service is lost.</span></span> <span data-ttu-id="57541-106">这些会话数据包括一个 SCT 令牌缓存。</span><span class="sxs-lookup"><span data-stu-id="57541-106">This session data includes an SCT token cache.</span></span> <span data-ttu-id="57541-107">因此，当客户端下一次向该服务发送无状态 SCT 时，将返回错误，这是因为无法检索到与该 SCT 相关联的密钥。</span><span class="sxs-lookup"><span data-stu-id="57541-107">So, the next time a client sends the service a stateless SCT, an error is returned, because the key that is associated with the SCT cannot be retrieved.</span></span> <span data-ttu-id="57541-108">但是，如果使用有状态 SCT，则与该 SCT 相关联的密钥将包含在该 SCT 中。</span><span class="sxs-lookup"><span data-stu-id="57541-108">If, however, a stateful SCT is used, then the key that is associated with the SCT is contained within the SCT.</span></span> <span data-ttu-id="57541-109">由于密钥包含在 SCT 中并因而包含在消息中，因此安全会话不会因为重新使用服务而受到影响。</span><span class="sxs-lookup"><span data-stu-id="57541-109">Because the key is contained within the SCT and thus contained within the message, the secure session is not affected by the service being recycled.</span></span> <span data-ttu-id="57541-110">默认情况下，Windows Communication Foundation (WCF) 在安全会话中使用无状态 Sct。</span><span class="sxs-lookup"><span data-stu-id="57541-110">By default, Windows Communication Foundation (WCF) uses stateless SCTs in a secure session.</span></span> <span data-ttu-id="57541-111">本主题详细介绍如何在安全会话中使用有状态 SCT。</span><span class="sxs-lookup"><span data-stu-id="57541-111">This topic details how to use stateful SCTs in a secure session.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="57541-112">如果安全会话涉及到派生自 <xref:System.ServiceModel.Channels.IDuplexChannel> 的协定，则无法在该安全会话中使用有状态 SCT。</span><span class="sxs-lookup"><span data-stu-id="57541-112">Stateful SCTs cannot be used in a secure session that involves a contract that derives from <xref:System.ServiceModel.Channels.IDuplexChannel>.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="57541-113">对于在安全会话中使用有状态 SCT 的应用程序，服务的线程标识必须是具有关联用户配置文件的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="57541-113">For applications that use stateful SCTs in a secure session, the thread identity for the service must be a user account that has an associated user profile.</span></span> <span data-ttu-id="57541-114">如果服务在不具有用户配置文件的帐户下运行（如 `Local Service`），则可能引发异常。</span><span class="sxs-lookup"><span data-stu-id="57541-114">When the service is run under an account that does not have a user profile, such as `Local Service`, an exception may be thrown.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="57541-115">当需要在 Windows XP 上进行模拟时，请不要在安全会话中使用有状态 SCT。</span><span class="sxs-lookup"><span data-stu-id="57541-115">When impersonation is required on Windows XP, use a secure session without a stateful SCT.</span></span> <span data-ttu-id="57541-116">如果在模拟时使用有状态 SCT，则会引发 <xref:System.InvalidOperationException>。</span><span class="sxs-lookup"><span data-stu-id="57541-116">When stateful SCTs are used with impersonation, an <xref:System.InvalidOperationException> is thrown.</span></span> <span data-ttu-id="57541-117">有关详细信息，请参阅 [不支持的方案](unsupported-scenarios.md)。</span><span class="sxs-lookup"><span data-stu-id="57541-117">For more information, see [Unsupported Scenarios](unsupported-scenarios.md).</span></span>  
  
### <a name="to-use-stateful-scts-in-a-secure-session"></a><span data-ttu-id="57541-118">在安全会话中使用有状态 SCT</span><span class="sxs-lookup"><span data-stu-id="57541-118">To use stateful SCTs in a secure session</span></span>  
  
- <span data-ttu-id="57541-119">创建一个自定义绑定，该绑定指定由使用有状态 SCT 的安全会话来保护 SOAP 消息。</span><span class="sxs-lookup"><span data-stu-id="57541-119">Create a custom binding that specifies that SOAP messages are protected by a secure session that uses a stateful SCT.</span></span>  
  
    1. <span data-ttu-id="57541-120">通过将添加 [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) 到服务的配置文件来定义自定义绑定。</span><span class="sxs-lookup"><span data-stu-id="57541-120">Define a custom binding, by adding a [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) to the configuration file for the service.</span></span>  
  
        ```xml  
        <customBinding>  
        </customBinding>
        ```  
  
    2. <span data-ttu-id="57541-121">将一个 [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) 子元素添加到中 [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="57541-121">Add a [\<binding>](../../configure-apps/file-schema/wcf/bindings.md) child element to the [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md).</span></span>  
  
         <span data-ttu-id="57541-122">通过在配置文件中将 `name` 属性设置为一个唯一的名称，指定一个绑定名称。</span><span class="sxs-lookup"><span data-stu-id="57541-122">Specify a binding name by setting the `name` attribute to a unique name within the configuration file.</span></span>  
  
        ```xml  
        <binding name="StatefulSCTSecureSession">  
        </binding>
        ```  
  
    3. <span data-ttu-id="57541-123">通过将子元素添加到，指定发送到此服务的消息的身份验证模式 [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="57541-123">Specify the authentication mode for messages sent to and from this service by adding a [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) child element to the [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md).</span></span>  
  
         <span data-ttu-id="57541-124">通过将 `authenticationMode` 属性设置为 `SecureConversation`，指定使用安全会话。</span><span class="sxs-lookup"><span data-stu-id="57541-124">Specify that a secure session is used by setting the `authenticationMode` attribute to `SecureConversation`.</span></span> <span data-ttu-id="57541-125">通过将 `requireSecurityContextCancellation` 属性设置为 `false`，指定使用有状态 SCT。</span><span class="sxs-lookup"><span data-stu-id="57541-125">Specify that stateful SCTs are used by setting the `requireSecurityContextCancellation` attribute to `false`.</span></span>  
  
        ```xml  
        <security authenticationMode="SecureConversation"  
                  requireSecurityContextCancellation="false">
        </security>
        ```  
  
    4. <span data-ttu-id="57541-126">指定在通过将一个子元素添加到来建立安全会话时如何对客户端进行身份验证 [\<secureConversationBootstrap>](../../configure-apps/file-schema/wcf/secureconversationbootstrap.md) [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="57541-126">Specify how the client is authenticated while the secure session is established by adding a [\<secureConversationBootstrap>](../../configure-apps/file-schema/wcf/secureconversationbootstrap.md) child element to the [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md).</span></span>  
  
         <span data-ttu-id="57541-127">通过设置 `authenticationMode` 属性，指定如何对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="57541-127">Specify how the client is authenticated by setting the `authenticationMode` attribute.</span></span>  
  
        ```xml  
        <secureConversationBootstrap authenticationMode="UserNameForCertificate" />  
        ```  
  
    5. <span data-ttu-id="57541-128">通过添加编码元素（例如）来指定消息编码 [\<textMessageEncoding>](../../configure-apps/file-schema/wcf/textmessageencoding.md) 。</span><span class="sxs-lookup"><span data-stu-id="57541-128">Specify the message encoding by adding an encoding element, such as [\<textMessageEncoding>](../../configure-apps/file-schema/wcf/textmessageencoding.md).</span></span>  
  
        ```xml  
        <textMessageEncoding />  
        ```  
  
    6. <span data-ttu-id="57541-129">通过添加传输元素（例如）来指定传输 [\<httpTransport>](../../configure-apps/file-schema/wcf/httptransport.md) 。</span><span class="sxs-lookup"><span data-stu-id="57541-129">Specify the transport by adding a transport element, such as the [\<httpTransport>](../../configure-apps/file-schema/wcf/httptransport.md).</span></span>  
  
        ```xml  
        <httpTransport />  
        ```  
  
     <span data-ttu-id="57541-130">下面的代码示例使用配置来指定一个自定义绑定，消息可以将该绑定与安全会话中的有状态 SCT 结合使用。</span><span class="sxs-lookup"><span data-stu-id="57541-130">The following code example uses configuration to specify a custom binding that messages can use with stateful SCTs in a secure session.</span></span>  
  
    ```xml  
    <customBinding>  
      <binding name="StatefulSCTSecureSession">  
        <security authenticationMode="SecureConversation"  
                  requireSecurityContextCancellation="false">  
          <secureConversationBootstrap authenticationMode="UserNameForCertificate" />  
        </security>  
        <textMessageEncoding />  
        <httpTransport />  
      </binding>  
    </customBinding>  
    ```  
  
## <a name="example"></a><span data-ttu-id="57541-131">示例</span><span class="sxs-lookup"><span data-stu-id="57541-131">Example</span></span>  

 <span data-ttu-id="57541-132">下面的代码示例创建一个自定义绑定，该绑定使用 <xref:System.ServiceModel.Configuration.AuthenticationMode.MutualCertificate> 身份验证模式启动安全会话。</span><span class="sxs-lookup"><span data-stu-id="57541-132">The following code example creates a custom binding that uses the <xref:System.ServiceModel.Configuration.AuthenticationMode.MutualCertificate> authentication mode to bootstrap a secure session.</span></span>  
  
 [!code-csharp[c_CreateStatefulSCT#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_createstatefulsct/cs/secureservice.cs#2)]
 [!code-vb[c_CreateStatefulSCT#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_createstatefulsct/vb/secureservice.vb#2)]  
  
 <span data-ttu-id="57541-133">将 Windows 身份验证与有状态的 SCT 结合使用时，WCF 不会 <xref:System.ServiceModel.ServiceSecurityContext.WindowsIdentity%2A> 使用实际调用方的标识来填充属性，而是将属性设置为匿名。</span><span class="sxs-lookup"><span data-stu-id="57541-133">When Windows authentication is used in combination with a stateful SCT, WCF does not populate the <xref:System.ServiceModel.ServiceSecurityContext.WindowsIdentity%2A> property with the actual caller's identity but instead sets the property to anonymous.</span></span> <span data-ttu-id="57541-134">因为 WCF 安全性必须为传入 SCT 的每个请求重新创建服务安全上下文的内容，所以服务器不会跟踪内存中的安全会话。</span><span class="sxs-lookup"><span data-stu-id="57541-134">Because WCF security must re-create the content of the service security context for every request from the incoming SCT, the server does not keep track of the security session in the memory.</span></span> <span data-ttu-id="57541-135">因为不可能将 <xref:System.Security.Principal.WindowsIdentity> 实例序列化为 SCT，所以 <xref:System.ServiceModel.ServiceSecurityContext.WindowsIdentity%2A> 属性返回一个匿名标识。</span><span class="sxs-lookup"><span data-stu-id="57541-135">Because it is impossible to serialize the <xref:System.Security.Principal.WindowsIdentity> instance into the SCT, the <xref:System.ServiceModel.ServiceSecurityContext.WindowsIdentity%2A> property returns an anonymous identity.</span></span>  
  
 <span data-ttu-id="57541-136">下面的配置演示这一行为。</span><span class="sxs-lookup"><span data-stu-id="57541-136">The following configuration exhibits this behavior.</span></span>  
  
```xml  
<customBinding>  
  <binding name="Cancellation">  
       <textMessageEncoding />  
        <security
            requireSecurityContextCancellation="false">  
              <secureConversationBootstrap />  
        </security>  
    <httpTransport />  
  </binding>  
</customBinding>  
```  
  
## <a name="see-also"></a><span data-ttu-id="57541-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="57541-137">See also</span></span>

- [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md)
