---
description: 了解详细信息：数字签名的加密
title: 数字签名的加密
ms.date: 03/30/2017
helpviewer_keywords:
- encryption of digital signatures [WCF]
- digital signatures [WCF], encryption
- digital signatures [WCF]
ms.assetid: 0868866d-40b4-4341-8e42-eee3b7f15b69
ms.openlocfilehash: a68cea324fd5c2619f501eaf42bc518c17b89a6e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99704844"
---
# <a name="encryption-of-digital-signatures"></a><span data-ttu-id="2d481-103">数字签名的加密</span><span class="sxs-lookup"><span data-stu-id="2d481-103">Encryption of Digital Signatures</span></span>

<span data-ttu-id="2d481-104">默认情况下，会对消息进行签名和加密，并对签名进行数字加密。</span><span class="sxs-lookup"><span data-stu-id="2d481-104">By default, a message is signed and encrypted, and the signature is digitally encrypted.</span></span> <span data-ttu-id="2d481-105">你可以对此进行控制，方法是用 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement> 或 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> 的实例创建一个自定义绑定，然后将其中一个类的 `MessageProtectionOrder` 属性设置为一个 <xref:System.ServiceModel.Security.MessageProtectionOrder> 枚举值。</span><span class="sxs-lookup"><span data-stu-id="2d481-105">You can control this by creating a custom binding with an instance of the <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement> or the <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> and then setting the `MessageProtectionOrder` property of either class to a <xref:System.ServiceModel.Security.MessageProtectionOrder> enumeration value.</span></span> <span data-ttu-id="2d481-106">默认值为 <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncryptAndEncryptSignature>。</span><span class="sxs-lookup"><span data-stu-id="2d481-106">The default is <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncryptAndEncryptSignature>.</span></span> <span data-ttu-id="2d481-107">此过程要比仅仅签名和加密多花 10% 到 40% 的时间。</span><span class="sxs-lookup"><span data-stu-id="2d481-107">This process takes 10 to 40 percent longer than simply signing and encrypting.</span></span> <span data-ttu-id="2d481-108">但是，禁用签名的加密可能会使攻击者猜出消息的内容。</span><span class="sxs-lookup"><span data-stu-id="2d481-108">Disabling encryption of the signature, however, might allow an attacker to guess the contents of the message.</span></span> <span data-ttu-id="2d481-109">这种情况是可能的，原因是签名元素包含消息中每个签名部分的纯文本的哈希代码。</span><span class="sxs-lookup"><span data-stu-id="2d481-109">This is possible because the signature element contains the hash code of the plain text of every signed part in the message.</span></span> <span data-ttu-id="2d481-110">例如，尽管默认情况下加密了消息正文，可是未加密的签名包含消息正文的哈希代码。</span><span class="sxs-lookup"><span data-stu-id="2d481-110">For example, although the message body is encrypted by default, the unencrypted signature contains the hash code of the message body.</span></span> <span data-ttu-id="2d481-111">如果消息简短，攻击者有可能推测出内容。</span><span class="sxs-lookup"><span data-stu-id="2d481-111">If the message is small, an attacker might be able to deduce the contents.</span></span> <span data-ttu-id="2d481-112">对签名进行加密可减小或消除这种可能性。</span><span class="sxs-lookup"><span data-stu-id="2d481-112">Encrypting the signature reduces or eliminates this possibility.</span></span>  
  
 <span data-ttu-id="2d481-113">因此，应仅在内容价值较低时才禁用签名的加密，比如在发送无安全问题的大型二进制文件时，而禁用可以显著提高性能。</span><span class="sxs-lookup"><span data-stu-id="2d481-113">Therefore, disable encryption of the signature only when the value of the content is low, and the performance gain will be significant, for example, when sending large binary files that have no security implications.</span></span>  
  
### <a name="to-disable-digital-signing"></a><span data-ttu-id="2d481-114">禁用数字签名</span><span class="sxs-lookup"><span data-stu-id="2d481-114">To disable digital signing</span></span>  
  
1. <span data-ttu-id="2d481-115">创建 <xref:System.ServiceModel.Channels.CustomBinding>。</span><span class="sxs-lookup"><span data-stu-id="2d481-115">Create a <xref:System.ServiceModel.Channels.CustomBinding>.</span></span> <span data-ttu-id="2d481-116">有关详细信息，请参阅 [如何：使用 SecurityBindingElement 创建自定义绑定](how-to-create-a-custom-binding-using-the-securitybindingelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2d481-116">For more information, see [How to: Create a Custom Binding Using the SecurityBindingElement](how-to-create-a-custom-binding-using-the-securitybindingelement.md).</span></span>  
  
2. <span data-ttu-id="2d481-117">将 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement> 或 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> 添加到绑定集合。</span><span class="sxs-lookup"><span data-stu-id="2d481-117">Add either an <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement> or a <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> to the binding collection.</span></span>  
  
3. <span data-ttu-id="2d481-118">将 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement.MessageProtectionOrder%2A?displayProperty=nameWithType> 属性设置为 <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncrypt>，或将 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement.MessageProtectionOrder%2A?displayProperty=nameWithType> 属性设置为 <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncrypt>。</span><span class="sxs-lookup"><span data-stu-id="2d481-118">Set the <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement.MessageProtectionOrder%2A?displayProperty=nameWithType> property to <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncrypt>, or set the <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement.MessageProtectionOrder%2A?displayProperty=nameWithType> property to <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncrypt>.</span></span>  
  
 <span data-ttu-id="2d481-119">有关创建自定义绑定的详细信息，请参阅 [创建 User-Defined 绑定](../extending/creating-user-defined-bindings.md)。</span><span class="sxs-lookup"><span data-stu-id="2d481-119">For more information about creating custom bindings, see [Creating User-Defined Bindings](../extending/creating-user-defined-bindings.md).</span></span> <span data-ttu-id="2d481-120">有关为特定身份验证模式创建自定义绑定的详细信息，请参阅 [如何：为指定的身份验证模式创建 SecurityBindingElement](how-to-create-a-securitybindingelement-for-a-specified-authentication-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="2d481-120">For more information about creating a custom binding for a specific authentication mode, see [How to: Create a SecurityBindingElement for a Specified Authentication Mode](how-to-create-a-securitybindingelement-for-a-specified-authentication-mode.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d481-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="2d481-121">See also</span></span>

- <xref:System.ServiceModel.Security.MessageProtectionOrder>
- <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
- <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
- [<span data-ttu-id="2d481-122">如何：使用 SecurityBindingElement 创建自定义绑定</span><span class="sxs-lookup"><span data-stu-id="2d481-122">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [<span data-ttu-id="2d481-123">创建用户定义的绑定</span><span class="sxs-lookup"><span data-stu-id="2d481-123">Creating User-Defined Bindings</span></span>](../extending/creating-user-defined-bindings.md)
- [<span data-ttu-id="2d481-124">如何：为指定的身份验证模式创建 SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="2d481-124">How to: Create a SecurityBindingElement for a Specified Authentication Mode</span></span>](how-to-create-a-securitybindingelement-for-a-specified-authentication-mode.md)
